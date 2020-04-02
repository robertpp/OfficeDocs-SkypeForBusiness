---
title: Manage the Microsoft Teams Commercial Cloud Trial offer
author: ChuckEdmonson
ms.author: chucked
manager: serdars
ms.topic: reference
audience: Admin
ms.reviewer: baluc
ms.service: msteams
search.appverid: MET150
localization_priority: Priority
description: "Office 365 users who are not licensed for Microsoft Teams can initiate a 1-year trial of Teams."
f1.keywords:
- NOCSH
ms.collection: 
  - M365-collaboration
appliesto: 
  - Microsoft Teams
---

Manage the Microsoft Teams Commercial Cloud Trial offer
=======================================================

The Microsoft Teams Commercial Cloud Trial offers existing Office 365 users in your organization who are not licensed for Microsoft Teams to initiate a 1-year trial of the product. Admins can switch this feature on or off for users in their organization.

> [!IMPORTANT]
> The Microsoft Teams Commercial Cloud Trial will be replaced by Microsoft Teams Exploratory beginning in January 2020. To learn about this new offer, read [Manage Teams Exploratory license](teams-exploratory.md).

## What's in the offer

The service plans included in this offer are:

- Exchange Foundation
- Flow for Office 365 Plan 1
- Forms
- Microsoft Planner
- Microsoft Teams (Teams1, Teams IW)
- Office 
- PowerApps for Office 365 Plan 1
- SharePoint Online Kiosk
- Stream
- Sway
- Whiteboard
- Yammer Enterprise 

The trial grants a one-year trial subscription to your entire organization. For each license assigned, the trial allocates 2 GB of SharePoint Online storage. 

## Who is eligible

Users must be enabled to sign up for apps and trials (in the Microsoft 365 admin center). For more information, see [Manage the trial](#manage-the-trial), later in this article. 

Users who do not have an Office 365 license that includes Teams can initiate the Microsoft Teams Commercial Cloud Trial offer. For example, if a user has Office 365 Business (which doesn't include Teams), they are eligible for the trial.

## Who is not eligible

Your organization is not eligible for the trial if you are a Syndication Partner Customer or if you are a GCC, GCC High, DoD, or EDU customer.

If your organization is ineligible for the Microsoft Teams Commercial Cloud Trial offer, you will not see the **Let users install trial apps and services** switch.

## How users sign up for the trial

Eligible users can sign up for the trial offer by signing in to Teams ([teams.microsoft.com](https://teams.microsoft.com)). They will see the following screen to start the trial. 

![Screenshot of the start page for the Teams IW trial.](media/iw-trial-start-screen.png)

All trials within your organization share the same start and end dates, which is the date the first user signed up for the trial. For example, if user A starts the first trial on January 25, 2019 and user B starts a trial on June 3, 2019, both users' trial will expire on January 25, 2020.

## <a name="manage-the-trial"></a>Manage the trial

The Teams Trial is meant to be initiated by individual end users, and you may not initiate the Teams Trial offer on behalf of end-user employees.

Admins can disable the ability for end users to claim trial apps and services within their organization. Currently, the trial described in this article is the only trial in this category, but it might apply to other similar programs in the future. 

### Prevent users from installing trial apps and services

You can turn off a user’s ability to install trial apps and services.

1. From the [Microsoft 365 admin center](https://portal.office.com/adminportal/home), go to **Settings** > **Settings**, select **Services**, and then select **User owned apps and services**.

    ![Screenshot of the Services page in the admin center](media/iw-trial-services.png)

2. Clear the **Let users install trial apps and services** check box.

    ![Screenshot of the User owned apps and services page in admin center](media/iw-trial-user-owned-apps-services.png)


### Manage trial availability for a user with a license that includes Teams

A user who is assigned a license that includes Teams is not eligible for the trial. When the Teams service plan is enabled, the user can sign in and use Teams. If the service plan is disabled, the user cannot sign in and is not presented with the trial option either.

To turn off access to Teams:

1. In the Microsoft 365 admin center, select **Users** > **Active users**.

2. Select the box next to the name of the user.

3. On the right, in the **Product licenses** row, choose **Edit**.

4. In the **Product licenses** pane, switch the toggle to **Off**.

    ![Screenshot of the Product licenses page in the admin center.](media/iw-trial-enable-3.png)

### Manage Teams availability for users who already claimed the trial

If a user has claimed a Teams trial license, you can remove it by removing the license or service plan.

To turn off the trial license:

1. In the Microsoft 365 admin center, select **Users** > **Active users**.

2. Select the box next to the name of the user.

3. On the right, in the **Product licenses** row, choose **Edit**.

4. In the **Product licenses** pane, switch the toggle to **Off**.

    ![Screenshot of the Teams trial license setting on the licenses pane](media/iW-trial-enable-4.png)
    
    >[!Note]
    >The Microsoft Teams Trial toggle switch will appear after the first user in the organization signs up for the trial.

### Manage Teams for users who have the trial license

You can manage users who have a trial license just like you manage users who have a regular paid license. For more information, see [Manage Microsoft Teams settings for your organization](enable-features-office-365.md).

### Upgrade users from the trial license

To upgrade users from the trial license, do the following:

1. Purchase a subscription that includes Teams.

2. Remove the Teams trial subscription from the user.

3. Assign the newly purchased license.

For more information, see [Office 365 licensing for Microsoft Teams](Office-365-licensing.md).

> [!NOTE]
> If the trial ends and a user is not immediately upgraded to a subscription that includes teams, the user data is not removed. The user still exists in Azure Active Directory and all data within Teams still remains. Once a new license is assigned to the user to enable Teams functionality again, all content will still exist. 

### Remove a legacy Microsoft Teams Trial license

As of April 22, 2019, users can begin claiming the latest Microsoft Teams Commercial Cloud Trial license. If you would like to move users in your organization off of the legacy trial license and onto the latest one, you will need to first remove the legacy Microsoft Teams Trial license from each user. Once the legacy license is removed, each affected user can claim the updated Microsoft Teams Commercial Cloud Trial license.

- If you would like to remove this license via PowerShell, see:
[Remove licenses from user accounts with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/remove-licenses-from-user-accounts-with-office-365-powershell)

- If you would like to remove this license through the admin portal, see:
[Remove licenses from users in Office 365 for business](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/remove-licenses-from-users?view=o365-worldwide)
