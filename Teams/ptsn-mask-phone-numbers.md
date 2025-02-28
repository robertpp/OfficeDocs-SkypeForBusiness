---
title: Mask phone numbers in Microsoft Teams meetings
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.reviewer: oscarr
ms.date: 02/18/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.subservice: teams-audio-conferencing
audience: Admin
ms.collection: 
  - M365-collaboration
  - m365initiative-meetings
f1.keywords: 
  - NOCSH
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
description: Learn how to mask phone numbers in Microsoft Teams.
---

# Mask phone numbers in Microsoft Teams meetings

When participants dial in to a Teams meeting using Audio Conferencing, only internal participants can see their full phone number. By default, participants outside of your organization can't see other participants' phone numbers. Here's an example of how external participants see phone numbers:

![an example of a masked phone number.](media/hiddenPhoneNum.png)

For specific industry use cases, as an admin, you can choose how the Audio Conferencing participants' phone numbers appear in meetings organized in their tenant. You can choose from three options:

- Phone numbers are masked only from external participants. The participants who belong to the meeting organizer's tenant still see the full phone number.
- Phone numbers are masked from everyone in the meeting except the organizer.
- Phone numbers are unmasked, which makes them visible to everyone in the meeting.

This setting is applied in the meeting where phone numbers are visible.

## Use Teams admin center to set phone-number masking

To change the Public Switched Telephone Network (PSTN) masking setting in the Teams admin center, log into the Teams admin center as an administrator, select **Meetings** > **Conference Bridges** in the navigation pane, and then select **Bridge settings**. **Display masked caller IDs** is a dropdown at the bottom of the Bridge settings pane, and allows you to choose the following:

1. Sign in to the Microsoft Teams admin center.
2. In navigation pane, expand **Meetings** > **Conference Bridges**.
3. Select **Bridge settings**.
4. For the **Masked phone numbers** dropdown, select one of the following options:

    - From participants outside your organization
    - From all meeting participants (except the organizer)
    - Turned off

5. Select **Apply**.

## Use Microsoft PowerShell to set phone-number masking

To change the PSTN masking setting in PowerShell, set the **`MaskPstnNumbersType`** parameter of the [Set-CsOnlineDialInConferencingTenantSettings](/powershell/module/teams/set-csonlinedialinconferencingtenantsettings) cmdlet to one of the available options.

To mask phone numbers only from external participants, run the following command:

```PowerShell
Set-CsOnlineDialInConferencingTenantSettings -MaskPstnNumbersType "MaskedForExternalUsers"
```

To mask phone numbers from all participants in the meeting (except the organizer), run the following command:

```PowerShell
Set-CsOnlineDialInConferencingTenantSettings -MaskPstnNumbersType "MaskedForAllUsers"
```

To disable phone number masking, run the following command:

```PowerShell
Set-CsOnlineDialInConferencingTenantSettings -MaskPstnNumbersType "NoMasking"
```
