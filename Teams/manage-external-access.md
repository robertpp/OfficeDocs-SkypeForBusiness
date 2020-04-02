---
title: Manage external access (federation) in Microsoft Teams
author: LolaJacobsen
ms.author: lolaj
manager: serdars
ms.topic: article
ms.service: msteams
audience: admin
ms.collection: 
  - Teams_ITAdmin_GuestAccess
  - M365-collaboration
ms.reviewer: vinbel
search.appverid: MET150
f1.keywords:
- CSH
ms.custom: 
- ms.teamsadmincenter.externalaccess.overview
description: Your Teams or IT admin can configure external access for other domains (federation) to let users from those domains participate in Teams. 
appliesto: 
  - Microsoft Teams
localization_priority: Normal
---
Manage external access in Microsoft Teams
======================================================

External access is a way for Teams users from an entire external domain to find, call, chat, and set up meetings with you in Teams. You can also use external access to communicate with external users who are still using Skype for Business (online and on-premises) and Skype (in preview).

If you want external users to have access to teams and channels, guest access might be a better way to go. For more information about the differences between external access and guest access, see [Compare external and guest access](communicate-with-users-from-other-organizations.md#compare-external-and-guest-access). 

Use external access when:
  
- You have users in different domains who need to collaborate. For example, Rob@contoso.com and Ann@northwindtraders.com are working on a project together along with some others in the contoso.com and northwindtraders.com domains.

- You want the people in your organization to use Teams to contact people in specific businesses outside of your organization.

- You want anyone else in the world who uses Teams to be able to find and contact you, using your email address. 

> [!IMPORTANT]
> Currently, to federate within the Microsoft Teams app to an external user outside of your organization who's not currently a guest of your Azure Active Directory (Azure AD) or tenant, you must be correctly set up for hybrid and moved to Skype for Business Online. As of February 25, 2019, Teams doesn't support native federation without the user of the SIP profile being homed in Skype for Business Online. For more on setting up your account for hybrid and then moving to Teams, see [Upgrade Skype for Business hybrid deployment to Teams](https://docs.microsoft.com/microsoftteams/upgrade-to-teams-execute-skypeforbusinesshybrid).

## Plan for external access

By default, external access is turned on in Teams, which means that your organization can communicate with all external domains. If you add blocked domains, all other domains will be allowed; and if you add allowed domains, all other domains will be blocked. There are three scenarios for setting up external access in the Teams admin center (**Org-wide settings** > **External access**):

- **Open federation**: This is the default setting in Teams, and it lets people in your organization find, call, chat, and set up meetings with people external to your organization in any domain.

    In this scenario, your users can communicate with all external domains that are running Teams or Skype for Business AND are using open federation OR have added your domain to their allow list.

- **Allow specific domains**: By adding domains to an **Allow** list, you limit external access to only the allowed domains. Once you set up a list of allowed domains, all other domains will be blocked. To allow specific domains, click **Add a domain**, add the domain name, click **Action to take on this domain**, and then select **Allowed**.

- **Block specific domains** - By adding domains to a **Block** list, you can communicate with all external domains *except* the ones you've blocked. To block specific domains, click **Add a domain**, add the domain name, click **Action to take on this domain**, and then select **Blocked**. Once you set up a list of blocked domains, all other domains will be allowed.

## Allow or block domains

### Step 1 - Enable your organization to communicate with another Teams organization

![An icon showing the Microsoft Teams logo](media/teams-logo-30x30.png)  **Using the Microsoft Teams admin center**

1. In the left navigation, go to **Org-wide settings** > **External access**.

2. Turn on the **Users can communicate with other Skype for Business and Teams users** setting.

     ![Screenshot of Users can communicate with other Skype for Business and Teams users setting turned on](media/manage-external-access-2.png).

3. If you want to allow all Teams organizations to communicate with users in your organization, skip to step 5.

4. If you want to limit the organizations that can communicate with users in your organization, you can either allow all except some domains, or you can allow only specific domains. 

    - To allow all except some domains, add the domains you want to block by clicking **Add domain**. In the **Add a domain** pane, type the domain name, click **Blocked**, and then click **Done**. 
    - To limit communications to specific organizations, add those domains to the list with a status of **Allowed**. Once you have added any domain to the Allow list, communications with other organizations will be limited to only those organizations whose domains are in the Allow list. 

5. Click **Save**.

6. Make sure the admin in the other Teams organization completes these same steps. For example, in their **allowed domains** list, their admin needs to enter the domain for your business if they limit the organizations that can communicate with their users.

### Step 2 - Test it

To test your setup, you need a Teams user who's not behind your firewall.
  
1. After you and the admin from the organization have changed the **External access** settings, you should be good to go.

2. In the Teams app, search for the person by email address, and send a request to chat.

3. Ask your Teams contact to send you a request to chat. If you don't receive their request, the problem is your firewall settings (assuming they've already confirmed their firewall settings are correct).

4. Another way to test whether the problem is your firewall is to go to a WiFi location not behind your firewall. such as a coffee shop, and use Teams to send a request to your contact to chat. If the message goes through at the WiFi location, but does not when you're at work, then you know the problem is your firewall.

> [!NOTE]
> If you and another user both turn on external access and allow one another's domains, this will work. If it doesn't work, the other user should make sure their configuration isn't blocking your domain.

## Communicate with users in a Skype for Business Online organization

If you're setting up external access to let your Teams users find and contact users in a Skype for Business organization that limits who can contact their users, follow the steps to set up external access from your domain to the other organization's domain. Then ask the admin in the other organization to follow the steps below to configure external access for Skype for Business Online.

For specific guidance on common Skype for Business Online scenarios, see [Common external access scenarios](#common-external-access-scenarios) below.

![An icon showing the Skype for Business logo](media/sfb-logo-30x30.png) **Using the Skype for Business admin center**

Have the admin in that organization do these steps:

1. In the Microsoft 365 admin center, go to **Admin Centers** > **Teams & Skype** > **Legacy portal**.
  
2. In the **Skype for Business admin center**, choose **Organization** > **External communications**.

3. To set up communication with a specific business or with users in another domain, in the drop-down box, choose **On only for allowed domains**.

    OR, if they want to enable communication with everyone else in the world who has open Skype for Business policies, choose **On except for blocked domains**. This is the default setting.

4. Under **Blocked or allowed domains**, choose **+**, and then add the name of the domain you want to allow.

## Communicate with Skype users (in preview)

Follow these steps to let Teams users in your organization chat with and call Skype users. Teams users can then search for and start a one-on-one text-only conversation or an audio/video call with Skype users and vice versa.

![An icon showing the Microsoft Teams logo](media/teams-logo-30x30.png)  **Using the Microsoft Teams admin center**

1. In the left navigation, go to **Org-wide settings** > **External access**.

2. Turn on the **Users can communicate with Skype users** setting.

    ![Screenshot of Users can communicate with Skype setting turned on](media/manage-external-access-5.png).

To learn more about the ways that Teams users and Skype users can communicate, including limitations that apply, see [Teams and Skype interoperability](teams-skype-interop.md).

## Common external access scenarios

|**If you want to....**  |**Do this**  |
|---------|-----------------------|
|Let **Teams users** in your organization communicate with **Teams users** in another (external) organization.|In External Access, add the external domain to the Allowed list or use open federation. Then have the administrator in the other Teams organization do the same thing.      |
|Let **Teams users**  in your organization  communicate with **Skype for Business Online users**  in the same organization.  |Enable Coexistence mode or choose the Islands upgrade mode to support Skype for Business users in your organization.   |
|Let **Teams users** in your organization communicate with **Skype for Business Online users** in another (external) organization.      |In External Access, add the external domain to the Allowed list or use open federation. <br><br>Turn on **Users can communicate with other Skype for Business and Teams users** setting in External Access. Then have the administrator in the other Teams organization do the same thing. <br><br>**NOTE**: The external domain with Skype for Business users must enable Coexistence mode or choose the Islands upgrade mode to support Skype for Business users in that organization.|
|Let **Teams users** in your organization communicate with **Skype** users.<br> (in preview)  |Turn on the **Users can communicate with Skype users** setting in External Access. |
|Let your **Skype for Business Online users** communicate with **Teams users** in another Office 365 organization.| Your Skype for Business Online users can communicate with Teams users in another organization if your users are in one of the following upgrade modes: Islands, SfBOnly, SfBWIthTeamsCollab, SfBWithTeamsCollabAndMeetings; and the other organization's Teams users are in TeamsOnly mode. <br><br>Turn on the **Users can communicate with other Skype for Business and Teams users** setting in External Access. Then have the administrator in the other Teams organization do the same things.|
|Let your **Skype for Business Online users** communicate with **Skype for Business Online users** from another Office 365 organization.    | Your Skype for Business Online users can communicate with Skype for Business Online users in another organization if your users are in one of the following upgrade modes: Islands, SfBOnly, SfBWIthTeamsCollab, SfBWithTeamsCollabAndMeetings; and the other organization's Skype for Business Online users are in one of the following upgrade modes: Islands, SfBOnly, SfBWIthTeamsCollab, SfBWithTeamsCollabAndMeetings.<br><br>Turn on the **Users can communicate with other Skype for Business and Teams users** setting in External Access. Then have the administrator in the other Teams organization do the same things.|
|Let your **Skype for Business Online users** communicate with **Skype for Business users** from an on-premises organization.     |Your Skype for Business Online users can communicate with Skype for Business users from an on-premises organization if your users are in one of the following upgrade modes: Islands, SfBOnly, SfBWIthTeamsCollab, SfBWithTeamsCollabAndMeetings; and the other organization's Skype for Business Online users are in one of the following upgrade modes: Islands, SfBOnly, SfBWIthTeamsCollab, SfBWithTeamsCollabAndMeetings.<br><br>Turn on the **Users can communicate with other Skype for Business and Teams users** setting in External Access. Then have the administrator in the other Teams organization do the same things.|
|Let your **Skype for Business Online users** communicate with **Skype users** (inside or outside your organization).   |Turn on the **Users can communicate with Skype users** setting in External Access.|

> [!IMPORTANT]
> You don't have to add any **Skype domains** as allowed domains in order to enable Teams or Skype for Business Online users to communicate with Skype users inside or outside your organization. All **Skype domains** are whitelisted, which means all of these domains are considered ALLOWED.

## How does external access compare with guest access?

To learn about the difference between external access and guest access, read [Communicate with users from other organizations](communicate-with-users-from-other-organizations.md).

## Related topics

- [Native chat experience for external (federated) users](native-chat-for-external-users.md)
