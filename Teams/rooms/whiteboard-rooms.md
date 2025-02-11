---
title: "Whiteboard on Teams Rooms" 
author: mstonysmith
ms.author: tonysmit
manager: pamgreen
ms.reviewer:  yoojinjung 
ms.date: 01/08/2025  
ms.topic: article
audience: admin
ms.service: msteams  
ms.subservice: itpro-rooms  
ms.localizationpriority: medium
ms.collection:
  - M365-collaboration
  - teams-rooms-consoles
  - Tier1
ms.custom: QuickDraft  
search.appverid: MET150  
f1.keywords:
    - NOCSH   
description: Learn how to use Microsoft Whiteboard on Microsoft Teams Rooms to enhance collaboration during and outside of scheduled meetings.
---
  
# Using Microsoft Whiteboard on Microsoft Teams Rooms

Microsoft Whiteboard on Microsoft Teams Rooms is a tool for enhancing collaboration by allowing participants to visually share ideas and work together in real-time, no matter where they are. This article provides information on how to use Whiteboard in both meeting and nonmeeting scenarios.

For more information on Microsoft Whiteboard, see [Introduction to Microsoft Whiteboard](/microsoft-365/whiteboard).

## Outside of a meeting

Brainstorm effortlessly in the office by tapping the **Whiteboard** button on the home screen. With a single touch, Microsoft Whiteboard launches, enabling collaboration outside of a Teams meeting.

- **Temporary Whiteboards:** Since resource accounts don't have OneDrive, starting a whiteboard from Teams Rooms creates a temporary session. To save your work, select the **Save** button and invite your Teams work account. This ensures the whiteboard is saved in your OneDrive for Business.

    Temporary whiteboard example:
  
    ![Whiteboard example for content that isn't saved to OneDrive for Business.](media/whiteboard-rooms/whiteboard-image-1.png)

  > [!WARNING]
  > Users get an error to save the Whiteboard if they invite a participant who doesn't have OneDrive or has invited a guest.

- **Switch to online collaboration:** Transition seamlessly from local to online collaboration by selecting **Start meeting** on the whiteboarding screen. This initiates an ad-hoc meeting and presents a temporary whiteboard. Add participants to the meeting and collaborate in real-time. The temporary whiteboard is saved to the OneDrive of the first participant, in the same tenant, who doesn't join through a Teams Rooms device. Participants get an email from the whiteboard owner with a link to the whiteboard. Additionally, participants can access the whiteboard in the meeting chat's **Meeting Whiteboard** tab menu.

  Once it's saved to a participant's OneDrive for Business:
  
  ![Whiteboard example for content that is saved to OneDrive for Business.](media/whiteboard-rooms/whiteboard-image-2.png)

  > [!NOTE]
  > Upon selecting **Start meeting**, Teams Rooms users can invite others to the meeting. A participant not joining through a Teams Rooms device must join for the Whiteboard to become collaborative. Whiteboard collaboration between two Teams Rooms only isn't supported.

## In a meeting

When a remote participant shares a whiteboard in a meeting, Teams Rooms displays it in the shared content area.

- **Interactive whiteboarding:** If your Teams Rooms device is a Touch board or configured with a touch-enabled Front of Room display, you can interact with the shared whiteboard.
- **Start a whiteboard:** To start a whiteboard during a meeting from Teams Rooms devices, tap **Share** button and select **Microsoft Whiteboard**. If the meeting is scheduled by a non-MTR user in the same tenant, the whiteboard is saved in the organizer's OneDrive if they're present when the whiteboard is initiated. If the organizer isn't present when the whiteboard is initiated, the whiteboard will instead be saved in the OneDrive of a non-MTR participant present in the meeting.

> [!NOTE]
> Check your tenant settings meet the requirements outlined in [Manage sharing for Microsoft Whiteboard](/microsoft-365/whiteboard/manage-sharing-organizations) to have the **Start Whiteboard** feature.

## Whiteboard on Teams Rooms on Windows

The **Start whiteboard** feature is enabled by default for Touch board devices like Surface Hub 3. This means:

- **Home screen:** The **Whiteboard** button appears outside of meetings next to **Calendar**.
- **In-meeting Share Tray:** The **Microsoft Whiteboard** option is available.

The feature is available in Worldwide and GCC environments. 

Even if the **Start Whiteboard** feature is disabled and/or your Teams Rooms device isn't a Touch board device like Surface Hub 3, you can view and follow whiteboards shared by remote participants in a meeting. It mirrors a remote participant's view when the remote participant uses the [Follow me](https://support.microsoft.com/office/guide-participants-through-a-whiteboard-with-follow-e5950c68-4fe1-4567-b39f-8fe523abc67a) feature on the whiteboard.

## Whiteboard on Teams Rooms on Android

The **Start Whiteboard** feature is enabled by default for any Teams Rooms on Android devices. We recommend enabling the Start Whiteboard feature only for Touch board devices because they are certified for the best whiteboarding experience. When the feature is enabled: 

- **Home screen:** The **Whiteboard** button appears outside of meetings next to **Calendar**.
- **In-meeting Share Tray:** The **Microsoft Whiteboard** option is available.

The feature is available in Worldwide and GCC environments. 

Even if the **Start Whiteboard** feature is disabled on your Teams Rooms on Android device, you can view and follow whiteboards shared by remote participants in a meeting. It mirrors a remote participant's view when the remote participant uses the [Follow me](https://support.microsoft.com/office/guide-participants-through-a-whiteboard-with-follow-e5950c68-4fe1-4567-b39f-8fe523abc67a) feature on the whiteboard.

> [!NOTE]
> If needed, you can disable the **Start Whiteboard** feature via the admin setting on your device or by applying a configuration profile in Teams Admin Center under **Allow room to use Microsoft Whiteboard** setting in the **Meeting settings** section.

## Related articles

- [Microsoft Teams Rooms](rooms-plan.md)
- [Set up and use Microsoft Whiteboard](/surface-hub/whiteboard-collaboration)
