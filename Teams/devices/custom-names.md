---
title: Add a custom name for Teams panels
author: mstonysmith
ms.author: tonysmit
manager: pamgreen
ms.reviewer: eviegrimshaw
ms.date: 11/18/2024
ms.topic: article
ms.service: msteams
ms.subservice: itpro-devices
audience: Admin
appliesto: 
  - Microsoft Teams
ms.collection: 
  - teams-rooms-devices
  - Teams_ITAdmin_Devices
  - Tier1
f1.keywords: 
  - NOCSH
search.appverid: MET150
ms.localizationpriority: medium
description: This article provides the information required when you want to add in a custom name for a Microsoft Teams panel.
---

# Add a custom name for Teams panels
  
You can now customize the display name for your Teams panel. For example, you can shorten the name to something that is more easily readable for your users.  

To use custom names, it depends on the version of Teams panels app installed and the license assigned to the resource account that is signed in to that Teams panel. Verify the following:

- The Teams panel is running on version 1449/1.0.97.2024122401 or later.
- The account signed in on your Teams panel device is assigned a Teams Rooms Pro or Teams Shared Devices license.

The custom name will be displayed on the Teams panel home screen, so we recommend making sure it is clear and understandable to your users. In addition, this won't change the display name shown on Microsoft Teams Rooms if you have one inside of the room.

To set up and manage custom names for your Teams panels:

1. Sign in to the **Teams Rooms Pro Management Portal**.
2. Go to **Inventory** > **Planning** > select the account where you’d like to apply a custom name.
1. In the **Custom name** field, add the name for the Teams panel. By default, this field is automatically filled with the name that is shown in the Global Address Book (GAL).

4. Select **Save**.

> [!NOTE]
> Within 24 hours of the custom name being updated to a name other than the GAL one, the Teams panel home screen reflects the new name. The home screen will also have a tooltip that, when selected, will show the user the GAL name.

> :::image type="content" source="media/custom-names/image.png" alt-text="Screenshot of the home screen of the Teams panel with the custom name." lightbox="media/custom-names/image.png":::

> :::image type="content" source="media/custom-names/image1.png" alt-text="Screenshot of the dialogue box showing the full conference room name." lightbox="media/custom-names/image1.png":::

In Teams admin settings, an admin can view the GAL name and custom name if one has been applied under **Device settings** > **Display name**. It isn't possible to edit the name in these admin settings. Editing can only be done in the Teams Rooms Pro Management portal.

If you would like to remove the custom name, you can remove the name in the custom name field in the Teams Rooms Pro Management portal, and the display name on Teams panel will automatically default to the GAL name.

## Related articles

- [Plan for Teams panels](/microsoftteams/devices/teams-panels)
- [Certified Teams panels](teams-panels-certified-hardware.md)
