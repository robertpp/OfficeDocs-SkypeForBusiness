---
title: Require end-to-end encryption for sensitive Teams meetings
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.topic: how-to
ms.service: msteams
ms.reviewer: maahma
ms.date: 1/9/2025
audience: admin
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.collection: 
  - m365solution-compliantmeetings
  - m365initiative-meetings
  - highpri
  - Tier1
appliesto: 
  - Microsoft Teams
description: Learn how to enable end-to-end encryption for Teams meetings.
---

# Require end-to-end encryption for sensitive Teams meetings

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Meetings ![Image of a x for no](/office/media/icons/cancel-teams.png)Webinars ![Image of a x for no](/office/media/icons/cancel-teams.png)Town halls

[!INCLUDE[Teams Premium ECM](includes/teams-premium-ecm.md)]

Whether or not you enable end-to-end encryption, Teams always secures meetings based on industry standards. Data exchanged during meetings is always secured while in transit and at rest. For more information, see [Media encryption for Teams](teams-security-guide.md#media-encryption). End-to-end encryption is provided as an additional layer of security, but in return, you have to forgo any services in the meeting that access to the meeting in return for functionality like transcription.

Think of regular Teams meeting security like a long corridor that intersects other corridors, with every intersection being carefully guarded. End-to-end encryption is like a corridor with no other junctions, just walls from where you start to where you end up. Microsoft uses the "intersections" to provide services like:

- Breakout rooms

- Microsoft 365 Copilot in Teams meetings and events

- Excel Live

- Live captions and transcription

- People dialing in by phone

- PowerPoint Live

- Recording

- Request control of shared content

- Together mode, companion mode, large gallery

All of these services require some level of data processing, which is all done in accordance with the Microsoft Privacy statement. With end-to-end encryption, you won't be able to use any of those meeting features.  If for example you were going to have an in-person meeting to discuss a major change in the company org chart, you might take extra security measures you don't usually take like pulling the blinds and covering the whiteboards and you might not let a caterer or janitor into that room because the damage from a leak could be catastrophic. Your normal in-person meeting experience might be secure enough due to other security measures like badges and cameras and security guards at the building entrance, but if you would consider hiring a security guard to sit at the meeting room entrance and restrict what goes in or out of the room, that kind of meeting online might be a candidate for end-to-end encryption. 

End-to-end encrypted meetings can be made between two parties when: the parties are using the latest version of the Teams desktop client for Windows or Mac or they are on a mobile device with the latest update for iOS and Android.

Web, Virtual Desktop (VDI), and Cloud Video Interoperability (CVI) devices aren't currently supported. Participants trying to join an end-to-end encrypted meeting from one of these platforms are blocked.

A maximum of 200 participants can attend an end-to-end encrypted meeting.

If your organization uses compliance recording for 1:1 calls, end-to-end encryption isn't available, because making that recording requires access to the recording services. An individual who needs compliance recording can't join an end-to-end encrypted meeting. For more info on how Teams supports compliance recording, see [Introduction to Teams policy-based recording for callings & meetings](teams-recording-policy.md).

> [!NOTE]
> End-to-end meeting encryption requires Teams Premium.

## Manage who can create meetings with end-to-end encryption

The Teams admin enhanced encryption policies control end-to-end meeting encryption. It is on by default in the Global (Org-wide default) policy, allowing meeting organizers with a Teams Premium license to schedule meetings, including channel meetings, that use end-to-end encryption. You can update the default policy or create more policies as needed. 

Consider what kind of user education you might need for users who are permitted to use end-to-end encryption; conscientious users may think they need to enable it for everything to be extra secure but may generate help desk calls when captions or recording don't work. 

If the policy is turned on for a meeting organizer, you can enforce end-to-end meeting encryption by using a meeting template. Sensitivity labels can enforce end-to-end encryption even if the policy isn't enabled for the meeting organizer.

To manage the end-to-end meeting encryption policy, follow these steps:

1. In the Teams admin center, select **Enhanced encryption policy**.

1. Select the policy you want to update.

1. Set **End-to-end meeting encryption**, to **Not enabled** or **Not enabled, but users can enable**.

1. Select **Save**.

## Related topics

- [Configure Teams meetings with three tiers of protection](configure-meetings-three-tiers-protection.md)
- [Use end-to-end encryption for one-to-one Microsoft Teams calls](teams-end-to-end-encryption.md)
