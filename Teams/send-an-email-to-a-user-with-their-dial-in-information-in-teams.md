---
title: Email a user their Audio Conferencing information
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.reviewer: oscarr
ms.date: 02/18/2025
ms.topic: how-to
ms.assetid: 7440d3e2-1b49-4258-bd2c-79e9072f8c8d
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.subservice: teams-audio-conferencing
ms.collection: 
  - M365-collaboration
  - m365initiative-meetings
  - Tier1
audience: Admin
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
f1.keywords:
- CSH
ms.custom: 
  - Audio Conferencing
  - seo-marvel-apr2020
description: Learn about how to send your users an email with their Audio Conferencing information in Microsoft Teams.
---

# Send an email to a user with their Audio Conferencing information in Microsoft Teams

Sometimes, Microsoft Teams users need you to send them their Audio Conferencing information. As an admin, you can do this by selecting **Send conference info via email** under the properties for a user. When you send this email, it contains all of the Audio Conferencing information, including the conference phone or dial in phone number for the user.

Here's an example of the email that is sent:

![Example of a dial-in conferencing email message.](media/teams-send-email-to-user-with-audio-conferencing-image1.png)

> [!NOTE]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]
  
## Send an email with Audio Conferencing information to a user

### Sending an email using the Microsoft Teams admin center

1. In the navigation pane, expand **Users** > **Manage users**, and then select the user from the list of available users.
2. In the **Audio Conferencing** section, select **Edit**.
3. Select **Send conference info in email**.

:::image type="content" source="media/new-ac-user-small.png" alt-text="Screenshot of Audio Conferencing settings for a user in the Microsoft Teams Admin Center." lightbox="media/new-ac-user-expand.png":::

## Audio Conferencing email notifications

There are several emails that are sent to users in your organization after they're enabled for Audio Conferencing:

- When an **Audio Conferencing** license is assigned to them.
- When you manually reset the user's Audio Conferencing PIN.
- When an **Audio Conferencing** license is removed from them.
- When the Audio Conferencing provider for a user is changed from Microsoft to another provider or **None**.
- When the Audio Conferencing provider for a user is changed to Microsoft.

To learn how to manage these email notifications, see [Emails sent to users when their settings change in Microsoft Teams](emails-sent-to-users-when-their-settings-change-in-teams.md).
  
## Related topics

- [Try or purchase Audio Conferencing in Microsoft 365 for Microsoft Teams](try-or-purchase-audio-conferencing-in-office-365-for-teams.md)
