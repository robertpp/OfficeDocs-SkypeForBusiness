---
title: "See a list of telephone numbers in your organization"
ms.author: scottfrancis
author: sfrancis206
manager: pamgreen
ms.reviewer: davlick, roykuntz, jastark, pavellatif
ms.date: 01/21/2025
ms.topic: article
ms.assetid: 93098bc5-df63-4a1f-8734-0b72a6280a69
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - M365-collaboration
  - Tier1
audience: Admin
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom: 
  - Calling Plans
  - seo-marvel-mar2020
description: Learn how to see a list of all telephone numbers in your organization and all numbers that are assigned to users or unassigned.
---

# See a list of telephone numbers in your organization

This article is for Teams admins who are managing telephone numbers for their organization's tenant.

In Teams, the numbers that you associate with your tenant are stored in Microsoft's telephone number management inventory, reserved only for your tenant's use. You can see these numbers at any time.

You can see telephone numbers acquired through any of the Public Switched Telephone Network [(PSTN) connectivity options](pstn-connectivity.md) that connected to your tenant. The numbers you can see include numbers assigned to users and unassigned numbers that are reserved for use in your tenant.

To have your unassigned Direct Routing telephone numbers included in this view, you must upload them to Microsoft's telephone number management inventory. For more information, see [Upload Direct Routing numbers to your tenant](direct-routing-enable-users.md#upload-direct-routing-numbers-to-your-tenant).

To see the telephone numbers in your organization:

1. Go to the **Microsoft Teams admin center**.

2. In the left navigation, go to **Voice** > **Phone numbers**.

   - For you to see the **Voice** option in the left navigation in the Microsoft Teams admin center, you must first buy at least one **Enterprise E5 license**, one **Teams Phone** add-on license, or one **Audio Conferencing** add-on license.

3. To view the assignment status of a number, see the **Assignment Status** column, which also shows what type of service the number is assigned to. You can click the filter icon to filter by:

   - **Assigned to user**
   - **Assigned to conference bridge** 
   - **Assigned to Voice app (Auto Attendant/Call Queue)**
   - **Unassigned**

4. On the **Filter** pane, you can use the drop-down list to filter your view by:

   - **Number range** that you set. You can search by lowest number or highest number.
   - Numbers that start with a number that you specify.
   - Number **activation state**.
   - Number **type**.
   - Phone number **status**.

## To see the activation status for number assignments

After assigning numbers to users, you might want to see the activation status of the number assignments:
  
1. Go to the **Microsoft Teams admin center**.

2. In the left navigation, go to **Voice** > **Phone numbers**.

3. Click the filter icon to filter your view by **Activation state**. You can filter by:

   - **Activated**
   - **Assignment pending**
   - **Assignment failed**
   - **Update pending**
   - **Update failed**

## Using the Teams PowerShell module

You can also use the Teams PowerShell module version 1.1.6 or later to see the phone numbers in your organization. For more information about PowerShell, see [Microsoft Teams PowerShell Overview](teams-powershell-overview.md).

To see a list of all telephone numbers that you have for your organization, use the [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment) cmdlet. For example, to see each telephone number, its type, and its state, run the following command:

```PowerShell
Get-CsPhoneNumberAssignment | ft TelephoneNumber,ActivationState,NumberType
```

By default, the [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment) cmdlet returns the first 500 results. Use the "-skip" and "-top" parameters to customize your output.

Another way to get a list of all telephone numbers in your organization is to use the [Export-CsAcquiredPhoneNumber](/powershell/module/teams/export-csacquiredphonenumber) PowerShell cmdlet.

To see all of the telephone numbers that are assigned to users, use the [Get-CsOnlineUser](/powershell/module/teams/get-csonlineuser) cmdlet. For example, to see all users with a telephone number assigned, run the following command:

```PowerShell
Get-CsOnlineUser | Where-Object  { $_.LineURI -notlike $null } | ft DisplayName,UserPrincipalName,LineURI
```

## Related topics

[Manage telephone numbers for your organization](manage-phone-numbers-landing-page.md)

[Emergency calling terms and conditions](./emergency-calling-terms-and-conditions.md)

[Emergency Calling disclaimer label](https://download.microsoft.com/download/9/9/0/990e24c1-eb49-4b52-9306-dbd4c864ed91/emergency-calling-label-(en-us)-(v.1.0).zip)

[Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment)
  
[Get-CsOnlineUser](/powershell/module/teams/get-csonlineuser)
