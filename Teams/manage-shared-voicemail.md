---
title: "Manage Shared Voicemail"
author: mkbond007
ms.author: mabond
manager: pamgreen
ms.reviewer: vijurtse
ms.date: 03/03/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
  - M365-voice
  - m365initiative-voice
  - Tier1
audience: Admin
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom:
  - Phone System
description: "Learn how to configure and manage Shared Voicemail for Auto Attendants and Call Queues."
---

# Manage Shared Voicemail for Auto Attendants and Call Queues

This article describes how to configure and manage Shared Voicemail for Auto Attendants and Call Queues. Shared Voicemail allows multiple users to access a single voicemail inbox.

For information about personal voicemail, see [Set up Cloud Voicemail](set-up-phone-system-voicemail.md).

## Overview

Shared Voicemail is an additional type of voicemail that complements personal voicemail. Shared voicemail is sent to a group of users, and any member of this group can access the message.

Shared Voicemail connects to Microsoft 365 Groups and can be accessed from the Group's associated group folder in Outlook or through a Microsoft Teams Microsoft 365 group-associated Teams Channel under the Calls section. Shared Voicemail also supports distribution lists and mail-enabled security groups, but we recommend using a Microsoft 365 Group.

Your users can receive Shared Voicemail through the redirection logic from Auto Attendants or Call Queues. For more information about Auto Attendants and Call Queues, see [Plan for Teams Auto attendants and Call queues](plan-auto-attendant-call-queue.md).

## Prerequisites

In order to manage Shared Voicemail, you must configure a Microsoft 365 Group with mailbox support. For Shared Voicemail, you should use a Teams or Outlook type security group.

Private and public group types work for Shared Voicemail. However, if the group is public, anybody in your organization can view group-related information. For more information about public and private groups, see [Make Microsoft 365 Groups public or private](https://support.microsoft.com/office/c0a991b3-9c56-48b8-bf0f-05530f836b1b). For more information about groups, see [Overview of Microsoft 365 Groups for administrators](/microsoft-365/admin/create-groups/office-365-groups)

A **Microsoft 365 group with Outlook type** has mailbox enabled by default, but this group might be missing Teams support. For more information, see [Create a group in Outlook](https://support.microsoft.com/office/04d0c9cf-6864-423c-a380-4fa858f27102).

If your organization plans to view and manage Shared Voicemails within Microsoft Teams chats or other applications, you need to ensure that the relevant Microsoft 365 group has Microsoft Teams support. By design, voicemails that are stored in Teams-supported groups are accessible via Microsoft Teams.

A **Microsoft 365 group with a Microsoft Teams type** has the mailbox hidden by default. To make the mailbox visible, use the [Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup) cmdlet with the `-HiddenFromExchangeClientsEnabled` parameter to make a mailbox visible.

  ```powershell
  Set-UnifiedGroup -Identity <GUID> -HiddenFromExchangeClientsEnabled:$false
  ```

If you select a Microsoft 365 group that isn't supported by Teams, then your organization can only manage voicemails addressed to this group only in Outlook.

For more information about creating a group in Teams, see [Microsoft 365 Groups and Microsoft Teams](/microsoftteams/office-365-groups). For information about creating a group in Outlook, see [Create a group in Outlook](https://support.microsoft.com/office/04d0c9cf-6864-423c-a380-4fa858f27102).

## Configure Shared Voicemail

As an admin, you can configure Shared Voicemail for your Auto Attendants and Call Queues. We recommend using Microsoft 365 groups for Call Queue and Auto Attendant setup to ensure seamless integration with Shared Voicemail.

Only members of the Microsoft 365 group can access the Shared Voicemail. Each Shared Voicemail is associated with one Microsoft 365 Group.

To reduce oversharing information, each specific call queue or auto attendant should have its own Microsoft 365 group for Shared Voicemail. Otherwise, if you configure the call redirection logic so that multiple Call Queues with different agents redirect calls to a common Shared Voicemail group, all these users must be members of the Voicemail-associated Microsoft 365 Group to manage voicemails. This permission model could potentially lead to information oversharing. Therefore, we recommend creating a separate Shared Voicemail group for each specific Call Queue or Call Queue-related security group.

For more information, see [manage-your-call-queue-and-auto-attendant-settings-in-microsoft-teams](https://support.microsoft.com/office/52c741c6-8577-4faf-aa5a-c7853e0ab8f8).

### Auto attendants

For auto attendants, you can set up redirection rules to forward calls to a Shared Voicemail. For example, you might want to configure a rule to forward out-of-office hours calls to Shared Voicemail or to forward calls within a certain category directly to Shared Voicemail.

For auto attendant calls that are sent to Shared Voicemail, you can enable or suppress a system greeting. Custom greetings aren't available yet for auto attendants.

For more information about Auto Attendants, see [Set up a Microsoft Teams Auto attendant](create-a-phone-system-auto-attendant.md).

### Call queues

[Authorized users](create-a-phone-system-call-queue.md?tabs=authorized-users#tabpanel_1_authorized-users) of a Call Queue can set up custom Shared Voicemail greetings for the following features:

- Call overflow
- Call timeout
- No agents

You can also turn off custom greetings for call queues. Avoid including any special characters in the greeting messages of Shared Voicemail.

For more information about creating greetings for call queues, see [manage-voice-applications-policies](manage-voice-applications-policies.md).

For more information about redirecting Call Queues to Shared Voicemail, see [Call queue call exception handling](create-a-phone-system-call-queue.md?tabs=call-exception-handling) and [Additional messaging on Call queue call exception handling](create-a-phone-system-call-queue.md?tabs=call-exception-handling-additional-messaging).

## Location of Shared Voicemails

The location of Shared Voicemails depends on if your Microsoft 365 group type is for Outlook or Teams.

### Microsoft Teams

In Microsoft Teams, Shared Voicemails can be found under the **Calls** section of the Microsoft 365 group's associated Teams channel, whereas personal voicemails are typically found in your personal **Calls** tab.

### Microsoft Outlook

In Outlook, Shared Voicemails are located in the associated Microsoft 365 group's **Inbox** folder. Personal voicemails are typically found in your personal **Inbox** or, in older versions of Outlook, under the **Voice mail** Search Folder.

Voicemails in Outlook are basically regular emails that include specific voicemail data and an audio file attachment. All voicemails are categorized with the type *Voicemail*, which allows you to apply rules to these messages. For example, you can create a rule to move all messages categorized as "Voicemail" to a separate Outlook folder. Outlook's functionality for regular emails also applies to voicemails, such as deleting, marking as read/unread, setting categories, applying flags, and more.

To get an automatic summary of voicemails more accurately using Outlook Copilot, organize voicemails in a separate folder. This way, you can ask Copilot to summarize new messages specifically in this folder.

For more information about organizing emails, setting rules, categories, flags, or reminders in Outlook, see the following articles:

- [Set categories, flags, or reminders](https://support.microsoft.com/office/a894348d-b308-4185-840f-aff63063d076)
- [Organize email by using folders in Outlook](https://support.microsoft.com/office/0616c259-4bc1-4f35-807d-61eb59ac79c1)
- [Set up rules in Outlook](https://support.microsoft.com/office/75ab719a-2ce8-49a7-a214-6d62b67cbd41)

## Related articles

[Set up Cloud Voicemail](set-up-phone-system-voicemail.md)

[Microsoft 365 Groups and Microsoft Teams](/microsoftteams/office-365-groups)

[Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup)

[Create a group in Outlook](https://support.microsoft.com/office/04d0c9cf-6864-423c-a380-4fa858f27102)

[Plan for Teams Auto attendants and Call queues](plan-auto-attendant-call-queue.md)
