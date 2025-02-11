---
title:  Manage the Audio Conferencing settings for a user in Microsoft Teams
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.reviewer: oscarr
ms.date: 1/9/2025
ms.topic: article
ms.assetid: 0f39dc9d-eb60-4c5a-9ae3-e34a01834d9b
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.subservice: teams-audio-conferencing
search.appverid: MET150
ms.collection: 
  - M365-collaboration
  - m365initiative-meetings
  - Tier1
audience: Admin
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords: 
  - CSH
ms.custom: 
  - Audio Conferencing
  - seo-marvel-mar2020
description: An admin can edit the Teams Audio Conferencing settings, including provider, default toll or toll-free number, conference ID, or PIN for a user.
---

# Manage the Audio Conferencing settings for a user in Microsoft Teams

As an admin, you can edit Audio Conferencing settings for each user in your organization. To edit settings for your organization, see [Manage the Audio Conferencing settings for your organization](manage-the-audio-conferencing-settings-for-my-organization-in-teams.md).

## Using the Microsoft Teams admin center

1. Open the Teams admin center.
2. Expand **Users** from the navigation pane and select **Manage users**.
3. Select the name of the user you want to manage.
4. Under the **Audio Conferencing** section in the **Account** tab, edit any of the following settings:

:::image type="content" source="media/new-ac-user-small.png" alt-text="Screenshot of Audio Conferencing settings for a user in the Microsoft Teams Admin Center." lightbox="media/new-ac-user-expand.png":::

| Setting | Description |
|:-----|:-----|
|**Send conference info in email**  |Select this link to instantly send an email to the user with their audio conferencing phone number. This email doesn't include the PIN.For more information, see [Send an email to a user with their Audio Conferencing information](send-an-email-to-a-user-with-their-dial-in-information-in-teams.md).  |
|**PIN** |Select **Reset PIN** if you need to reset the PIN for the user. For more information, see [Reset the Audio Conferencing PIN](reset-the-audio-conferencing-pin-in-teams.md). |
|**Default conferencing toll phone number** (required) |Set the numbers on the audio conferencing bridge and format them as you want them to appear in Teams meeting invitations. To change the default toll number, select **Edit** next to **Audio Conferencing.** In the **Audio Conferencing** pane, choose a number under **Toll number.** You can also set phone numbers by adding them to the **`-Set-CsTeamsAudioConferencingPolicy`** and assigning the policy to your users. Phone numbers added to the policy take precedence over numbers set using the **Default conferencing Toll phone number**. If no phone numbers are added to the **`-Set-CsTeamsAudioConferencingPolicy`**, the phone number set with **Default conferencing Toll phone number** is shown on Microsoft Teams meeting invitations.|
|**Invites from this user can include toll-free number**|This setting can only be changed using the **`-Set-CsTeamsAudioConferencingPolicy`**. |
|**Dial-out permissions**|To change this setting, select **Edit** next to **Audio Conferencing** and in the **Audio Conferencing** pane, choose an option under **Dial-out from meetings**.|

> [!NOTE]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

## Related topics

- [Manage the Audio Conferencing settings for your organization](manage-the-audio-conferencing-settings-for-my-organization-in-teams.md)
- [Audio Conferencing common questions](audio-conferencing-common-questions.md)
