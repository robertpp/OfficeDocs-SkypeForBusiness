---
title: Set the phone numbers included on invites
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.reviewer: oscarr
ms.date: 02/18/2025
ms.topic: article
ms.assetid: 32954439-d365-4125-872f-b37466ecb035
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

description: Follow these steps to create a default phone number for callers to join a Microsoft Teams meeting.
---

# Set the phone numbers included on invites in Microsoft Teams

Audio Conferencing allows users in your organization to create Microsoft Teams meetings that participants can dial in to using a phone number.

A conferencing bridge gives you a set of dial-in phone numbers for your organization. Participants can use all the numbers to join meetings, but as an admin, you can select which ones are included on the organizer's meeting invites.

> [!NOTE]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

## Initial assignment of phone numbers that are included in the meeting invites for users

The phone numbers included in the meeting invites of users enabled for Audio Conferencing are defined in the **`-TeamsAudioConferencingPolicy`**. When a user is assigned the **`-TeamsAudioConferencingPolicy`**, all toll and toll-free phone numbers added in the policy are included in their meeting invites. If a user is assigned a **`-TeamsAudioConferencingPolicy`** without any toll or toll-free numbers specified, their meeting invites display default conferencing numbers set in their individual settings.

> [!NOTE]
> Toll or toll-free phone numbers added to the *TeamsAudioConferencingPolicy* of a user take precedence over the phone numbers set individually using the default conferencing toll phone number and the default conferencing toll-free phone number in a user's settings.

In addition to phone numbers, each meeting invite includes a link that opens the full list of all dial-in phone numbers that can be used to join a given meeting.

> [!IMPORTANT]
> It can take up to 24 hours for the assigned phone numbers to show up on your meeting invite. If you aren't seeing updated numbers appear, wait at least 24 hours before contacting support.

### New users

**`-TeamsAudioConferencingPolicy`** also defines the toll and toll-free phone numbers included in meeting invites for new users. By default, all new users are assigned the Global **`-TeamsAudioConferencingPolicy`**. The Global policy doesn't have any phone numbers added, unless you change this. In this scenario, the meeting invites for users with Audio Conferencing enabled display default toll and toll-free conferencing numbers from each user's settings.

For a new user, the default conferencing toll numbers are assigned based on their **Usage Location** set in the Microsoft 365 administration center when enabling the Audio Conferencing service. If there's a toll number in the conference bridge that matches the country/region of the user, that number is automatically assigned as the user's default toll number. If there isn't one, the number defined as the default toll number of the conference bridge is assigned as the default toll number of the user.  

Once a user is enabled for the Audio Conferencing service, you can change the default toll and toll-free phone numbers of the user from their initial values as needed.

To learn how to set or change the default audio conferencing phone number for users in PowerShell using the **`-TeamsAudioConferencingPolicy`** cmdlet, see [Audio Conferencing policy settings for toll and toll-free numbers](audio-conferencing-toll-free-numbers-policy.md).

## Set or change the default audio conferencing phone number for a meeting organizer or user individually

1. Sign in to the Microsoft Teams admin center.
2. In navigation pane, expand **Users** > **Manage users**.
3. Select the user's name from the list of available users.
4. Next to **Audio Conferencing**, select **Edit**.
5. Use the **Toll number** or **Toll-free number** fields to enter the numbers for the user.
6. Select **Apply**.

> [!IMPORTANT]
> When you change a user's audio conferencing settings, existing Microsoft Teams meetings must be updated and sent to attendees.

> [!NOTE]
> The phone numbers entered in this setting are only used if the *TeamsAudioConferencingPolicy* assigned to the user doesn't have any phone numbers added.

## PowerShell

To set or change the default audio conferencing phone number for a meeting organizer or user using [Microsoft Teams PowerShell](/powershell/module/teams), set the **`ServiceNumber`** or **`TollFreeServiceNumber`** parameters of the [Set-CsOnlineDialInConferencingUser](/powershell/module/teams/set-CsOnlineDialInConferencingUser) cmdlet to one of the available numbers.

## Related topics

- [Try or purchase Audio Conferencing in Microsoft 365 for Microsoft Teams](try-or-purchase-audio-conferencing-in-office-365-for-teams.md)
- [Change the phone numbers on your Audio Conferencing bridge](change-the-phone-numbers-on-your-audio-conferencing-bridge.md)
