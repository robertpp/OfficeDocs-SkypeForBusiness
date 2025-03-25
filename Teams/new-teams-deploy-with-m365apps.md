---
title:  Deploy the Microsoft Teams client with Microsoft 365 Apps
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
ms.reviewer: 
search.appverid: MET150
f1.keywords:
- NOCSH
description: Learn about how to upgrade to new Microsoft Teams with Microsoft 365 Apps.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---
# Upgrade to new Microsoft Teams with Microsoft 365 Apps

The new Teams app automatically installs with new and existing installations of Microsoft 365 Apps on Windows. Administrators may exclude the Teams client from automatically installing with Microsoft 365 Apps on Windows.

>[!Important]
>If the classic Teams app is already installed, the Microsoft 365 Apps deployment will install new Teams alongside classic Teams on the device. The classic Teams installation will not change.

## Rollout schedule

For more information on the timeline for the Teams clients, see [End of availability for classic Teams client](teams-classic-client-end-of-availability.md).

## Prerequisites for target computers

See [New Teams system requirements](teams-client-system-requirements.md) for information on requirements for the new Teams client.

>[!Note]
>Learn more: [**Update History for Microsoft 365 Apps**](/officeupdates/update-history-microsoft365-apps-by-date#supported-versions).

## How to exclude new Teams from new installations

Admins who don't want new Teams included with Microsoft 365 Apps on devices running Windows can follow these steps to opt out.

1. Sign in to the Microsoft 365 Apps admin center (https://config.office.com) with an admin account.
2. Go to **Customization > Device Configuration > Modern Apps Settings**.
3. Select **Microsoft Teams (work or school)**,  then clear the **Enable automatic installation of new Microsoft Teams** check box.

>[!Note]
>For the best Teams experience, we recommend leaving the setting as is.

> [!NOTE]
> If you've set Teams update policy to **Not enabled**, but users still received new Teams client with M365 Apps, please follow instructions in our [How to uninstall the new Teams client](teams-client-uninstall.md) article to uninstall it for your users.

## Office 365 plans that don't include Microsoft Teams

Some Office 365 plans include Microsoft 365 Apps, but don't include the Teams service. Teams will still be installed with Microsoft 365 Apps even if a plan doesn't have the Teams service.

For Office 365 plans that don't include the Teams service, a free trial version of Teams, valid for one year, is available. Your users can start using it when they sign in to Teams. For more information about this free trial version and providing your users access, see Manage the Microsoft Teams Commercial Cloud Trial offer.
