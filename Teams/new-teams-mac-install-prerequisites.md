---
title: Deploy Microsoft new Teams client for the Mac
author: MicrosoftHeidi
ms.author: heidip
manager: jtremper
ms.topic: article
ms.date: 01/31/2025
ms.service: msteams
audience: admin
ms.collection: 
- Teams_ITAdmin_GuestAccess
- M365-collaboration
- m365initiative-deployteams
ms.reviewer: smylavarapu
search.appverid: MET150
f1.keywords:
- NOCSH
description: Learn about deploying the new Microsoft Teams desktop client for the Mac.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---
# New Teams for Mac - Overview and prerequisites

>[!Note]
> The features described in this article are available to [**Teams Public preview**](/microsoftteams/public-preview-doc-updates) and [**Microsoft 365 Targeted release**](/microsoft-365/admin/manage/release-options-in-office-365) customers only. Features and content are subject to change. Check back for updates.

The new Teams for Mac has been reimagined from the ground up with performance in mind, providing a faster, simpler, and more flexible experience. The new Teams client installs and loads faster, letting you launch the app and join meetings more quickly, giving you more time to focus on the business tasks.

The new Teams ensures more efficient use of device resources. Whether you have users on multiple accounts or tenants, the new Teams can help eliminate the silos and bring them together in one place, giving them more extensibility and scale.

## Prerequisites

### Minimum Mac and Teams versions

For information on deploying the Teams client on Mac, see [New Teams system requirements](teams-client-system-requirements.md).

### Turn on System Notification

After installing the new client, if users don't choose to Allow Notifications with the initial macOS Alert about notifications settings, then users must turn on the **Allow Notifications** from system settings.

#### System notification for Monterey OS

1. Open macOS System Preferences.
2. Go to **Notifications & Focus** and under **Notifications**, select Microsoft Teams.
3. Switch the **Allow notifications** toggle to turn on notifications.

:::image type="content" source="media/new-teams-mac-notifications-monterey.png" alt-text="new teams for mac notifications macOS Monterey":::

##### System notification for macOS Ventura and Sonoma

1. Open macOS System Preferences.
2. Go to **Notifications** and under **App Notifications**, select Microsoft Teams.
3. Switch the **Allow notifications** toggle to turn on notifications.

:::image type="content" source="media/new-teams-mac-notifications.png" alt-text="new teams for mac notifications macOS Ventura Sonoma":::

### Turn on Screen Sharing

Users can enable screen sharing for sharing content on calls and in meetings using the regular in-app flow when they first try to screen share. This action requires that they restart new Teams. The user needs to drop from the meeting. Alternatively, users can turn on permissions for screen recording under system settings.

#### Screen sharing for Monterey OS

1. Open macOS System Preferences.
2. Go to Security & Privacy > Privacy tab > Screen Recording.
3. Select the **+** sign to add Microsoft Teams to allow recording content of your screen.

:::image type="content" source="media/new-teams-mac-security.png" alt-text="new teams mac security page":::

##### Screen sharing for macOS Ventura and Sonoma

1. Go to Privacy & Security > Screen Recording.  
2. Switch the toggle for Microsoft Teams to Allow recording of the content of your screen.

:::image type="content" source="media/new-teams-mac-screen-recording.png" alt-text="new teams mac screen recording page":::

## How to uninstall new Teams Client

You can uninstall the new Teams client just like any other Mac app.

### How to clear the cache

1. Command + Space and enter Terminal.
2. rm -rf ~/Library/Group Containers/UBF8T346G9.com.microsoft.teams
3. rm -rf ~/Library/Containers/com.microsoft.teams2
