---
title: Planning for SMS in Microsoft Teams
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
description: Plan for SMS in Teams for the United States, Puerto Rico, and Canada
---

# Plan for SMS in Teams with Microsoft Calling Plan numbers

> [!NOTE]
> SMS for Teams Calling Plans in the United States (including Puerto Rico) and Canada is currently being rolled out for general availability.
>
> Due to a high volume of requests for SMS in Teams, processing times to approve Campaigns and Brands for SMS in Teams may take longer than usual. We appreciate your patience as we work diligently to address all requests. Thank you for your understanding.

This article is for IT administrators and IT professionals planning to enable Short Message Service (SMS) for their tenant in Microsoft's Teams admin center.

## Overview

Microsoft Teams Calling Plans support sending and receiving SMS messages within Teams Chat, for users in United States (including Puerto Rico) and Canada.

Users in US and CA can send SMS messages to numbers that can receive SMS messages and that are regionally assigned to recipients in the US or CA.

Teams users sending or receiving SMS messages outside of the US or Canada aren't supported.

All SMS messaging to and from Teams is considered:

- Business messaging
- Non-consumer messaging
- Application-to-Person (A2P) messaging

These references are used interchangeably. Most notably, SMS in Teams is *not* categorized as *consumer* SMS messaging.

In the US, the PSTN (Public Switched Telephone Network) industry requires that operators direct A2P messaging to their recipients through a specialized network, known as the 10DLC (10 Digit Long Code) network. The purpose of the specialized network is to control A2P access to subscribers and reduce the chance of your A2P messages being flagged as spam.

Check the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) for developments.

## Registering to use the 10DLC network

Before an operator can transmit A2P messages into the 10DLC network and to their subscribers, 10DLC operators must approve the following two aspects of the SMS sender's company:

1. Validity of the company
2. The company's intent for accessing this network

The shared, independent, and approving authority, used by 10DLC network operators to validate legitimate SMS messaging, is [The Campaign Registry (TCR)](https://www.campaignregistry.com/about/).  

**Microsoft is required to facilitate a customer's registration with The Campaign Registry before Microsoft Teams Calling Plan numbers can be enabled for SMS.**

Registration with TCR involves the following two parts:

1. **Brand**: The identification and validation of your company
2. **Campaign**: The purpose and context of your SMS operation

> [!NOTE]
> TCR and participating carriers determine trust scores. TCR requires brand vetting in the following cases:
>
> - To achieve higher trust scores for better message throughput and delivery rates.
> - Brand vetting for 10DLC (10-Digit Long Code) messaging is typically required for companies outside the Russell 3000 list.

To receive approval with TCR, Teams administrators use the Teams admin center to pass their company's Brand and Campaign information to TCR. TCR then reviews your Brand and Campaign, which helps ensure SMS messaging integrity, compliance, and accountability with industry standards.

> [!NOTE]
> Microsoft Teams customers in US and CA must receive Brand *and* Campaign approval before any number can be enabled for SMS in Teams. Teams phone numbers can't be enabled for SMS until TCR approves the brand and campaign.

Registration and enabling SMS for Teams Calling Plan numbers can be summarized in the following diagram:

:::image type="content" source="media/sms-tcr-registration-small.png" alt-text="Screenshot that shows overview of the SMS enablement process for Teams Calling Plan numbers." lightbox="media/sms-tcr-registration-large.png":::

The Brand and Campaign approval requirement applies to businesses that do mass texting or marketing, as well as businesses that send individual messages, **even if it isn't for marketing purposes**.

### Brand approval

When you apply for Brand approval, legally identifiable information about your company must be submitted, including the following information:

- Business ID
- Legal address
- Stock Symbol
- Website

More details can be found in [Step 1: Create a brand](sms-setup-brand.md).

### Campaign approval

When you apply for Campaign approval, resources about your company's campaign operation must be submitted, including the following information:

- SMS use cases
- Message flow actions (describing opt-in and opt-out words)
- A2P SMS privacy statement
- A2P SMS Terms and conditions

More details can be found in [Step 2: Create campaign](sms-setup-campaign.md).

## Licensing

In addition to registering the company Brand and Campaign for access to the 10DLC network, your users must be assigned the following licenses:

- Teams
- Teams Phone
- Microsoft Teams Calling Plan

Inbound and outbound SMS messaging support is included in Microsoft Teams Calling Plans, for supported countries/regions.

### Voice enablement

In addition to licensing, your users must have a Teams Calling Plan phone number assigned and be "voice enabled."

To acquire and assign Teams Calling Plan phone numbers, see [Calling Plans for Office 365](calling-plans-for-office-365.md).

To voice enable your users, you can use the Teams admin center or PowerShell.

- In the Teams admin center, go to **Users** > **Manage users** and select the user you want to edit. Under the **Account** tab > **Assigned phone number**, turn **Enterprise Voice** to **On** and select **Save**.
- For PowerShell, use the [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) cmdlet and set the `-EnterpriseVoiceEnabled` parameter to `$true`.

### SMS message segments and thresholds

The maximum size of a single SMS message determines the accounting for SMS messages. The size of a single SMS message segment is 140 bytes or 160 GSM 7-bit-encoded, standard text characters.

When a sent SMS message exceeds the character limit, the message splits into multiple segments. These segments are sent individually and reassembled by the recipient's device to form the complete message. Each message segment accounts for one Teams SMS message.

For example, if a Teams user sends a message that is 240 characters, requiring two message segments, the usage indicates a cost equivalent to two SMS messages in your billing.

The number of SMS message segments per Calling Plan license depends on the assigned Microsoft Calling Plan and can be determined in the following table:

|Teams Calling Plan | Supports SMS capability |Included SMS (threshold before paying overage) |
|:-----|:-----|:-----|
|Pay-as-you-go |Yes |0 |
|Domestic 120 |Yes |100 |
|Domestic |Yes |200 |
|Domestic + International |Yes | 200 |
|Teams Phone + Calling Plan Bundle |Yes |Phone + Domestic = 200 (if purchased as Calling Plan bundle) / Phone + Pay-as-you-go = 0 (if purchased as pay-as-you-go bundle) |

The number of allotted messages in a Calling Plan accounts for a total of inbound messages received plus outbound messages sent.

As with calling minutes, the number of SMS messages allocated per licensed user are pooled at the tenant level. Overage charges don't apply until the resources pooled across all users' plans in the tenant are consumed within the billing period.

## Usage and billing

For Domestic Calling Plan licenses, allotted SMS messages are pooled for all SMS-enabled users in the tenant, and there's support for overages.

For Pay-As-You-Go Calling Plan licenses, SMS messages are billed per use.

SMS usage in all Calling Plans accounts for sent and received messages.

All users within the same tenant in the US, PR, and CA with the same Calling Plan share a common pool of SMS messages. For example, if 100 users in the United States, Puerto Rico, or Canada have a Domestic Calling Plan, each user is allocated 200 SMS, creating a shared pool of 20,000 SMS messages. Any inbound or outbound messages exceeding this pool are billed per-message.

Pooling applies only to identical Calling Plans.

### Rate limiting

To ensure 10DLC's high quality of service consistent with provided SLAs, operators enforce rate limits for the number of messages that can be sent from a TCR-registered entity. There are a wide range of rate limits, depending on several factors, including:

- The tier of your Brand
- The 10DLC operator that is sending the SMS on your user's behalf
- The use case of the Campaign

The operator that provides the *recipient's* SMS service is the operator that enforces the rate limit. Varying differences in rate limits can be observed in the following table:

|Operator |UCaaS Low Volume |UCaaS High Volume |
|:-----|:-----|:-----|
|AT&T – Max SMS per minute, per campaign |Fixed: 75 |Depends on the brand score: <br>240 (class F), <br>2,400 (class D), <br>4,500 (class B) |
|T-Mobile – Max SMS per day, per brand |Fixed: 2,000 |Depends on the brand score: <br>10,000 (Low Mid), <br>40,000 (High Mid), <br>100,000 (Top)|

> [!NOTE]
> If an operator's rate limit cap regularly blocks your users, and their high volume of SMS messaging is warranted, you can apply for a rate limit increase by contacting [Microsoft's Telephone Number Services (TNS) - Service Desk](contact-tns-service-desk.md).

### SMS usage fees

The price of an SMS message is accrued per-message segment. The per-message segment charge is based on the country/region of the message, as shown in the following table:

|Country/Region |Send Message |Receive Message |
|:-----|:-----|:-----|
|United States and Puerto Rico |$0.0075 USD |$0.0075 USD |
|Canada |$0.1028 CAD |$0.01028 CAD |

### Carrier fees

US, PR, and CA 10DLC operators apply a surcharge for processing SMS messages sent to and/or received by users on their network.

- **For outbound messages**, the carrier of the *recipient's number* determines the surcharge.
- **For inbound messages**, the carrier of the *sender's number* determines the surcharge.

For per-message segment pricing related to SMS usage, including currency conversions, see [SMS Pricing](https://go.microsoft.com/fwlink/?linkid=2303326).

This processing surcharge is a per-message-segment fee that may vary over time. If the surcharge rates are expected to change, the SMS pricing table is updated 30 days before the implementation of any price changes.

Carrier fees are included in the Calling Plan allotted messages. For overages, carrier fees are added to usage fees, per message.

### Billing and reporting

Detailed SMS usage on a per-message basis can be analyzed in the Teams admin center, under **Analytics & reports**. For more information about SMS reporting, see [Step 3: Enable SMS](sms-management.md).

Costs incurred for usage-to-date can be monitored and managed depending on the type of billing account that is used for invoicing. An example of billing account types and respective cost management methods can be reviewed in the following table:

|Billing account type |Cost management method |
|:-----|:-----|
|Microsoft Online Subscription Agreements, Enterprise Agreements, Legacy Direct, and Legacy Cloud Solution Partner (CSP) |Prepaid Communication Credits in the Microsoft 365 admin center |
|Microsoft Customer Agreement via Direct or Enterprise |Postpaid Cost Management in the Microsoft 365 admin center |
|Microsoft Customer Agreement via Cloud Solution Partner |Postpaid usage charges managed with partner |

For funding and analyzing costs related to prepaid or postpaid models, see [Microsoft Calling Plan overview](calling-plan-overview.md) and [Communication Credits](what-are-communications-credits.md).

## Considerations and limitations

One brand and one campaign are allowed per tenant.

By default, a campaign supports enabling up to 49 Microsoft Calling Plan numbers to be SMS-enabled. If more than 49 numbers need to be enabled for SMS, refer to note in [Step 2: Create campaign](sms-setup-campaign.md).

After you [enable a phone number for SMS in Teams](sms-management.md) and assign the number to a user, the user can begin sending and receiving SMS messages. There's no policy governance to limit the number of messages sent to or received by the user.

Teams Calling Plans support sending SMS where the sender type is a 10 digit long code (1-234-123-1234). Teams Calling Plans don't currently support toll-free numbers (1-8XX), short codes (12345), or alphanumeric sender ID (CONTOSO).

Further prerequisites and next steps can be found in the following article: [Step 1: Create a brand](sms-setup-brand.md)

SMS messages in Teams are supported with one-on-one Chat conversations. MMS, attachments, emojis, stickers, and GIFs aren't currently supported.

For end user documentation, see [Send and receive SMS in Microsoft Teams](https://support.microsoft.com/office/send-and-receive-sms-in-microsoft-teams-a7d163cb-3562-4f4a-b1c1-81c722c1a0f1).

## Related articles

- [Microsoft Calling Plan Overview](calling-plan-overview.md)

- [Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

- [Step 1: Create a brand](sms-setup-brand.md)

- [Step 2: Create a campaign](sms-setup-campaign.md)

- [Step 3: Enable SMS](sms-management.md)

- [Microsoft SMS in Teams legal messaging policy](sms-microsoft-teams-policy.md)

- [Privacy policy and terms and conditions templates for SMS in Teams](sms-privacy-terms-template.md)
