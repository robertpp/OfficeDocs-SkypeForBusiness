---
title: Manage messaging policies in Teams
ms.author: lolaj
author: lolajacobsen
manager: serdars
ms.reviewer: jastark
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.collection: 
  - M365-collaboration
audience: Admin
appliesto: 
  - Microsoft Teams
localization_priority: Normal
search.appverid: MET150
f1.keywords:
- CSH
ms.custom: 
  - ms.teamsadmincenter.messagingpolicies.overview
description: "Learn about Messaging policies and how they can be used to control chat messaging in Teams."
---

# Manage messaging policies in Teams

<!--- Add zone marker here--->

Messaging policies are used to control which chat and channel messaging features are available to users in Microsoft Teams. You can use the default policy that is created automatically or create one or more custom messaging policies for people in your organization. After you create a policy, you can assign it to a user or group of users in your organization.

By default, a policy named Global (org-wide default) is created. All users in your organization will be assigned this messaging policy by default. You can either make changes to this policy or create one or more custom policies and assign users to them. When you create a custom policy, you can allow or prevent certain features from being available to your users and then assign it to one or more users who will need the settings applied to them. 

## Change or create a messaging policy

You can easily manage messaging policies in the Microsoft Teams admin center (https://admin.teams.microsoft.com) by signing in with administrator credentials and choosing **Messaging policies** in the left navigation pane. To edit the existing default messaging policy for your organization, select the **Global (Org-wide default)** row, and then make your changes. To create a new custom messaging policy, select **New policy**, give the new policy a name, and then select your settings. Choose **Save** when you are done.

For example, say you want to make sure that sent messages aren't deleted or altered. You would create a new custom policy named "Retain sent messages" and turn off the following settings:

- Owners can delete sent messages
- Users can delete sent messages
- Users can edit sent messages

Then assign the policy to the users.

> [!NOTE] 
> A user can only be assigned one messaging policy at a time.
 
## Assign a messaging policy to a user

If you create a custom messaging policy, it will only be active for a user if the policy is assigned to the user. To assign a custom policy to a user, go to the Microsoft Teams admin center, choose **Users** in the left navigation pane, and select the user you want to assign the policy to. On the user's page, choose **Edit** next to **Assigned policies**. Then, in the **Edit user policies** pane, under **Messaging policy**, select the messaging policy from the drop-down list, and select **Save**. You can also edit settings from the list of users. To do this, select the user by clicking to the left of the user's display name. Select **Edit settings**. Then, on the **Edit settings** pane, under **Messaging policy**, select the policy from the drop-down list and then select **Save**.

If you are applying a policy to more than one user, select each of the users by clicking to the left of the user name, and then select **Edit settings**. On the **Edit Settings** pane, under **Messaging policy**, select the policy from the drop-down list and then select **Save**.

You can also assign a messaging policy to one or more users as follows:

1. Go to **Microsoft Teams admin center** > **Messaging policies**.
2. Select the policy by clicking to the left of the policy name.
3. Select **Manage users**.
4. In the **Manage users** pane, search for the user by display name or by user name, select the name, and then select **Add**. Repeat this step for each user that you want to add.
5. When you are finished adding users, select **Save**.

> [!NOTE]
> You can't delete a policy if users are assigned to it. You must first assign a different policy to all affected users, and then you can delete the original policy.

<!--- End zone marker here--->

## Messaging policy settings

Use the following settings to change the global messaging policy or create a new custom policy:

- **Owners can delete sent messages**  Use this setting to let owners delete messages that users sent in chat.
- **Users can delete sent messages** Use this setting to let users delete messages that they sent in chat.
- **Users can edit sent messages** Use this setting to let users edit the messages that they sent in chat.
- **Read receipts** Read receipts allow the sender of a chat message to be notified when their message was read by the recipient in 1:1 and group chats 20 people or less. Message read receipts remove uncertainly about whether a message was read, and improve team communication. Please note that read receipts are not captured in eDiscovery reporting.  
    - **User controlled** This means that users get to decide if they want read receipts ON or OFF. Default setting within the app is ON. Users can then turn it OFF. 
    - **On for everyone** This means everyone in the tenant will have the feature ON with no option to turn it off. Be aware that when using the **On for everyone** setting, the only way to set receipts for the whole tenant is either to have only one messaging policy for the whole tenant (the default policy named "Global (Org-wide Default)") or to have all messaging policies in the tenant use the same settings for receipts. The read receipts feature is most effective when the feature is enabled to **On for everyone**.
    - **Off for everyone** This means the feature is disabled and no one in the tenant has read receipts nor can they turn it on. 
<a name="bkchat"> </a>

- **Chat**  Turn this setting on if you want users in your organization to be able to use the Teams app to chat with other people.
- **Use Giphys in conversations**  If you turn this on, users can include Giphys in chat conversations with other people. Giphy is an online database and search engine that allows users to search for and share animated GIF files. Each Giphy is assigned a content rating.
- **Giphy content rating** 
    - **No restriction** This means that your users will be able to insert any Giphy in chats regardless of the content rating.
    - **Moderate**  This means that your users will be able to insert Giphys in chats, but will be moderately restricted from adult content.
    - **Strict**  This means that your users will be able to insert Giphys in chats, but will be strictly restricted from adult content.
- **Use Memes in conversations** If you turn this on, users can include Memes in chat conversations with other people. 
- **Use Stickers in conversations** If you turn this on, users can include Stickers in chat conversations with other people.
- **Allow URL previews** Use this setting to turn automatic URL previewing on or off in messages.
- **Allow users to translate messages** Turn this setting on to let users automatically translate Teams messages into the language specified by their personal language settings for Office 365.
- **Allow immersive reader for viewing messages** Turn this setting on to let users view messages in Microsoft Immersive Reader. Immersive Reader is a learning tool that provides a full screen reading experience to increase readability of text.
- **Send urgent messages using priority notifications** If you turn this on, users can send messages using [priority notifications](https://support.microsoft.com/article/mark-a-message-as-important-or-urgent-in-teams-ea99d5b6-1317-4550-8d75-86ff14cd4462). Priority notifications notify users every 2 minutes for a period of 20 minutes or until messages that are marked as *urgent* are picked up and read by the recipient, maximizing the likelihood that the message is acted upon in a timely manner.   [!INCLUDE [pri-message-offer](includes/pri-message-offer.md)]
- **Audio message creation** 
  > [!Important]
  > Audio messages are not captured in eDiscovery reporting. 
    - **Allowed in chats and channels** This means that users can leave audio messages in both chats and channels.
    - **Allowed in chats only** This means that users can leave audio messages in chats, but not in channels.
    - **Disabled** This means that users cannot create audio messages in chats or channels.  
- **On mobile devices, display favorite channels above recent chats** Enable this setting to move favorite channels to the top of the mobile device screen so that a user doesn't need to scroll to find them. 
- **Allow a user to remove users from a group chat** Turn this setting on to let a user remove other users from a group chat. This feature lets you continue a chat with a smaller group of people without losing the chat history.

> [!NOTE]
> Some of these settings, such using Giphys, can also be configured at the team level by team owners and at the private channel level by private channel owners.

### Related topics
[Meeting policies in Teams](meeting-policies-in-teams.md)
