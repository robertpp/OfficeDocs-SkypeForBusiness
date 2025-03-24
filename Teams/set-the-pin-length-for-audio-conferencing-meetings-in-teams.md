---
title: Set the PIN length for Audio Conferencing meetings
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.reviewer: oscarr
ms.date: 02/18/2025
ms.topic: how-to
ms.assetid: b86d31c6-1543-478f-b8c6-4b71e708403a
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
description: "Learn the parameters for the length and requirements of a PIN and see how to set the length for meetings in Microsoft Teams."
---

# Set the PIN length for Audio Conferencing meetings in Microsoft Teams

When you set up Audio Conferencing for Microsoft Teams, you get an Audio Conferencing bridge. A conferencing bridge can contain one or more phone numbers. The phone number you set is included on the meeting invites for the Microsoft Teams app.
  
The Audio Conferencing bridge answers a call for users who dial-in to a meeting using a phone. It answers the caller with voice prompts from an auto attendant and then, depending on your settings, can play notifications and ask callers to record their name.

As an admin, you can use **Microsoft bridge settings** to change the settings for meeting notifications and the meeting join experience. You can also set the length of the PINs that are used by meeting organizers. Meeting organizers use PINs to start meetings if they can't join the meeting using the Microsoft Teams app.

> [!NOTE]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

## What's a PIN?

- PINs can be from 4 to 12 digits; the default is 5. Numbers are only used when creating PINs. Letters and special characters aren't used.

- A PIN is only required for the meeting organizer when a Microsoft Teams user doesn't start the meeting. If everyone is dialing in to the meeting, then the PIN is required for the meeting organizer to start the meeting.

- PIN security settings are applied to all of the phone numbers that are associated with a Microsoft bridge. They're applied to all meetings that use the phone numbers associated with a given bridge.

> [!NOTE]
> A PIN and a conference ID serve different purposes in a meeting. Callers use the conference ID to join the meeting and identify it. On the other hand, a meeting organizer uses a PIN to authenticate themselves and start the meeting when dialing in.
  
## Set the PIN length

Using the Microsoft Teams admin center:

1. In the navigation pane, expand **Meetings** > **Conference Bridges**.
2. Select **Bridge Settings**.
3. In the **Bridge settings** pane, under **PIN length**, select the number of digits you want for the PIN.
4. Select **Save**.

## Related topics

- [Try or purchase Audio Conferencing in Microsoft 365 for Microsoft Teams](try-or-purchase-audio-conferencing-in-office-365-for-teams.md)
