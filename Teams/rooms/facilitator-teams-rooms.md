---  
title: "Facilitator in Teams Rooms"  
author: mstonysmith
ms.author: tonysmit  
manager: pamgreen
ms.reviewer: kramachandra
ms.date: 03/18/2025  
ms.topic: article
appliesto: 
  - Microsoft Teams
audience: admin  
ms.service: msteams  
ms.subservice: itpro-rooms  
ms.localizationpriority: Medium
ms.collection: 
  - M365-collaboration
  - teams-rooms-consoles
  - Tier1
  - magic-ai-copilot
ms.custom: QuickDraft  
search.appverid: MET150  
f1.keywords:
- NOCSH 
ai-usage: ai-assisted
description: This user guide provides comprehensive set up instructions and information on using the Facilitator agent within Teams Rooms. The AI-powered Facilitator agent or app lets meeting participants hold unscheduled meetings and use Facilitator to  transcribe the entire meeting conversation and create rich AI notes with summaries, action items, and speaker attribution.
---  

# Facilitator in Microsoft Teams Rooms

[!INCLUDE [Preview feature](../includes/preview-feature.md)]

You can use the AI-powered Facilitator agent in Teams Rooms for real-time notes and action items during both scheduled, hybrid, and impromptu or ad hoc in-person meetings. In hybrid meetings, the agent appears in the notes panel. For in-person meetings, scan the QR code on the display to activate the agent as the group's assistant.

The Facilitator agent can be used in:

- **Facilitator in Teams** Used for Teams chat and meetings that are scheduled on a calendar. This can include a Teams Rooms device, where facilitator chat interactions and AI notes can be viewed by in-room participants.
- **Facilitator in Teams Rooms** Used for unscheduled, impromptu or ad hoc in-person discussions with a Teams Room device available in the meeting room. Facilitator can serve as the meeting note taker and generate AI notes for these discussions.

## Facilitator in Teams

Facilitator is an AI-powered agent that is available in Microsoft Teams that is used to automatically take notes of the conversations that happen during a meeting. Facilitator in Teams is used in both chat (peer to peer) and in meetings that are scheduled by a user. In both of these cases, a Teams Room console can also be added to the meeting invite as a participant if there is a one available in the meeting room. The meeting participants in the room can view Facilitator interactions in chat and navigate to notes to view AI notes taken during the meeting.

> [!IMPORTANT]

For more information and the requirements, see [Set up Facilitator in Microsoft Teams for collaborative AI-generated notes](/microsoftteams/facilitator-teams).

## Facilitator in Teams Rooms

When a Teams Room console is available in a room and a user wants to have an unscheduled meeting, such as adhoc, 1:1 (peer to peer), or group in-person, the meeting participants can use Facilitator in Teams Rooms and create rich AI notes with summaries, action items, containing speaker attribution.

> [!NOTE]
> Facilitator in Teams Rooms must be started by one of the persons in the room who's signed into Teams on their mobile phone within the same organization. Facilitator based offline note taking isn't available for federated or external users.

Once facilitator has been invited to the in person meeting, remote users can be added to the meeting once it's started. You can invite remote participants by looking them up on the Teams Room console.

The Facilitator agent in Teams and in Teams Rooms lets meeting participants get more out of meetings, by collaborating better, and stay more productive in both unscheduled and scheduled meetings.

> [!IMPORTANT]
> Currently, only the user who scans the QR code to start the meeting is attributed in the transcription and notes. All other meeting participants in the room are identified as generic speakers (For example, Speaker 1, Speaker 2). This will be addressed in a future update.

## Set up Facilitator

When you're setting up Facilitator in Teams and Teams Rooms, there are steps that you need to perform to enable it for scheduled meetings but there are also steps you need to follow for adhoc or unscheduled meetings to be able to use AI-generated notes, summaries, and action items.

### Facilitator for scheduled meetings

To enable AI-generated notes using Facilitator for Teams meetings:

**Step 1: Turn on Facilitator for meetings** See, [Set up Facilitator in Microsoft Teams](/microsoftteams/facilitator-teams).

This includes the steps to assign licenses to users that want to use Facilitator in Teams for AI notes, summaries, and action items for scheduled meetings. Users must have the correct licenses and Loop components enabled.

Make sure they have these licenses assigned to them.

- An eligible *Microsoft 365* base license. For the list of eligible base licenses, see [Understand licensing requirements for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing).
- An eligible *Microsoft Teams* license. Teams licenses may be included in your *Microsoft 365* subscription, or you may need to purchase a separate Teams license if you have *Microsoft 365 (no Teams)* licenses.
- A *Microsoft 365 Copilot* license. See [Where can I get Microsoft Copilot?](https://support.microsoft.com/topic/where-can-i-get-microsoft-copilot-40a622db-6d25-4266-b008-4bbcb55cf52f)
- Be a Microsoft Teams Public preview participant. See [Microsoft Teams Public preview](/microsoftteams/public-preview-doc-updates).

**Step 2: Turn on and enable Loop**  Enable Loop experiences in Teams for AI-generated notes: [Manage Loop components in your organization](/microsoft-365/loop/loop-components-configuration)

> [!IMPORTANT]
> AI-generated notes for all meetings are created by Facilitator are stored as a .loop file in a OneDrive folder titled **Meetings** of the user who initiated Facilitator in Teams. This data is treated as meeting transcript data.

In a scheduled meeting with Teams Rooms on Windows or Teams Rooms on Android devices invited, you can view notes generated by Facilitator by turning on the **Notes** button on the console.

:::image type="content" source="./media/facilitator/facilitator-8-low-res.png" alt-text="Screenshot of the facilitator in scheduled meetings experience." lightbox="./media/facilitator/facilitator-8-hi-res.png":::

### Facilitator for unscheduled meetings in Teams Rooms

To enable AI-generated notes using Facilitator in Teams Rooms:

**Step 1: Assign a Teams Rooms Pro license to each resource account you have for your Teams Rooms devices.** See, [Microsoft Teams Rooms licenses](/microsoftteams/rooms/rooms-licensing).

**Step 2: Turn on Facilitator for Teams Rooms** In the Microsoft Teams Rooms Management portal, go to **Room** > **Settings** > **Meeting** > **Facilitator QR Code** and toggle it on.

:::image type="content" source="./media/facilitator/facilitator-10-low-res.png" alt-text="Screenshot of turning on facilitator in Teams Rooms Pro Management portal." lightbox="./media/facilitator/facilitator-10-hi-res.png":::

For more information, see [Set up Facilitator in Microsoft Teams](/microsoftteams/facilitator-teams).

**Step 3: Turn on Public Preview of Microsoft Teams Rooms** In the Microsoft Teams Rooms Management portal, go to **Room** > **Settings** > **Account** > **Enable public preview** and toggle it on.

:::image type="content" source="./media/facilitator/facilitator-9-low-res.png" alt-text="Screenshot of turning on public preview in Teams Rooms Pro Management portal." lightbox="./media/facilitator/facilitator-9-hi-res.png":::

For more information, see [Pro Management Portal](/microsoftteams/rooms/rooms-pro-management)

## Discovery experience

After you perform all of the required steps and the prerequisites have been met, meeting participants will see an icon for Facilitator added to their Teams app and the QR code for Facilitator will be available on the Teams Rooms console.

When one or more users see that a meeting room is available, and they want to start an unscheduled meeting with Teams Rooms, the presence detector on Teams Rooms will wake up, a banner is displayed on the room display,  and it will inform users that they can invite Facilitator to take notes for their meeting. This banner appears when there's no scheduled meeting and the room is available for the next 10 minutes.

:::image type="content" source="./media/facilitator/facilitator-1-low-res.png" alt-text="Screenshot of the discovery experience." lightbox="./media/facilitator/facilitator-1-hi-res.png":::

## Inviting Facilitator for note taking

To invite the Facilitator agent to take notes:

- Scan the QR code on the top left of the display
- Press **Facilitator** on the home screen of the Teams Rooms console and scan the QR code shown with a mobile device.

:::image type="content" source="./media/facilitator/facilitator-2-low-res.png" alt-text="Screenshot of the invitation experience." lightbox="./media/facilitator/facilitator-2-hi-res.png":::

After scanning the QR code on your mobile device, the Teams app will show an option to invite  Facilitator with the room as the attendee. There are other options that are available in the list for you to choose from a well.

:::image type="content" source="./media/facilitator/facilitator-3-low-res.png" alt-text="Screenshot of the QR code experience." lightbox="./media/facilitator/facilitator-3-hi-res.png":::

## Meeting experience

The meeting starts with the Teams Rooms invited and transcription is turned on. The display for the Teams Rooms indicates that Facilitator is listening to the conversation and taking notes. After a few minutes, the screen will display notes and start summarizing the discussion. These notes continue to automatically update based on the ongoing conversation with the meeting participants.

:::image type="content" source="./media/facilitator/facilitator-4-low-res.png" alt-text="Screenshot of the mobile experience." lightbox="./media/facilitator/facilitator-4-hi-res.png":::

To end the meeting, use the **End** button on the Teams Room.

:::image type="content" source="./media/facilitator/facilitator-5-low-res.png" alt-text="Screenshot of the listening experience." lightbox="./media/facilitator/facilitator-5-hi-res.png":::

:::image type="content" source="./media/facilitator/facilitator-6-low-res.png" alt-text="Screenshot of the meeting notes experience." lightbox="./media/facilitator/facilitator-6-hi-res.png":::

## Accessing notes

To access the notes after the meeting, navigate to the **Recap** section in your Teams calendar or chat. The meeting is titled **Discussion with AI-generated notes in**.

:::image type="content" source="./media/facilitator/facilitator-7-low-res.png" alt-text="Screenshot of accessing notes experience." lightbox="./media/facilitator/facilitator-7-hi-res.png":::

## Frequently Asked Questions

**Question Is this feature available in both Teams Rooms on Windows and Android?**
  
- **Answer** *Currently Facilitator is available only as Public Preview on Teams Rooms on Windows and it's projected to release to Teams Rooms on Android at a later date.*

**Question** **Where do I access the notes after the meeting?**  

- **Answer** *On your Teams calendar, navigate to the meeting > **Recap** > **Notes**.*

**Question Can I turn off Facilitator during the discussion?**  

- **Answer** *You can mute the microphone in the room to ensure Facilitator or transcription doesn't capture any content. You can also remove Facilitator from the console by tapping it on the roster.*

**Question Is Facilitator agent recording the meeting?**

- **Answer**  *The Facilitator agent only turns on transcription during the meeting. The meeting won't be recorded.*

**Question How are the meeting room participants identified and attributed in AI notes and transcription?**
  
- **Answer** *Currently, only the person who scans the QR code to invite Facilitator is identified and attributed if they've enrolled their profile. Identity and attribution support for other room participants is coming at a later date.*

## Related Articles

- [What is Responsible AI?](https://support.microsoft.com/topic/what-is-responsible-ai-33fc14be-15ea-4c2c-903b-aa493f5b8d92)
- [Frequently Asked Questions: AI, Microsoft Copilot, and Microsoft Designer](https://support.microsoft.com/topic/frequently-asked-questions-ai-microsoft-copilot-and-microsoft-designer-987b275d-f6f2-4d5d-94c5-e927cffae705)
- [Providing Feedback about Microsoft Copilot with Microsoft 365 Apps](https://support.microsoft.com/topic/providing-feedback-about-microsoft-copilot-with-microsoft-365-apps-c481c26a-e01a-4be3-bdd0-aee0b0b2a423?ocid=CopilotLab_SMC_Privacy_Feedback)
