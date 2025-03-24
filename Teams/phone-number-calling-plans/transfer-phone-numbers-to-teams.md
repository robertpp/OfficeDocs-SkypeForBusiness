---
title: Transfer phone numbers to Microsoft Teams
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: leiaglezer
ms.date: 01/10/2025
ms.topic: how-to
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
f1.keywords:
- NOCSH
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
description: Submitting a port request. Learn how to transfer telephone numbers to Microsoft for Calling Plans in Teams.
ms.custom: seo-marvel-mar2020
---

# Submitting a port request

This article is an accompaniment for IT professionals and Teams Phone administrators in the process of porting phone numbers to Microsoft Calling Plans.

## Prerequisites

1. Review the information in [Planning number ports](port-order-overview.md).
1. Gather related documentation pertaining to porting numbers for your country or region.
    1. Use the drop-down to select the country/region where you're getting numbers. Find information about availability and the downloadable PDF LOA forms required for porting numbers. Other documentation might be necessary.

       > [!div class="op_single_selector"]
       >
       > - [Australia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-australia)
       > - [Austria](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-austria)
       > - [Belgium](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-belgium)
       > - [Canada](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-canada)
       > - [Czech Republic](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-czech-republic)
       > - [Denmark](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-denmark)
       > - [Estonia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-estonia)
       > - [Finland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-finland)
       > - [France](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-france)
       > - [Germany](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-germany)
       > - [Hong Kong](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-hong-kong)   
       > - [Hungary](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-hungary)
       > - [Ireland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-ireland)
       > - [Italy](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-italy)
       > - [Japan](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-japan)
       > - [Latvia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-latvia)
       > - [Lithuania](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-lithuania)
       > - [Luxembourg](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-luxembourg)
       > - [Mexico](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-mexico)
       > - [New Zealand](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-new-zealand)
       > - [Norway](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-norway)
       > - [Poland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-poland)
       > - [Portugal](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-portugal)
       > - [Romania](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-romania)
       > - [Singapore](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-singapore)
       > - [Slovakia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-slovakia)
       > - [Slovenia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-slovenia)
       > - [South Africa](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-south-africa)
       > - [Spain](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-spain)
       > - [Sweden](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-sweden)
       > - [Switzerland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-switzerland)
       > - [Netherlands](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-netherlands)
       > - [United Kingdom](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-u-k)
       > - [United States & Puerto Rico](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-u-s)

1. Access the Teams Admin Center (TAC) with one of the following roles:
    1. Teams Telephony Administrator
    1. Teams Communications Administrator
    1. Teams Administrator

## Create a port order and transfer your phone numbers to Teams

### [**Porting wizard - New (U.S. & Canada)**](#tab/new-porting-wizard)

#### Launch the port wizard

In the Teams admin center's left navigation rail, go to **Voice** > **Phone numbers**. Select **Numbers**, and then select **Port**.

:::image type="content" source="../media/numberportwizarduscanada.png" alt-text="Screenshot that shows Teams admin center number port wizard for USA and Canada.":::

The wizard’s splash screen allows you to select the location for the numbers you wish to port.

- If you're porting U.S. or Canada numbers and would like to use the new porting wizard, then select **US & Canada Preview**.
- If you'd like to submit your port request using the classic porting wizard, then choose **All regions (current porting experience)**.

Select **US & Canada** and select **Start port**.

#### Get started

1. Review the information on the Get started page, and then from the drop-down, select the country/region currently hosting the telephone numbers to be ported.

2. When you specify a country or region, the wizard calls out the documents from the current carrier that you need to complete your port order.

3. Make note of these documents required for later steps.

#### Phone numbers

1. Add your phone numbers manually or by uploading a list.
    - To add phone numbers manually, enter numbers in 10-digit or E.164 format, separated by a comma or semi-colon. Ranges aren't supported. Optional dashes or hyphens are supported.
    - To upload a list of phone numbers, the list must be in CSV format and must have only one column with a header designated as PhoneNumber. Each phone number must be in a separate row and can be in 10-digit or E.164 format.

2. Upon adding phone numbers, the wizard compiles the numbers, categorize them, and then display a table of the numbers in groups by *account*, *service provider*, and *type*.
    - The wizard allows you to select one of the groups for processing. The wizard only processes a port request with one type of group at a time.
    - If the wizard categorized your numbers into more than one group, you must submit a separate port request for each. See [Planning number ports](port-order-overview.md).
    - If the wizard detects that your requested numbers are invalid for porting, the error is shown here.

3. Once your numbers are validated in the wizard, you have the option to save your progress and continue later. If you need to exit and return to your order, follow these steps:
    - Go to **Teams Admin Center**
    - Navigate to **Voice** > **Phone Numbers**
    - Select **Order History**
    - Select the desired order name hyperlink
    - Continue from where you left off.

#### Billing telephone number (BTN)

Enter the Billing telephone number (BTN) for the account with your existing service provider.

- The Billing telephone number (BTN) for the phone numbers being ported must match what the current service provider has on file for the account. Also, if there's a freeze on the account it must be removed. If the BTN is incorrect or there's a freeze on the account, your port request will be rejected after it's submitted.
- The BTN can also be referred to as the 'Account telephone number.' It's the primary phone number associated with your account. Your service provider uses the BTN to track activities, payments, and customer service records.
- You can usually find your BTN on an account statement. If you're unsure, ask your current service provider's account representative to help you identify your BTN.
- In a **full** port request, all numbers associated with the BTN are ported to Microsoft, including the BTN, and the respective account with the current provider is closed.
- In a **partial** port request, you have two scenarios:
    - You're porting only the phone numbers previously specified, **not including** the BTN which stays in service with the current provider.
    - You're porting only the phone numbers previously specified, **including** the BTN. If you choose this partial port option, you can designate one of the numbers that isn't being ported to become the replacement BTN for the account that is still open with your current service provider. Designating a replacement BTN is optional.

#### Account information

As with the BTN, it's essential to document the account information exactly the way the current service provider has it in their records.

> [!NOTE]
> You can save your work as you work through this page and the wizard.

- The organization name should match, exactly as represented in the current service provider's records.
- If the wizard identifies the service provider's name, don't change it here.
- The account  number should be discoverable on an account statement or invoice, or in your provider's online account portal.
- The account might have an account PIN and if so, it must be provided here. The account PIN isn't the same as a BTN Freeze PIN. A BTN Freeze PIN allows an authorized user to unfreeze an account for maintenance, such as porting activities. The account PIN is used for security, to prevent unauthorized access to account management and records. The *account* PIN is required in this step for all mobile numbers being ported.
- The authorized user is one or more persons associated with the account and is authorized for account management and records. Only one authorized user needs to be designated on your port request. If you're unsure of the account's authorized user, contact your service provider's account manager.
  - Updating the authorized user during the port request isn't supported. If you wish to change the authorized user, you can do so with the current service provider before the port. Once your port request is complete, Microsoft considers your tenant admins as authorized users.
- The service address is specific to the phone numbers that you're porting, and it represents the associated, physical, service address where the number is operational.
  - If the location isn't defined in your tenant, then select **Add a location**.

#### Documents

Upload the required and recommended articles from your service provider.

- Files should be in .pdf format.
- Files are stored within your tenant and shared with Microsoft's Telephone Number Service Center.

#### Porting details

Indicate the specifics for your Microsoft service.

- The order name becomes viewable by you in the Teams Admin Center during the porting process and after order completion for your records.
- For the port details, remember to review [Planning number ports](port-order-overview.md).
- The Requester details are necessary so that Microsoft's Telephone Number Service Center has contact information for port request updates.
- If adding multiple email addresses for more contacts, separate with a semi-colon.

#### Authorize and submit

You have two options for submitting.

1. Sign with e-signature (recommended)
    1. In this case, an email is sent to the current *authorized user* that you specified in **Account information** page, and they're prompted to authorize with Microsoft's e-signature tool.
    1. Once the authorized user approves, the request is automatically submitted to Microsoft.
1. Offline signature.
    1. In this case, you download the Letter of Authorization, get it signed, upload it, and submit to Microsoft.

In **Edit Mode**, you can modify any field of your validated order, except for the Country or Region that was selected on the Get Started page. If your updates impact the LOA (Letter of Authorization) and the LOA has already been signed and uploaded, we must refresh the LOA with your modifications. Download, sign, and reupload the updated LOA. Only after re-uploading the refreshed LOA will you be able to submit edits to your order.

#### Confirmation

Confirmation of the request is acknowledged within 72 business hours.

You can check the status of your order in the Teams Admin Center. In left side rail under Voice > Phone Numbers navigate to **Order History** and search by the name you gave your order in the porting details page.

You can research more about the process, here: [Porting status](port-order-status.md).

### [**Porting wizard - All regions**](#tab/classic-porting-wizard)

#### Launch the port wizard

In the Teams admin center's left navigation rail, go to **Voice** > **Phone numbers**. Select **Numbers**, and then select **Port**.

:::image type="content" source="../media/numberportwizardallregions.png" alt-text="Screenshot that shows Teams admin center number port wizard for all regions.":::

The wizard’s splash screen allows you to select the location for the numbers you wish to port.

- If you're porting U.S. or Canada numbers and would like to use the new porting wizard, then select **US & Canada Preview**.
- If you'd like to submit your port request using the classic porting wizard, then choose **All regions (current porting experience)**.
- Enhancements are in development to offer the new wizard to all other regions where Microsoft offers Calling Plans.

Select **All regions** and select **Start port**.

#### Get started

On the **Get started** page, populate the fields as per your request.

- **Country or region**: Specify the country or region where you're porting numbers.
- **List your phone number**: Add your phone numbers manually or by uploading a list.

  - **To add phone numbers manually**: Enter numbers in E.164 format, separated by a comma or semicolon. Ranges aren't supported. Optional dashes or hyphens are allowed.
  - **To upload a list of phone numbers**: Use a CSV file with one column labeled **PhoneNumber**. Each row should contain a single phone number in E.164 format.

#### Manage numbers

The **Manage numbers** page checks that the number format is correct, matches the specified country or region, and is valid before proceeding.

If the number validation summary isn't successful, view the details to understand the reason.

- Select **View details** in the number validation summary pane or select the phone number validation failure below **Validation status** to check the reasons for phone number failure.

- If the failure isn't understood, you can create a case with the TNS-Service Desk team through the [Phone Number Service Center portal](https://pstnsd.powerappsportals.com/create-ticket/).
  - For the scenario where you don't understand the number validation result, select **Case Type = General Inquiry** and in the description, provide the number validation summary that you see in TAC along with the list of phone numbers that you're trying to port.

The number validation summary must indicate all numbers are valid before you can proceed. If there are no errors, continue.

#### Add account information

On the **Add account information** page, complete the following, and then select **Next**.

> [!NOTE]
> The information displayed on this page is presented according to the country or region and number type. Each country and region has different regulations on the information required to port numbers. What you see on this page might be different from what's described here.

1. **Order details**: Input required name for your port request. The order name you specify here becomes viewable by you in the Teams Admin Center during the porting process and after order completion for your records.

2. **Port details**: Enter the Billing Telephone Number (BTN) in E.164 format.

    - If you enter a BTN number that isn't in the list of numbers that you're porting, your request is automatically categorized as a **Partial port** and the BTN will remain with your current service provider after the port is complete.
    - If you enter a BTN number that matches a number in the list of numbers that you're porting, you have two options.

        - **Option 1**: Port **all numbers in my account**. If you choose this option, the account with your current service provider will be closed after the port is complete.
        - **Option 2**: Port **some numbers in my account, and I'm including my account's BTN**. If you choose this partial port option, you can designate one of the numbers that isn't being ported to become the replacement BTN for the account that is still open with your current service provider. Designating a replacement BTN is optional.

> [!NOTE]
> All information input for your organization and current service provider must match *exactly* with the current service provider's records.
>
> Some fields are optional, but some service providers require the optional fields.

3. **Organization details**: Enter your organization's name.

4. **Current service provider details**: Provide the current service provider's name, account number, and security PIN. The account PIN is required to port mobile numbers.

5. **Requester details**: Populate this information with the contact details of the person who Microsoft can contact with port order status updates.

6. **Authorized user details**: Populate this information with the contact details of the person who is the authorized user with your current service provider.

7. **How do you want to sign the Letter of Authorization?**: Select whether you want e-signature or manual upload for the Letter of Authorization.

8. **Service address**: Enter the service address exactly as it matches the current service provider's record. Emergency addresses can be assigned later, when assigning the number to a user.

9. **Default number usage**: Select the intended type of usage for the numbers. If you would like to change it, select *Yes, change usages* to go to the **Add number features** page. If you select *No*, the wizard skips you to the **Complete your order** page.

#### Add number features

The add number features page is where you update the number usage. Usage is a category of service for the phone numbers.

- For numbers assigned to users, the default number type is geographic phone numbers and is listed as **User**.

- For numbers assigned to voice applications, such as Auto-Attendants and Call Queues, the number usage type should be set as **Voice app**.

- For numbers assigned to audio conferencing, the number usage type should be set to **Conference**.

Toll-free numbers default to **Voice app**, but you can make changes to the default number usages in this section of the wizard.

To update the number usage, check the desired number and select **Update number usage**. Then, from the right-hand side rail, use the drop-down and select your desired number usage to assign to the numbers.

#### Complete your order

- If you selected **Paper signature** in the **Add account information** page, you can download a Letter of Authorization template.

  - The template is prepopulated with the information you input in the wizard.
  - Once signed, you upload a copy of the signed Letter of Authorization and then you can select **Submit** and the port request proceeds.

- If you selected **E-signature** in the **Add account information** page, the authorized user receives an email to sign the Letter of Authorization once you select **Complete and send e-signature request**.

  - Once they electronically sign, the port request proceeds.

---

## What happens next

When we receive your port order, you receive an email that verifies your request. Your request is updated daily, and you're notified of its progress and status in email. If your current carrier rejects the port request, contact the [Phone Number Service Center](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md) for assistance.

> [!NOTE]
> If you already have a case open with the TNS-Service Desk for your port request, update that existing ticket instead of creating a new case.

For more information about Letters of Authorization to port existing phone numbers and other considerations, see [Manage phone numbers for Calling Plan](../manage-phone-numbers-for-your-organization.md) and [Planning number ports](port-order-overview.md).

## Report phone number issues

If you notice any issues with the ported numbers within the first 24-48 hours after the port is completed, contact the [Phone Number Service Center](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md). For any issues beyond 48 hours, contact the Microsoft Support Team.

## Related articles

- [Planning number ports](port-order-overview.md)
- [Different kinds of phone numbers used for Calling Plans](../different-kinds-of-phone-numbers-used-for-calling-plans.md)
- [Manage phone numbers for your organization](../manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md)
- [Emergency calling terms and conditions](../emergency-calling-terms-and-conditions.md)
- [Emergency Calling disclaimer label](https://download.microsoft.com/download/9/9/0/990e24c1-eb49-4b52-9306-dbd4c864ed91/emergency-calling-label-(en-us)-(v.1.0).zip)
