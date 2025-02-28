---
title:  Uninstall the new Teams client
ms.author: heidip
author: MicrosoftHeidi
manager: jtremper
ms.topic: article
ms.date: 01/31/2025
ms.service: msteams
audience: admin
ms.collection: 
- m365initiative-deployteams
ms.reviewer: 
search.appverid: MET150
f1.keywords:
- NOCSH
description: Learn about how to uninstall the new Microsoft Teams client.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# How to uninstall the new Teams client

## Remove new Teams for all users

To remove the new Teams from all users' computers, use the following PowerShell command:

```powershell

Remove-AppxPackage 
```

PowerShell cmdlet to remove new Teams from all users on all computers:

```powershell
Get-AppxPackage *MSTeams* -AllUsers |Remove-AppxPackage -AllUsers
```

PowerShell cmdlet for an individual user without administrator privilege:

```powershell
Get-AppxPackage *MSTeams*|Remove-AppxPackage
```

Command to uninstall teams machine-wide:
teamsbootstrapper.exe -x -m

## Further information

- If you need to remove the classic Teams client, see [How to uninstall the new Teams client](teams-client-uninstall.md).
- If you need a script to help with the uninstall of classic Teams, see [Uninstall the classic Teams client using a script](teams-client-uninstall-script.md).
