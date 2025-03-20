---
title: Enable and manage SMS in Microsoft Teams
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
description: Enable and manage SMS in Microsoft Teams
---

# Enable and manage SMS in Microsoft Teams

This article is for IT administrators and IT professionals who are administering the Short Message Service (SMS) usage in Microsoft Teams. You can manage SMS for Teams through the Teams admin center.

## Prerequisites

### Brand and Campaign

To ensure successful enablement of SMS for a Teams Calling Plan phone number, confirm service enablement is configured, as described in the articles [Step 1: Create brand](sms-setup-brand.md) and [Step 2: Create campaign](sms-setup-campaign.md).

### Licensing

To enable Teams users with SMS capabilities, you must assign the following licenses to your users:

- Teams
- Teams Phone
- Microsoft Teams Calling Plan

For more information, see [SMS Licensing](sms-overview.md#licensing).
  
### Billing mechanism

A tenant **billing mechanism** *should* be in place for SMS consumption overages and *must* be in place for Pay-as-you-go Calling Plans.

Funding for usage overages is supported either with prepaid Communication Credits using a Microsoft Online Subscription Agreement (MOSA) or with postpaid invoicing using a Microsoft Customer Agreement (MCA). For more information, see [SMS overview of usage and billing](sms-overview.md#usage-and-billing).

#### Permissions

As an administrator, you must be assigned one of the following Role-Based Access Control (RBAC) roles:

- Teams Administrator
- Teams Communications Administrator
- Teams Telephony Administrator

For more information about Teams administrator roles, see [Use Microsoft Teams administrator roles to manage Teams](using-admin-roles.md).

## Turn on SMS for a user

To enable SMS in Teams for a user, you must turn on SMS for a user's phone number. 

In Teams admin center, navigate to the left side rail, select **Voice** > **Phone numbers** > **Numbers**, and then find and select the number for the user. In the contextual menu just above the list of phone numbers, select **Enable SMS**.

If the number isn't already assigned to a user, you can assign that number to a user. For more information on number management, see [Manage phone numbers for users](assign-change-or-remove-a-phone-number-for-a-user.md).

## Turn off SMS for a user

To turn off SMS for a user in Teams admin center, navigate to the left side rail, select **Voice** > **Phone numbers** > **Numbers**, and then find and select the number for the user. In the contextual menu just above the list of phone numbers, select **Disable SMS**.

## SMS usage report

To view itemized SMS reporting in Teams admin center, navigate to the left side rail, select **Reports & analytics** > **Usage reports** > **PSTN and SMS Usage**, choose a date range, and select **Run report**.

For more information, see [Microsoft Teams PSTN Usage report](.\teams-analytics-and-reports\pstn-usage-report.md).

## Related topics

- [SMS overview](sms-overview.md)

- [Step 1: Create brand](sms-setup-brand.md)

- [Step 2: Create campaign](sms-setup-campaign.md)
