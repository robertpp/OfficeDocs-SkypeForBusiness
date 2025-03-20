---
title: Admins- Manage transcription and captions for Teams meetings
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.topic: article
ms.service: msteams
audience: admin
ms.collection: 
  - M365-collaboration
  - m365initiative-meetings
  - highpri
  - Tier1
  - magic-ai-copilot
ms.reviewer: harinlee
ms.date: 2/28/2025
search.appverid: MET150
ms.localizationpriority: medium
f1.keywords:
- NOCSH
description: Learn how to configure transcription and caption policies for Teams meetings and events.
appliesto: 
  - Microsoft Teams
---

# Admins- Manage transcription and captions for Teams meetings

[!INCLUDE[Teams Premium](includes/teams-premium-ecm.md)]

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Meetings ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Webinars ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Town halls

> [!NOTE]
> When organizers turn off Microsoft 365 Copilot in Teams meetings and events, recording and transcription are also turned off. To learn more about Copilot, see [Manage Microsoft 365 Copilot in Teams meetings and events](copilot-teams-transcription.md).

Microsoft Teams offers transcription and live captions to enhance accessibility and engagement during meetings and events. Transcription creates a real-time written record of what was said during a meeting or event. Participants can view the transcript after the meeting along with timestamps and speaker attribution. Live captions provide real-time subtitles during the meeting. Teams doesn't save captions.

As an admin, you can manage whether your users can use and access transcripts and captions for Teams meetings and events.

## Live transcription

Transcription is both a per-organizer and per-user policy setting. For meetings and events to include transcripts, the organizer must have this setting turned on. The user who starts the recording or transcript must also have this setting turned on.

When live transcription is turned on, users have a real-time written copy of the meeting's conversation. After the meeting, users can find the searchable transcription stored with the meeting recording. If transcription was turned on for the recording, Stream plays the video with the transcript next to the recording, and shows who is speaking and when as the video plays.

If recording is turned on, but transcription is turned off, the recording doesn't have a transcript file stored next to it. Also, when viewing the recording playback in Stream, captions can't be turned on.

The transcription link remains for the lifetime of the file in most cases, but can be broken if the video file is copied within the same OneDrive or SharePoint site. This action would result in captions not displaying on the copied video file.

Transcripts are stored together with meeting recordings in OneDrive and SharePoint storage. To learn more about how transcripts are stored, see [Teams meeting recording and transcript storage and permissions in OneDrive and SharePoint](tmr-meeting-recording-change.md) and [View, edit, and manage video transcripts and captions](https://support.microsoft.com/office/3cb9acb6-05b2-4f59-a50d-7df61123aa20#bkmk_how-captions-and-transcripts-are-stored).

> [!NOTE]
> Transcription for recorded meetings is currently only supported for English (US), English (Canada), English (India), English (UK), English (Australia), English (New Zealand), Arabic (United Arab Emirates), Arabic (Saudi Arabia), Chinese (Simplified, China), Chinese (Traditional, Hong Kong SAR), Chinese (Traditional, Taiwan), Czech (Czechia), Danish (Denmark), Dutch (Belgium), Dutch (Netherlands), French (Canada), French (France), Finnish (Finland), German (Germany), German (Switzerland), Greek (Greece), Hebrew (Israel), Hindi (India), Hungarian (Hungary), Italian (Italy), Japanese (Japan), Korean (Korea), Norwegian (Norway), Polish (Poland), Portuguese (Brazil), Portuguese (Portugal), Romanian (Romania), Russian (Russia), Slovak (Slovakia), Spanish (Mexico), Spanish (Spain), Swedish (Sweden), Thai (Thailand), Turkish (Türkiye), Ukrainian (Ukraine), Vietnamese (Vietnam), Welsh(United Kingdom).

### Use the Teams admin center to manage transcription

In the Teams admin center, you can manage the **Transcription** setting for your users within a meeting policy located under **Meetings** > **Meeting policies**. This setting is **On** by default for new policies.

### Use PowerShell to manage transcription

You can use the **`-AllowTranscription`** parameter in the[Set-CsTeamsMeetingPolicy](/powershell/module/skype/set-csteamsmeetingpolicy) cmdlet to manage transcription.

```powershell
Set-CsTeamsMeetingPolicy -Identity <policy name> -AllowTranscription $True
```

For information on how your users can use transcription, see [View live transcription in a Teams meeting](https://support.microsoft.com/office/dc1a8f23-2e20-4684-885e-2152e06a4a8b).

## Live translated transcription (Teams Premium)

By default, transcripts are shown in the language spoken that's during a meeting or event. Live translated transcription allows your users to translate the meeting or event transcript into the language they're most comfortable with. The meeting or event organizer must have a Teams Premium license for attendees to use live translated transcription.

To turn on **Live translated transcription**, **Transcription** must be set to '**On**' in the corresponding meeting policy in the Teams admin center. To turn off **Live translated transcription**, set **Transcription** to **Off**.

For information on how your end users can turn on live translated captions, read [View live transcription in Microsoft Teams meetings](https://support.microsoft.com/office/view-live-transcription-in-microsoft-teams-meetings-dc1a8f23-2e20-4684-885e-2152e06a4a8b).

## Live captions

Teams can detect what was said in a meeting, webinar, or town hall and present real-time captions along with speaker attribution.

This setting is a per-user policy and applies during a meeting. This setting controls whether the **Turn on live captions** option is available for the user to turn automatically generated live captions on or off in meetings that the user attends. These captions aren't saved alongside the video file.

:::image type="content" alt-text="This screenshot shows the menu initiated by selecting the ellipses icon. The option to Turn on live captions is highlighted." source="media/meeting-policies-live-captions.png" lightbox="media/meeting-policies-live-captions.png":::

|Teams admin center policy option|Parameter value in PowerShell| Behavior|
|---|---|---|
| Off, but organizers and co-organizers can turn them on | DisabledUserOverride| **This value is the default setting.** Live captions are off by default, but users with this assigned policy can turn on live captions during meetings or events. |
| Off | Disabled | Users with this assigned policy can't use live captions in meetings or events.|

### Use the Teams admin center to manage live captions

In the Teams admin center, you manage the **Live Captions** policy setting within a meeting policy located under **Meetings** > **Meeting policies**. This setting is off by default.

### Use PowerShell to manage live captions

You can use the **`-LiveCaptionsEnabledType`** parameter in the [Set-CsTeamsMeetingPolicy](/powershell/module/skype/set-csteamsmeetingpolicy) cmdlet to manage live captions.

To disable live captions for users with this policy, run the following script:

```powershell
Set-CsTeamsMeetingPolicy -Identity <policy name> -LiveCaptionsEnabledType Disabled
```

To enable live captions for users with this policy, run the following script:

```powershell
Set-CsTeamsMeetingPolicy -Identity <policy name> -LiveCaptionsEnabledType DisabledUserOverride 
```

To learn how your end users can use live captions for meetings and webinars, see [Use live captions in a teams meeting](https://support.microsoft.com/office/4be2d304-f675-4b57-8347-cbd000a21260).

For details on how your organizers can create human-generated captions, see [Use CART captions in a Microsoft Teams meeting](https://support.microsoft.com/office/2dd889e8-32a8-4582-98b8-6c96cf14eb47).

## Live translated captions (Teams Premium)

Live translated captions allow your users to see captions translated into the language they’re most comfortable with. By default, live captions are displayed in the language spoken during a meeting or event. For town halls, organizers can pre-select up to 6 languages for attendees to use during the event. With a Teams Premium license, this limit increases to 10 languages. The meeting or event organizer must have a Teams Premium license for attendees to use live translated captions.

To turn on Live translated captions, you must set **Live captions** to **'Off, but organizers and co-organizers can turn them on'** in the corresponding meeting policy in the Teams admin center. To turn off Live translated captions, set **Live captions** to **Off**.

For information on how your end users can use live translated captions, see [Use live translated captions in a teams meeting](https://support.microsoft.com/office/use-live-captions-in-microsoft-teams-meetings-4be2d304-f675-4b57-8347-cbd000a21260).

## Manage whether organizers can prevent participants from copying or forwarding meeting chat messages, live captions, and transcripts

As an admin, you can choose whether organizers in your organization can restrict participants from copying or forwarding meeting chat messages, live captions, transcripts, and AI-generated insights in the meeting recaps. This setting also restricts forwarding and sharing messages to Outlook. By default, this per-organizer setting is set **On**. To learn more, see [Manage chat for sensitive Teams meetings](manage-chat-sensitive-meetings.md).

## Diagnostics for transcripts

You can run the Teams transcripts diagnostic tool in the Microsoft 365 admin center to verify if a user’s account meets the requirements to transcribe a Teams meeting.

> [!NOTE]
> Diagnostics in the Microsoft 365 admin center aren't available for Microsoft 365 Government, Microsoft 365 operated by 21Vianet, or Microsoft 365 Germany.

To run the diagnostic tool for transcripts, follow these steps:

1. Select the Run Tests button to populate the diagnostic in the Microsoft 365 admin center:

   > [!div class="nextstepaction"]
   > [Run Tests](https://aka.ms/MeetingTranscribeDiag)

2. In the Username or Email field, enter the email address of the affected user.
3. In the Teams Meeting URL field, enter the meeting URL.
4. Select **Run Tests**.
5. After the diagnostic runs, select the provided links to resolve the issues that were found.

## Related topics

- [Teams meeting recording](meeting-recording.md)
- [Block the download of Teams meeting recording and transcript files from SharePoint or OneDrive](block-download-meeting-recording.md)
- [Teams meeting recording and transcript storage and permissions in OneDrive for Business and SharePoint](tmr-meeting-recording-change.md)
- [Manage Teams recording policies for meetings and events](meeting-recording.md)
- [Accessibility guide for Microsoft Teams Admins](accessibility-guide-admin.md)
- [Teams policies reference - Meetings](settings-policies-reference.md#meetings)
- [Set-CsTeamsMeetingPolicy](/powershell/module/skype/set-csteamsmeetingpolicy)
