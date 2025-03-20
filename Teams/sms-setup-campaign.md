---
title: Set up a Campaign for SMS in Microsoft Teams
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: nijait, julienp
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
description: Learn how to set up a Campaign to enable SMS in Microsoft Teams.
---

# Create a Campaign for SMS in Microsoft Teams

> [!NOTE]
> Due to a high volume of requests for SMS in Teams, processing times to approve Campaigns and Brands for SMS in Teams may take longer than usual. We appreciate your patience as we work diligently to address all requests. Thank you for your understanding.

This article is for IT administrators and IT professionals who are enabling Short Message Service (SMS) in Teams and need to register their company's Campaign with The Campaign Registry (TCR).

Before reading this article, make sure you've read [Plan for SMS in Teams](sms-overview.md) and [Step 1: Create a brand](sms-setup-brand.md).

SMS in Teams is only available in the United States (including Puerto Rico) and Canada.

> [!NOTE]
> Customers in the United States and Canada must have an approved Brand and Campaign before enabling SMS for Teams Calling Plan numbers.

## Prerequisites

Ensure fundamental understanding of the *purpose* for a Campaign, as described in [Learn about SMS Texting in Teams](sms-overview.md).

Administrators must have one of the following role-based access control (RBAC) roles assigned:

- Teams Administrator
- Teams Communications Administrator
- Teams Telephony Administrator

## Campaign registration details for SMS in Teams

After your brand is registered with TCR and the Teams admin center shows that your brand's status is **Approved**, proceed with the campaign registration.

The 10DLC (10-digit long code) registration process involves validating your **Campaign**, or organization's objective, for accessing the 10DLC network. To get your campaign approved, you must submit details to TCR via the Teams admin center.

Examples of details that TCR may require, based on [your Brand](sms-setup-brand.md):

- **Campaign details**
  - *Brand*: The brand associated with this campaign.
  - *Description*: A description for the campaign, explaining its purpose and target audience.
  - *Call-to-Action/Message Flow*: A description of how end users are expected to engage with this campaign (such as opt-in process, expected interactions).

- **Campaign use cases**
  - *Content Type*: The type of content you intend to send (such as Marketing or Customer Care).
  - *Sub-content Type*: A more specific content category if applicable.
  - *Sample Message*: A sample message that aligns with the campaign's use case. Multiple sample messages are acceptable.

- **Campaign and content attributes**
  - *Subscriber Opt-in*: Indication if subscriber opt-in is required.
  - *Subscriber Opt-in Message*: If opt-in is required, the message for subscribers to receive when opting into the campaign.
  - *Subscriber Opt-out*: Indication if subscribers can opt out.
  - *Subscriber Opt-out Answer*: If opt-out is required, the message for subscribers to receive when opting out.
  - *Subscriber Help*: Indication if subscriber help is available.
  - *Subscriber Help Answer*: If help is available, the message for subscribers seeking assistance, including a website, phone number, and email.
  - *Privacy Policy*: A link to your privacy policy, concerning data exchanged via SMS with your company.
  - *Terms and Conditions*: A link to your terms and conditions, concerning correspondence via SMS with your company.

- **Additional attributes**
  - *Direct Lending or Loan Arrangement*: Indicates if the campaign involves any lending or loan arrangements.
  - *Embedded Link*: Specifies if the campaign includes an embedded link.
  - *Embedded Phone Number*: Specifies if a phone number is embedded within the campaign content.
  - *Age-gated Content*: Indicates if the content is age-restricted.

## Create an SMS in Teams Campaign in Teams admin center

The Teams Admin Center allows you to provide the minimum details about your company's Campaign.

To initiate Campaign approval application, do the following steps:

1. In the Teams admin center, navigate to **Voice** > **Service configuration** > **SMS** > **Step 2: Create campaign**.
1. Select **Create Campaign / Update Campaign / View details** to open a right-side configuration slide-out and populate the fields with your company's campaign information. Your Brand must be approved before you can apply for Campaign approval.

Populate your campaign application to TCR according to the following steps associated with the Campaign field sections:

- [Step 1: Campaign details](#step-1-check-campaign-details)
- [Step 2: Accept Terms and Conditions](#step-2-accept-terms-and-conditions)
- [Step 3: Submit your Campaign and view Campaign status](#step-3-submit-your-campaign-and-view-status)

### Step 1: Check Campaign details

In the campaign form, provide details of your company's plan for SMS operations, if any.

|Category |Description |
|:-----|:-----|
|Direct lending or loan arrangements related |Indicates whether the campaign includes content related to direct lending or other loan arrangements. |
|Embedded Link |Indicates whether the campaign is using an embedded link of any kind. Public URL shorteners (bitly, tinyurl) aren't accepted. |
|Embedded phone number |Indicates whether the campaign is using an embedded phone number (except the required HELP information contact phone number). |
|Age-gated content |Indicates whether the campaign includes any age-gated content as defined by Carrier and CTIA guidelines.|

### Step 2: Accept Terms and Conditions

Select the box to accept the terms and conditions.

The terms as follows relate to Microsoft sharing your brand information with an operator, in this case, The Campaign Registry.

>Teams SMS services involve an integration between Microsoft and the underlying carrier, aggregator, or operator ("Operator"). Microsoft must share application details and/or brand information with the Operator to ensure that the program meets regulatory guidelines and standards set by operators. The Operator is the final reviewer and approver of your service application. If the details you provide on your application change, it's your responsibility to resubmit your application with up-to-date information. By submitting an application, you agree that Microsoft may share the application details as necessary for provisioning the Teams messaging service.

### Step 3: Submit your Campaign and view status

After reviewing your Campaign's details and accepting Microsoft's terms and conditions, select **Submit**.

After submission, the Campaign status shows as **Submitted** and the campaign information can't be modified without Microsoft Support intervention.

> [!NOTE]
> If TCR *rejects* your campaign submission, a Microsoft case is automatically opened on your behalf with Microsoft's Telephone Number Services (TNS) - Service Desk. You can view your case by navigating to the [Phone Number Service Center](https://pstnsd.powerappsportals.com), and then selecting the tab for **My Company Cases**. Open the case, and you can interact with the Telephone Number Services - Service Desk team about the details and status of the case.

Once TCR approves your Campaign, you can move on to [Step 3: Enable SMS](sms-management.md).

## Considerations

Because the Campaign application approval can be tedious, Microsoft is working to minimize the level of effort to get your Campaign approved. The following topics relate to considerations when preparing your SMS operation.

### Opt-out messaging

In the initial Campaign application to TCR, Microsoft provides a generic campaign opt-in, opt-out, and help message. The following default messages are provided to TCR (and first time recipients of Teams SMS messages):

|Message action |Default message |
|:-----|:-----|
|First message (and START if recipient previously messaged STOP) |This message is sent from an employee of *Contoso* (your brand). Message frequency varies. For more info on Microsoft or SMS service, reply HELP. To stop receiving messages from this number, reply STOP. Standard message and data rates may apply. |
|STOP |You have opted out of this conversational SMS service and will not receive further messages from this *Contoso* (your brand) number. Reply START to resume. Message and data rates may apply. |
|HELP |For more info on SMS service for *Contoso* (your brand), contact (*your Brand support contact inserted here*). To stop receiving messages from this number, reply STOP. Message and data rates may apply. |

If a recipient responds with "STOP," all following messages from the Teams user's number are blocked to that recipient. The STOP command applies to the phone number only. Other Teams users in your tenant can still send messages to the recipient.

A recipient doesn't need to respond to the first message with START to enable SMS message flow. The first message from a Teams user to a recipient includes the opt-out message, but explicit consent isn't required on the 10DLC network to continue conversational SMS messaging.

### Building a campaign with more than 49 SMS-enabled numbers

If you require more than 49 SMS-enabled numbers, you must work with [Microsoft's Telephone Number Services - Service Desk](contact-tns-service-desk.md) so that they can work with you on an exception to the default maximum campaign quantity. Provide the TNS Service Desk with the number of SMS-enabled numbers and the expected volume of messages sent and received per month, so that they can support the required provisioning.

### Campaign approval process timeline

The Service Level Agreement for campaign approval or rejection is seven days maximum.

If you submit incorrect campaign information, if you don't receive an approval or rejection notice in seven days, or if you have questions related to the process, [contact Microsoft's Telephone Number Services (TNS) - Service Desk](contact-tns-service-desk.md).

TCR might require additional information from your company before approving your campaign. Some potential information that may be required before approval includes:

- Further description details about your campaign's purpose
- Your company's privacy statement related to SMS messaging
- Your company's terms and conditions related to SMS messaging
- More resources for recipients who respond with HELP

If your company doesn't have a privacy statement or terms and conditions related to SMS messaging, you can use a Microsoft-provided template, completed with your company's information. For the template, see [SMS privacy statement and terms and conditions template](sms-privacy-terms-template.md).

## Related topics

- [Microsoft Calling Plan Overview](calling-plan-overview.md)

- [Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

- [Learn about SMS texting in Teams](sms-overview.md)

- [SMS privacy statement and terms and conditions template](sms-privacy-terms-template.md)

- [Step 3: Enable SMS](sms-management.md)

- [Plan for SMS in Microsoft Teams](sms-overview.md)

- [Microsoft's SMS in Teams messaging policy](sms-microsoft-teams-policy.md)
