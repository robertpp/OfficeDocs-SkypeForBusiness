---
title: Create a Brand for SMS in Microsoft Teams
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: nijait
ms.date: 02/24/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.collection:
  - M365-voice
  - m365initiative-voice
  - Tier1
search.appverid: MET150
audience: Admin
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
  - CSH
description: Learn how to set up an SMS Brand to enable SMS in Microsoft Teams.
---

# Create a Brand for SMS in Microsoft Teams

This article is for IT administrators and IT professionals who are enabling Short Message Service (SMS) in Teams. 

Use this accompaniment when creating a brand in Microsoft's Teams admin center to register your company with The Campaign Registry (TCR).

SMS in Teams is only available in the United States, Puerto Rico, and Canada.

## Prerequisites

Ensure fundamental understanding of the *purpose* for a Brand, as described in [Learn about SMS Texting in Teams](sms-overview.md).

Administrators must have one of the following Role-Based Access Control (RBAC) roles assigned:

- Teams Administrator
- Teams Communications Administrator
- Teams Telephony Administrator

## Create a Teams SMS brand in Teams admin center

The 10DLC (10-digit long code) registration process involves verifying your organization's identity with SMS network providers. To get your organization verified, you build an organization profile as your "Brand" in the Teams admin center.

1. In the Teams admin center, go to **Voice** > **Service configuration** > **SMS** > **Step 1: Create brand**.
1. Select **Create brand / Updated brand / View details** to open a right-side configuration slide-out and populate the fields with your company's information.

The form fields change dynamically depending on your company's country/region and status. For example, if your company's headquarters is in the US and is a *publicly traded* company, more fields are required to disclose your company's stock symbol. However, if you have a private company, a stock symbol won't be required.

Populate your Brand application to The Campaign Registry according to the field headers as follows:

### Brand identity

In the first section of the brand form, provide details of your company's specific identity, as denoted in its country/region.

|Form field |Description |
|:-----|:-----|
|Brand display name|Enter how your company's name or *Doing Business As* name should be displayed as the Caller ID in outgoing SMS messages.|
|Business name |Enter your company's official name as it's legally registered in your country or region.|
|Business ID |Enter the Business ID of your company, respective to the country or region of your company's headquarters. For example, US and PR companies (and companies with a US EIN), enter your Tax ID's nine-digit EIN. Canadian companies, enter your nine-digit Business Number (BN), Corporation/Incorporation Number, or Registry ID.|
|Business ID issuing Country |Enter the country/region where your business ID is issued.|
|Business address |Enter the address to match the address where your company is headquartered. If you already defined your headquarters as an address in *Locations*, select **Use existing** and search for the address by the city or by the location description. If the address isn't already added, select **Add new** and enter it here.|
|Website |Enter your company's website or a website URL representing your business. *Providing your company's website is optional but recommended to increase the chances of TCR approval.*|

### Brand information

Within the brand information, provide context about your company's business.

|Form field |Description |
|:-----|:-----|
|Brand legal form |Select the legal structure of your company. For example, *Private company*, *Publicly Traded Company*, or *Non-profit organization*.|
|Brand stock symbol |If your company is a publicly traded company, enter your company's stock symbol.|
|Brand stock exchange |If your company is a publicly traded company, select the exchange where it's listed and traded.|
|Brand segment |From the drop-down, select the industry that best categorizes your company's business.|

### Contact information

If there are issues with the registration of your brand, Microsoft Support will reach out to a point of contact that you designate. Populate your contact information according to the field headers as follows:

|Form field |Description |
|:-----|:-----|
|First name | Enter the first name of the point of contact for this application process. |
|Last name | Enter last name. |
|Phone number | Enter the phone number of the point of contact for inquiries related to this application process. |
|Email address | Enter the email address of the point of contact for inquiries related to this application process. |

> [!IMPORTANT]
> If you designated your organization's legal form as a *Publicly Traded Company*, then The Campaign Registry employs Two Factor Authentication, sending an email from *noreply@auth.campaignregistry.com* to the email address supplied in the Contact information. The contact email address can't be a personal or free email account, and it can't be a distribution list, such as sales or support.

### Terms and Conditions

Once the fields are accurately filled out, select the box to accept Microsoft's terms and conditions.

The terms as follows relate to Microsoft sharing your brand information with an operator, in this case, The Campaign Registry.

> Teams SMS services involve an integration between Microsoft and the underlying carrier, aggregator, or operator ("Operator"). Microsoft must share application details and/or brand information with the Operator to ensure that the program meets regulatory guidelines and standards set by operators. The Operator is the final reviewer and approver of your service application. If the details you provide on your application change, it's your responsibility to resubmit your application with up-to-date information. By submitting an application, you agree that Microsoft may share the application details as necessary for provisioning the Teams messaging service.

### Brand submission and status

After filling out all the applicable Brand information, select **Submit**.

The Brand status should now show as **Submitted** and the Brand information can't be modified without Microsoft Support intervention.

If you designated your organization's legal form as *Publicly Traded Company* and you haven't received a Two Factor Authentication message from **noreply@auth.campaignregistry.com**, check your junk mail and your company's firewall rules.

The Service Level Agreement for Brand approval or rejection is three days maximum.

If you submitted incorrect brand information or if you haven't received an approval or rejection notice in three days, [contact Microsoft's Telephone Number Services - Service Desk](contact-tns-service-desk.md).

> [!Note]
> If the Campaign Registry *rejects* your brand submission, a case is automatically opened on your behalf with Microsoft's Telephone Number Services - Service Desk. You can view your case by navigating to the [Phone Number Service Center](https://pstnsd.powerappsportals.com), and selecting the tab for **My Company Cases**. Open the case, and you can interact with the Telephone Number Services (TNS) - Service Desk team about the details and status of the case.

Once your Brand has been approved by TCR, you can move on to [Step 2: Create a campaign](sms-setup-campaign.md).

## Related topics

- [Microsoft Calling Plan Overview](calling-plan-overview.md)

- [Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

- [Learn about SMS texting in Teams](sms-overview.md)

- [Step 2: Create a campaign](sms-setup-campaign.md)
