---
title: "Enable users for Direct Routing"
ms.reviewer: filippse
ms.date: 01/21/2025
ms.author: scottfrancis
author: sfrancis206
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: msteams
ms.localizationpriority: medium
search.appverid: MET150
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - Tier1
appliesto: 
  - Microsoft Teams
f1.keywords:
- NOCSH
description: "Learn how to enable users for Microsoft Teams Phone Direct Routing."
---

# Enable users for Direct Routing

This article describes how to enable users for Direct Routing and represents step 2 in the following steps for configuring Direct Routing:

- Step 1. [Connect the Session Border Controller (SBC) with Phone System and validate the connection](direct-routing-connect-the-sbc.md) .
- **Step 2. Enable users for Direct Routing** (this article).
- Step 3. [Configure voice routing](direct-routing-voice-routing.md).
- Step 4. [Translate numbers to an alternate format](direct-routing-translate-numbers.md). 

For information on all the steps required for setting up Direct Routing, see [Configure Direct Routing](direct-routing-configure.md).

When you're ready to enable users for Direct Routing, follow these steps: 

1. [Create a user in Microsoft 365 and assign a Teams Phone license](#create-a-user-and-assign-the-license).
1. [Ensure that the user is homed online](#ensure-that-the-user-is-homed-online).
1. [Configure the phone number and enable enterprise voice](#configure-the-phone-number-and-enable-enterprise-voice).
1. [Configure sending calls directly to voicemail](#configure-sending-calls-directly-to-voicemail).
1. [Assign Teams Only mode to users](#assign-teams-only-mode-to-users-to-ensure-calls-land-in-microsoft-teams).

## Create a user and assign the license

There are two options for creating a new user in Microsoft 365. However, we recommend that your organization chooses only one option to avoid routing issues: 

- Create the user in on-premises Active Directory and sync the user to the cloud. For more information, see [Integrate your on-premises directories with Microsoft Entra ID](/azure/active-directory/connect/active-directory-aadconnect).
- Create the user directly in the Microsoft 365 admin center. For more information, see [Add users individually or in bulk to Microsoft 365 or Office 365 - Admin Help](https://support.office.com/article/1970f7d6-03b5-442f-b385-5880b9c256ec). 

For information about license requirements, see [licensing and other requirements](direct-routing-plan.md#licensing-and-other-requirements) in [Plan Direct Routing](direct-routing-plan.md).

## Ensure that the user is homed online 

This step applies to Skype for Business Server Enterprise Voice enabled users being migrated to Teams Direct Routing.

Direct Routing requires the user to be homed online. You can check by looking at the `RegistrarPool` parameter, which needs to have a value in the infra.lync.com domain. Microsoft recommends, but doesn't require, that you change the LineURI from on-premises to online when migrating users to Teams Direct Routing. 

1. Connect a Microsoft Teams PowerShell session.

2. Issue the command:

    ```PowerShell
    Get-CsOnlineUser -Identity "<User name>" | fl RegistrarPool,OnPremLineUri,LineUri
    ``` 
    If `OnPremLineUri` is populated with a <E.164 phone number>, the phone number was assigned on-premises and synchronized to Microsoft 365. If you want to manage the phone number online, clear the parameter using on-premises Skype for Business Management Shell and synchronize to Microsoft 365 before configuring the phone number using Teams PowerShell.

1. From Skype for Business Management Shell, issue the command: 

   ```PowerShell
   Set-CsUser -Identity "<User name>" -LineUri $null
    ``` 
 > [!NOTE]
 > Don't set `EnterpriseVoiceEnabled` to False as there's no requirement to do so. Setting `EnterpriseVoiceEnabled` to False can lead to dial plan normalization issues if legacy Skype for Business phones are in use and the Tenant hybrid configuration is set with UseOnPremDialPlan $True.
    
   After the changes sync to Microsoft 365, the expected output of `Get-CsOnlineUser -Identity "<User name>" | fl RegistrarPool,OnPremLineUri,LineUri` is:

   ```console
   RegistrarPool                        : pool.infra.lync.com
   OnPremLineURI                        : 
   LineURI                              : 
   ```
 > [!NOTE]
 > All user's phone attributes must be managed online before you [decommission your on-premises Skype for Business environment](/skypeforbusiness/hybrid/decommission-on-prem-overview). 

## Upload Direct Routing numbers to your tenant

Uploading your Direct Routing phone numbers to Microsoft's telephone number management inventory supports future number management enhancements.

For example, if you upload your numbers, you can view them by using the PowerShell cmdlets [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment) and [Export-CsAcquiredPhoneNumber](/powershell/module/teams/export-csacquiredphonenumber) or in the Teams admin center under **Phone Numbers**.

Uploading your Direct Routing phone numbers to Microsoft's telephone number management inventory is optional. If you don't upload the phone numbers, you can still assign numbers to users. Assigning a number to a user automatically uploads the number to Microsoft's telephone number management inventory if it's not already there.

To upload Direct Routing telephone numbers to Microsoft's telephone number management inventory, use the [New-CsOnlineDirectRoutingTelephoneNumberUploadOrder](/powershell/module/teams/new-csonlinedirectroutingtelephonenumberuploadorder) cmdlet.

Uploading the numbers is an asynchronous operation. To see the status of your upload order, use the [Get-CsOnlineTelephoneNumberOrder](/powershell/module/teams/get-csonlinetelephonenumberorder) PowerShell cmdlet with **OrderType** set to `DirectRoutingNumberCreation`, as shown in the following example:

```PowerShell
 Get-CsOnlineTelephoneNumberOrder -OrderType DirectRoutingNumberCreation -OrderId <orderId>
```

> [!NOTE]
> Whenever porting Direct Routing numbers to Teams using another PSTN connectivity option, the numbers must be released from Microsoft's telephone number management inventory. After unassigning the numbers from the users and before your number port event, use the PowerShell cmdlet [New-CsOnlineTelephoneNumberReleaseOrder](/powershell/module/teams/new-csonlinetelephonenumberreleaseorder) to make the Direct Routing numbers available for porting. A release order can also be used if you don't want to keep your acquired Direct Routing numbers in Microsoft's inventory.

## Configure the phone number and enable enterprise voice 

After you create the user and assign a license, you must configure the user's online phone settings. The configuration of Cloud Voicemail for the user is automatic and no other configuration needs to be done.

You can configure the phone number by using the Teams admin center or by using Teams PowerShell.

### Use Teams admin center

1. Go to **Users** > **Manage users**.

2. Select a user.

2. Under **Account** > **General information**, select **Edit**.

3. Under **Assign phone number**, from the **Phone number type** drop-down menu, select **Direct Routing**.

4. Enter an assigned phone number and a phone number extension if applicable.

5. Select **Apply**.

   The account's general information now shows the assigned phone number and displays Direct Routing as the phone number type.

### Use PowerShell

1. Connect to a Microsoft Teams PowerShell session.

2. The next steps depend on whether you're managing the user's phone number on-premises or online. If you're managing the phone number on-premises, you must use the on-premises Skype for Business Management Shell, Control Panel, or one of the methods explained in [Decide how to manage attributes after decommissioning](/skypeforbusiness/hybrid/cloud-consolidation-managing-attributes).

   - If you're managing the user's phone number on-premises, you need to ensure that the user is Enterprise Voice enabled online by using the following command:

       ```PowerShell
       Set-CsPhoneNumberAssignment -Identity "<User name>" -EnterpriseVoiceEnabled $true
       ```
       
   - If you're managing the user's phone number online, you need to assign the phone number to the user by using the following command in Teams PowerShell. The user is automatically Enterprise Voice enabled by the command: 
 
       ```PowerShell
       Set-CsPhoneNumberAssignment -Identity "<User name>" -PhoneNumber <phone number> -PhoneNumberType DirectRouting
       ```
    
       For example, to add a phone number for user "Spencer Low," enter the following command: 

       ```PowerShell
       Set-CsPhoneNumberAssignment -Identity "spencer.low@contoso.com" -PhoneNumber "+14255388797" -PhoneNumberType DirectRouting
       ```
       If the users "Spencer Low" and "Stacy Quinn" share the same base number with unique extensions, enter the following command:
    
       ```PowerShell
       Set-CsPhoneNumberAssignment -Identity "spencer.low@contoso.com" -PhoneNumber "+14255388701;ext=1001" -PhoneNumberType DirectRouting
       Set-CsPhoneNumberAssignment -Identity "stacy.quinn@contoso.com" -PhoneNumber "+14255388701;ext=1002" -PhoneNumberType DirectRouting
       ```

    Microsoft recommends, but doesn't require, that the phone number is configured as a full E.164 phone number with country code. You can configure phone numbers with extensions. These extensions are used to look up users when the lookup against the base number returns more than one result. This functionality allows companies to configure phone numbers with the same base number and unique extensions. For lookup to be successful, the invite must include the full number with extension as follows:
    
    ```PowerShell
    Invite: <sip:+14255388701;ext=1001@sbc1.adatum.biz
    ```

## Configure sending calls directly to voicemail

Direct Routing allows you to end the call to a user and send it directly to a user's voicemail. If you want to send a call directly to voicemail, attach `opaque=app:voicemail` to the Request URI header (for example, `sip:user@yourdomain.com;opaque=app:voicemail`). The Teams user doesn't receive the calling notification. Instead, the call directly connects to the voicemail of the user.

## Assign Teams Only mode to users to ensure calls land in Microsoft Teams

Direct Routing requires that users be in Teams Only mode to ensure incoming calls land in the Teams client. To put users in Teams Only mode, assign them the "UpgradeToTeams" instance of TeamsUpgradePolicy. For more information, see [Upgrade strategies for IT administrators](upgrade-to-teams-on-prem-implement.md). If your organization uses Skype for Business Server, see the following article for information about interoperability between Skype and Teams: [Migration and interoperability with Skype for Business](migration-interop-guidance-for-teams-with-skype.md).

## Related articles

[Plan Direct Routing](direct-routing-plan.md)

[Configure Direct Routing](direct-routing-configure.md)
