---
title: "Disabling toll-free numbers for specific Teams users"
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.reviewer: oscarr
ms.date: 02/18/2025
ms.topic: article
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
description: Learn how to control how organizers can use toll-free numbers for their Audio Conferencing Bridge meetings.
---

# Turn off toll-free numbers for specific Teams users

If your organization has toll-free numbers in its Microsoft Audio Conferencing Bridge, as an admin, you can manage whether meeting organizers can use toll-free numbers.

By default, all users in your organization can use toll-free numbers. If available, participants can use those numbers to join their meetings. If this isn't the desired behavior for some users in your organization, you can prevent specific users from using those numbers in their meetings

When you turn toll-free numbers off for a meeting organizer:

- A toll-free number is no longer included in their meeting invites.
- Toll-free numbers are no longer listed on the "Find a local number" page that's referenced in their meeting invites.
- Participants can't dial any of your organization's toll-free numbers to join the meeting.
- Participants can continue joining meetings of the organizer using toll numbers.

## Turn off toll-free numbers for specific users

You can use the Teams admin center or PowerShell to turn off toll-free numbers for specific users.

### Teams admin center

1. In the navigation pane, expand **Meetings** > **Audio Conferencing**.
1. Select an existing policy or add a new one.
1. Toggle **Include toll-free numbers in meeting invites created by users of this policy** to **Off**.
1. Select **Save**.

### PowerShell

You can turn off toll-free numbers for specific users by changing the setting for **`-AllowTollFreeDialIn`** to **Off** within the *TeamsAudioConferencingPolicy* assigned to those users. Once turned off, any new meetings these users organize don't include any toll free numbers. To learn more, see [Audio Conferencing policy settings for toll and toll-free numbers](audio-conferencing-toll-free-numbers-policy.md).

> [!IMPORTANT]
> Old and previously scheduled recurring meetings may still show toll-free numbers and participants won't be able to join such meetings using a toll-free number. You can reschedule all old and recurring meetings for these users and remove toll-free numbers from them using MMS.

## Related topics

- [Audio Conferencing policy settings for toll and toll-free numbers](audio-conferencing-toll-free-numbers-policy.md)
