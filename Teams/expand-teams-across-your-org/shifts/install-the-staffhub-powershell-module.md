---
title: Install the StaffHub PowerShell module
author: LanaChin
ms.author: v-lanac
ms.reviewer: lisawu
manager: serdars
ms.topic: article
audience: admin
ms.service: msteams
search.appverid: MET150
description: Learn how to install and connect to the Microsoft StaffHub PowerShell module.
f1.keywords:
- NOCSH
localization_priority: Normal
ms.collection: 
  - M365-collaboration
  - Teams_ITAdmin_FLW
appliesto: 
  - Microsoft Teams
---

# Install the Microsoft StaffHub PowerShell module

> [!IMPORTANT]
> Effective December 31, 2019, Microsoft StaffHub will be retired. We’re building StaffHub capabilities into Microsoft Teams. Today, Teams includes the Shifts app for schedule management and additional capabilities will roll out over time. StaffHub will stop working for all users on December 31, 2019. Anyone who tries to open StaffHub will be shown a message directing them to download Teams. To learn more, see [Microsoft StaffHub to be retired](microsoft-staffhub-to-be-retired.md).  

Use the steps in this article to install and connect to the Microsoft StaffHub PowerShell module. You'll need this to [move your StaffHub teams to Teams](move-staffhub-teams-to-shifts-in-teams.md).

## Install the Microsoft StaffHub PowerShell module

1. Download the [StaffHub PowerShell module](https://www.powershellgallery.com/packages/MicrosoftStaffHub).
2. Open Windows PowerShell 3.0 or later as an admin. To do this, click **Start**, type **Windows PowerShell**, right-click **Windows PowerShell**, and then select **Run as administrator**.
    > [!NOTE]
    > To get the latest version of Windows PowerShell, see [Installing Windows PowerShell](https://docs.microsoft.com/powershell/scripting/install/installing-windows-powershell).
3. Run the following:

    ```PowerShell
    $ENV:PSModulePath
    ```
4. Check the folder path in the output and make sure that all folders in the path exist on your computer before you go to the next step. If folders are missing, create them.
5. Run the following to allow for installation of the StaffHub PowerShell module:

    ```PowerShell
    Set-ExecutionPolicy RemoteSigned
    ```
6. Run the following, where &lt;path&gt; is the path in the output from step 3. For example, the path might look like C:\Users\User1\Documents\WindowsPowerShell\Modules.

    Be sure to run each command separately.

    ```PowerShell
    Install-Module -Name PackageManagement -Force  -AllowClobber
    Install-Module -Name PowerShellGet -Force  -AllowClobber
    ```
7. Exit Windows PowerShell.
8. Open Windows PowerShell 3.0 or later as a global admin, and then run the following:

    ```PowerShell
    Install-Module -Name MicrosoftStaffHub
    ```

## Connect to the Microsoft StaffHub PowerShell module

1. Run the following:

    ```PowerShell
    Connect-StaffHub
    ```

2. When you're prompted, log in as a global admin.

## Related topics

- [Microsoft StaffHub PowerShell reference](https://docs.microsoft.com/powershell/module/staffhub/?view=staffhub-ps)
- [Move your Microsoft StaffHub teams to Shifts in Teams](move-staffhub-teams-to-shifts-in-teams.md)
