---
title:  Export options for switching from Microsoft Teams
ms.author: heidip
author: MicrosoftHeidi
manager: jtremper
ms.topic: article
ms.date: 12/30/2024
ms.service: msteams
audience: admin
ms.collection: 
- M365-collaboration
- m365initiative-deployteams
ms.reviewer: freda.li
search.appverid: MET150
f1.keywords:
- NOCSH
description: Guidance on exporting data when migrating from Microsoft Teams to a third-party application.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Export options for switching from Microsoft Teams

Microsoft supports customer choice, including enabling the export of data at no charge when switching from Teams to another provider. For any customer who prefers to use Teams Export APIs, refer to [Steps to access the Teams Export APIs](#steps-to-access-the-teams-export-apis).

In addition to the APIs, Teams now offers a brand-new data export tool for small to medium-sized customers to export data when switching. This tool allows for unlimited exports during a 90-day period with just a single action in the Teams admin center. For more information about how to use the tool, refer to [Steps to access the Teams data export tool](#steps-to-access-the-teams-data-export-tool).

## Steps to access the Teams data export tool

1. To export your data from Microsoft Teams for switching and access the tool at no charge, select [this link](https://aka.ms/AccessTeamsDataExportTool) to contact support through the Teams admin center.
1. Choose your preferred method of contact: email or phone. Make sure to have the following information ready.
    1. Title: Use a predefined title.
    1. Description: Provide an estimate of the size of your tenant and confirmation that you are accessing the tool for the purpose of switching from Teams.
        1. The tool supports the export of data for tenants of up to 500 users.
1. When we receive your request, we begin processing it and notify you when you can access the tool.

### Access the Teams data export tool

Exporting data may involve your confidential, personal, and sensitive data. Note the following considerations:

- **Access role**: As the tool gives access to sensitive Teams data, you need to sign in to the Teams admin center as the global administrator to access it.
- **Duration**: You can use the tool for up to 90 days from the time the access is provided to the tool.
- **Download window**: After the data is prepared, you'll download a ZIP file with a series of JSON files. When the download link becomes available, you have 24 hours to download it.

> [!NOTE]
> When you start exporting data or when an export is in progress, any new data created during or after the export is not included. To capture the content that is not included, you can do another export within the 90 days.

### What the Teams data export tool supports

The data exported through the tool closely resembles the data exported through the Teams Export APIs. For more details, refer to [Export content with the Microsoft Teams Export APIs](export-teams-content.md).

The Teams data export tool allows you to export the following from Microsoft Teams:

- 1:1 chats
- Group chats
- Meeting chats
- Channel messages

The Teams data export tool also supports the following  data:

- **Team and Channel structure**: The Teams data export tool supports the Team and Channels structure. Channels are specific collaboration spaces within a team where members can focus on topics, projects, or departments.
- **User/Roster**: The Teams data export tool supports exporting the list of users who are part of a specific team or channel, including details about each user's roles.
- **Apps**: The Teams data export tool supports exporting the list of installed apps for a channel.

### What the ZIP file includes

|File name |Note |Public documentation |
|----------|-----|---------------------|
|/users/usersList.json |List of all users with user details |[List users](/graph/api/user-list) |
|/users/{userId}/messages_{userId}.json |List of messages for a user |[chats: getAllMessages](/graph/api/chats-getallmessages) |
|/users/{userId}/retainedMessages_{userId}.json |List of edit message history of a user |[chat: getAllRetainedMessages](/graph/api/chat-getallretainedmessages) |
|/users/{userId}/meetings_{userId}.json |List of meetings user is part of |[List events](/graph/api/calendar-list-events) |
|/users/{userId}/meetingRecordings_{userId}.json |List of meeting recordings links organized by a user |[onlineMeeting: getAllRecordings](/graph/api/onlinemeeting-getallrecordings) |
|/users/{userId}/meetingTranscripts_{userId}.json |List of meeting transcript links organized by a user |[onlineMeeting: getAllTranscripts](/graph/api/onlinemeeting-getalltranscripts) |
|/teams/teamsList |List of teams |[List groups](/graph/api/group-list) |
|/teams/teamsSettings |Team settings of all teams |[Get team](/graph/api/team-get) |
|/teams/{teamId}/teamMembers_{teamId}.json |List of members of a team |[List members of team](/graph/api/team-list-members) |
|/teams/{teamId}/messages_{teamId}.json |List of messages for a team  |[channel: getAllMessages](/graph/api/channel-getallmessages) |
|/teams/{teamId}/retainedMessages_{teamId}.json |Message edit history of a team |[channel: getAllRetainedMessages](/graph/api/channel-getallretainedmessages) |
|/teams/{teamId}/teamInstalledApps_{teamId}.json |List of installed apps of a team |[List apps in team](/graph/api/team-list-installedapps) |
|/teams/{teamId}/groupEvents_{teamdId}.json |List of meetings for a team |[List calendarView](/graph/api/calendar-list-calendarview) |
|/teams/{teamId}/channels_{teamId}.json |List of channels for a team |[List allChannels](/graph/api/team-list-allchannels) |
|/teams/{teamId}/channels/{channelId}/channelMembers.json |List of members of a channel (Only available for shared and private channels; standard channel members are the same as teams member.) |[List members of a channel](/graph/api/channel-list-members) |

## Steps to access the Teams Export APIs

1. To export your data out of Microsoft Teams by using the Export APIs directly at no charge, select [this link](https://aka.ms/Teamsexportbillingsuspension) to contact support through the Teams admin center.
1. Choose your preferred method of contact: email or phone. Make sure to have the following information ready.
    1. Title: Use a predefined title.
    1. Description: Provide confirmation that you are exporting through the Teams Export APIs for the purpose of switching from Teams.
1. When we receive your request, we begin the evaluation process and notify you when you can access the APIs at no charge to customer charge.

### Access the Teams Export APIs

To learn more about which data we support to export using the Teams Export APIs, see [Export content with the Microsoft Teams Export APIs](export-teams-content.md).
