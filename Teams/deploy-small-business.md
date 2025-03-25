---
title: Set up Microsoft Teams in your small or medium business
author: MicrosoftHeidi
ms.author: heidip
manager: jtremper
ms.topic: install-set-up-deploy
audience: admin
ms.service: msteams
ms.reviewer: angch
ms.date: 03/18/2025
description: Set up Teams in your small or medium business to enable your users to collaborate using chat and file sharing, set up and attend small and large meetings, and talk via video and voice.
ms.localizationpriority: high
search.appverid: MET150
f1.keywords:
- NOCSH
ms.collection: 
  - M365-collaboration
  - m365initiative-deployteams
appliesto: 
  - Microsoft Teams
ms.custom: seo-marvel-mar2020
---

# Set up Microsoft Teams in your small or medium business

This guide is to help IT administrators in small and medium businesses learn about and set up Teams. By default, the person who signs up for and buys a Microsoft 365 for business subscription gets admin permissions. That person can assign admin permissions to other people to help them manage Microsoft 365 for their organization.

> [!NOTE]
> If you don't know who to contact at your work or school for help, try asking the person who gave you your Microsoft 365 user account and password.

Microsoft Teams is a digital hub that brings conversations, meetings, files, and apps together in one place. Because it’s built on Microsoft 365, businesses benefit from integrations with familiar Office apps and services.

Microsoft Teams can help you grow your business by empowering you to:

- Meet online with customers, partners, vendors, and colleagues. Attendees don't need Teams to join a Teams meeting.
- Share availability and schedule meetups through Bookings.
- Answer customer inquiries from your website via chat.
- Make phone calls with a Teams Phone license.
- Host high-quality webinars.
- Collaborate using files, chat, and apps.

This guide helps you get started with:

- Adding users and giving them access to Teams.
- Connecting your business’s domain to Teams.
- Syncing your existing calendar with Teams.
- Setting up Teams capabilities for your small or medium business.
- Installing Teams.
- Accessing support and sharing feedback.

If you're looking for information on how to use Teams or train others to use Teams, see our [Microsoft Adoption site](https://enablement.microsoft.com/microsoft-teams/smb) or [Microsoft Teams Training](training-microsoft-teams-landing-page.md).

> [!TIP]
> If you haven't done so already, we strongly suggest that you begin your Teams deployment with a pilot rollout. A pilot rollout allows you and a few early adopters to get familiar with Teams and its features before your planning and eventual complete rollout.

> [!IMPORTANT]
> Before you roll out Teams broadly, make sure your organization is ready by reviewing the items in: [Make sure you're ready](deploy-overview.md).

## Adding users and giving them access to Teams

Each user needs a user account and license before they can sign in and access Teams. You can add new users using the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339) by following [these instructions](/microsoft-365/admin/add-users/add-users).

If you've already set up a global or user admin account with an active Teams license, you can also use the Admin app within Teams to add users.

> [!CAUTION]
> Using a global admin account can be a security risk. When possible, we recommend using a non-global admin account.

1. Install and launch the Admin app within Teams.
1. Select the Add a user option on the Admin app Home page or within the Users page.
1. Add a single or multiple users by entering the required information.
1. Follow the prompts to buy and assign a license to the user.

You can change a user’s license at any time by selecting a user from the Users page. You can manage the license available in your environment using the Subscriptions page in the [Admin app in Teams](https://teams.microsoft.com/l/app/b47c7387-2807-440c-9fc2-7c8f46147a20).

Learn more about Teams licenses [at this link](https://www.microsoft.com/microsoft-teams/teams-products).

If you want to give your users the opportunity to try Teams before they have a Teams license, you can set up Teams Exploratory. [Learn more](teams-exploratory.md) about Teams Exploratory.

## Connecting your business' domains to Teams

When you purchase Microsoft 365, you get a default domain (For example: `contoso.onmicrosoft.com`). Without additional setup, your Microsoft 365 users have this default domain in their Microsoft 365 usernames (For example: `jane@contoso.onmicrosoft.com`).

This default domain may create confusion if your business has an existing domain (For example: contoso.com). Connecting your domain allows your users to sign in with their existing usernames and ensures that your partners and customers see a consistent identity when they interact with you over Teams. Connecting your domain to Teams doesn't impact how your domain is used for email, your website, or other products outside of Microsoft 365.

Learn more about the steps you need to take to connect your domain using the [Integrating your business email with Microsoft Teams](integrating-business-email.md) article. You can also follow [these steps](/microsoft-365/admin/setup/add-domain) to connect your domain in the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339).

## Synching your existing calendar with Teams

Teams is already connected to Exchange for calendaring by default. If you use a provider other than Exchange for email and calendaring, you can set up calendar syncing with Teams by connecting your domain. This syncing allows you and your users to see all your Teams and other meetings in both calendars. It also makes sure that incoming and outgoing Teams meetings aren't missed and meeting responses like accepts and declines are received.

For the best experience, you should connect your business’ domain before you set up calendar syncing. Follow these steps to set up calendar syncing using the [Integrating your business email with Microsoft Teams](integrating-business-email.md) article. Follow these steps to set up syncing between Google Calendar and Teams [Set up calendar syncing with Google Workspace](setup-calendar-syncing-with-google-workspace.md).

## Setting up Teams capabilities for your small or medium business

There are lots of ways you can customize Teams. The following sections show you how to set up Teams to suit the needs of your business. The order in which you set up each Teams capability is up to you. Check back frequently for setup guides for new capabilities.

Jump to the section you're interested in:

- [Chat, teams, and channels](#chat-teams-and-channels)
- [Meetings and conferencing](#meetings-and-conferencing)
- [Webinars](#webinars)
- [Teams Phone with Calling Plan](#teams-phone-with-calling-plan)
- [Scheduling through Bookings](#scheduling-through-bookings)
- [Schedule Teams meetings from Google Calendar](#schedule-teams-meetings-from-google-calendar)
- [Connect with customers on your website using Live chat](#connect-with-customers-on-your-website-using-live-chat)
- [AI powered collaboration through Copilot](#ai-powered-collaboration-through-copilot)
- [File sharing](#file-sharing)
- [Apps in Teams](#apps-in-teams)

## Chat, teams, and channels

Chat, teams, and channels are the cornerstone of Teams. **Chat** lets one or more users talk to each other, share files, and meet privately. **Teams**, which can be visible to everyone in your organization or only to a specific audience, let the right people collaborate whatever the task or occasion, whether it's a long-running project or organizing employee onboarding materials. **Channels** within teams can give a focused discussion space for specific topics, projects, departments, or any other categorization that makes sense for your team.

For details about what you should consider before rolling out chat, teams, and channels, check out [Overview of teams and channels](teams-channels-overview.md).

You don't need to do anything else for your users to start using chat, teams, and channels. However, there are lots of options for controlling how Teams is used. You can make the changes now, or wait until you can see how people are using Teams. The [Teams admin center](https://admin.teams.microsoft.com) gives you access to all of your messaging policies and settings. You can also use the [Admin app within Teams](https://teams.microsoft.com/l/app/b47c7387-2807-440c-9fc2-7c8f46147a20) to adjust the most popular settings. For more information, check out the following articles:

- [Manage messaging policies in Teams](messaging-policies-in-teams.md)
- [Teams settings](manage-teams-overview.md)

> [!TIP]
> See how you can manage team roles, access, and messaging policies by completing the [Manage Microsoft Teams](/training/modules/m365-teams-collab-manage-teams/) module on Microsoft Learn.

### Using chats, teams, and channels to collaborate externally

> [!TIP]
> For more information about guest and external access, see: [Use guest access and external access to collaborate with people outside your organization](communicate-with-users-from-other-organizations.md).

Collaboration over chat, teams, and channels can happen with people inside and outside of your organization. Enabling external collaboration may require you to adjust your Teams policies and settings.

With the proper setup, you can chat with Teams users outside of your business who are part of trusted Microsoft 365 organizations (For example, a customer or partner with a Microsoft 365 work or school account) or Teams and Skype users not managed by an organization (for example, a customer with a Microsoft 365 or Skype personal account). Enabling external chat doesn't open up other parts of your Teams environment to the Teams users you're chatting with, like meetings or files. [Learn more](trusted-organizations-external-meetings-chat.md?tabs=organization-settings) about the Teams settings and policies updates needed to allow for external chats.

If you want to give an external contact expanded access to your Teams environment, you can give them [guest access](guest-access.md). Guest access allows you to give access to teams, documents in channels, chats, and applications to people outside of your organization, while maintaining control over your business’s data. Anyone with a Microsoft 365 work, school, or personal account can be added as a guest. [Learn more](/microsoft-365/solutions/collaborate-as-team) about turning on guest access for your environment. Once guest access is enabled, [follow this guide](/microsoft-365/solutions/collaborate-as-team) to learn more about inviting guests to join you in Teams.

[Shared channels in Teams](shared-channels.md) create collaboration spaces where you can invite people who aren’t in the team hosting the channel. Only users who are owners or members of the shared channel can access the channel. Guests can’t be added to a shared channel, but you can invite people outside of your organization to participate if they have a Teams work or school account. [Learn more](/microsoft-365/solutions/collaborate-teams-direct-connect) about setting up collaboration with external participants in a shared channel.

## Meetings and conferencing

Meetings and conferencing let people in your organization meet online with partners, vendors, customers, and colleagues. Anyone with a Teams client can join **meetings** they're invited to. If an attendee doesn't have Teams, they can also join [using the web client](https://www.microsoft.com/microsoft-teams/join-a-meeting?) on a desktop or from the Teams mobile app from their mobile app store. [Learn more](plan-meetings-external-participants.md) about Teams meetings with external participants.

The participants can join in the conversation without the need for a phone by using the microphone, camera, and the screen of their device. Participants can chat, make voice calls, and share video and apps with other participants using a PC or mobile device.

There are several meetings capabilities you can use to reinforce your business's brand. **Meeting themes** are included with Teams Premium. They allow admins to customize the visual appearance of the prejoin and lobby screens by applying a specific theme. Meeting themes consist of your business's brand colors, a custom image to represent your branding, and your business's logo. To learn more about meeting themes in Microsoft Teams, see [Meeting themes](meeting-themes.md).

**Custom meeting backgrounds** allow Teams Premium admins to upload custom organizational images for their users to use as virtual backgrounds during meetings. This feature helps users maintain privacy, reduce distractions, or add a touch of business brand unity to their meetings. You can use a user or group policy to assign unique backgrounds to specific individuals or departments. If you don't have Teams Premium, individual users can upload and use their own meeting backgrounds on Teams desktop. To learn more about managing custom meeting backgrounds, see [Meeting backgrounds](custom-meeting-backgrounds.md).

**Audio conferencing** lets participants join to meetings using a regular phone by calling a conference phone number and entering a meeting ID. Audio conferencing is useful when a participant doesn't have a good Internet connection, the meeting is voice-only, or some other circumstance doesn't allow them to join via the Teams desktop or mobile app.

> [!NOTE]
> [Learn more](set-up-audio-conferencing-in-teams.md) about audio conferencing setup and licensing requirements.

> [!TIP]
> Get more familiar with meetings and events by completing the [Manage meetings, conferences, and events with Microsoft Teams](/training/modules/m365-teams-collab-manage-meetings) module on Microsoft Learn.

Meetings are enabled by default in Teams, however, you can control the meeting experience for organizers and participants. You can also set policies for what people are, and aren't, allowed to do before and during meetings. For more information, check out the following article:

- [Admin quick start - Meetings and live events in Microsoft Teams](quick-start-meetings-live-events.md)

## Webinars

Teams webinars allow you to run interactive presentations for your customers. When you set up a webinar in Teams, you can:

- Set up event registration.
- Publish speaker bios.
- Gain insight about your webinar attendance through webinar reports.

Webinars are enabled by default in your Teams environment. [Learn more](set-up-webinars.md) about managing who can schedule webinars for your business.

## Teams Phone with Calling Plan

Microsoft 365 Teams Phone with Calling Plan is a great solution for businesses with fewer than 300 users that gives you all the features of an office phone system. Teams Phone includes voicemail, caller ID, phone system menus, toll-free numbers, and more, without the need to manage a complex and costly on-premises phone system.

For more information on Teams Phone with Calling Plan for small and medium businesses, see [Teams Phone guidance for small and medium businesses](/microsoftteams/business-voice/whats-business-voice). If you need more assistance with understanding or deploying Teams Phone, contact us here: `ContactTeamsPhoneSMB@microsoft.com`.

## Scheduling through Bookings

The Microsoft Bookings functionality helps you schedule and manage appointments with your customers, clients, or colleagues. Bookings includes a web-based bookings page, which is integrated with Microsoft Outlook and Teams to optimize your calendar and give your customers the flexibility to book a time that works best for them.

- [Learn more](/microsoft-365/bookings/bookings-overview) about how Bookings can help your business streamline scheduling.
- [Learn more](bookings-app-admin.md) about how you can make the Bookings app for Teams available to users in your business.

## Schedule Teams meetings from Google Calendar

You can schedule Teams meetings directly from your Google Calendar using the Teams Meeting add-on for Google Calendar. [Learn more](https://support.microsoft.com/office/install-the-microsoft-teams-meeting-add-on-for-google-workspace-bba2dfbe-0b2b-4ee7-be10-261ad80ddb60) about installing the add-on. IT admins can also install the add-on from their Google Workplace Admin Console.

## Connect with customers on your website using Live chat

Live chat allows your website’s visitors to chat with your business through a chat widget on your customer-facing website. Visitors can ask questions via your website’s chat, connecting them directly to your support team in Teams. [Learn more](set-up-live-chat.md) about setting up and managing Live chat.

## AI powered collaboration through Copilot

Copilot in Teams can:

- Help your business perform tasks faster and enhance collaboration through the power of AI.
- Help you automate tasks so that you can focus on giving your customers and partners your full attention during meetings, calls, and chat conversations.
- Summarize key discussion points in meetings and calls, including who was speaking, what they said, and where people are aligned or disagreeing.
- Suggest action items and answer any questions you have, all in real-time during or after a meeting.
- Help you rewrite and edit chat and channel messages to improve tone, length, and clarity.
- Help you find and use information buried in documents or lost in conversations by bringing together data from your documents, presentations, email, calendar, notes, and contacts.
- Use information in Teams to help you catch up or identify tasks quickly.

Learn more about how you can enable Copilot in your Teams environment from the [small business-focused Copilot adoption site](https://adoption.microsoft.com/copilot/smb/) or [Microsoft 365 Copilot documentation](/copilot/microsoft-365/).

## File sharing

When you enable file sharing through Teams it allows your business to collaborate with partners, vendors, customers, and colleagues while protecting your business’s intellectual property and sensitive information. Files shared through Teams are owned and managed by your business rather than individuals. Users can share files from Teams channels, chats, meetings, and the OneDrive app in Teams.

By default, sharing with people outside your organization using external access, guest access, or anonymous access is enabled, but shared channels and cross-cloud scenarios require additional configuration. [Learn more](/microsoft-365/solutions/setup-secure-collaboration-with-teams) about how you can enable secure sharing for vendors, partners, and customers outside your organization.

## Apps in Teams

Apps in Teams help users bring together their business tools and services in one place where they can be used to collaborate with others. Teams apps are published by Microsoft and other companies. You can also create Teams apps specifically for your business. A few examples of apps are:

- An app to share and assign tasks to various users in a channel.
- An app that integrates with your customer management system and tracks customer leads and progress.
- An app that helps you schedule employee shifts and schedules.

As an admin, you control which apps are permitted. You can also help automatically install apps for your users. [Learn more](apps-in-teams.md) about Teams apps and how to manage them.

## Installing Teams

When you're ready for your users to start using Teams, they can install the Teams client on their Windows, Mac, or on their Android or iOS device. Users can download the Teams client directly from <https://teams.microsoft.com/downloads>.

Users can use Teams without an app installed on their desktop using the web. Access Teams on the web from [this site](https://teams.microsoft.com/).

Make sure each user in your organization has a Teams license before they can use Teams. For more information about assigning a Teams license, see [Manage user access to Teams](user-access.md#using-the-microsoft-365-admin-center).

Users will have the best experience joining meetings with a Teams license and application, but they aren't required. Customers or partners don't need a Teams license to join Teams meetings. [Learn more](anonymous-users-in-meetings.md) about how you can enable anonymous meeting join for your Teams environment.

> [!TIP]
> Get recommendations on how to plan your Teams client deployment by completing the [Deploy Microsoft Teams clients](/training/modules/m365-teams-collab-deploy-clients/) module on Microsoft Learn.

If your organization uses Microsoft Endpoint Configuration Manager, Group Policy, or a third-party distribution mechanism, to deploy software to your user's computers, see [Install Microsoft Teams using Microsoft Endpoint Configuration Manager](msi-deployment.md).

If you want detailed information about deploying Teams clients, see [Get clients for Microsoft Teams](get-clients.md).

## Accessing support and sharing feedback 

If you need more help setting up your Teams environment for your small business, you can reach out to our live support agents. Request support through the Teams Admin app by:

1. Launching the [Teams Admin app](https://teams.microsoft.com/l/app/b47c7387-2807-440c-9fc2-7c8f46147a20) within the Teams client.
1. Selecting **Support** in the left navigation.
1. Searching for the issue you need help with.
1. If the articles provided don't meet your needs, select **Contact Support**.
1. Select a method of support and a support agent will contact you.

If you have feedback on how we can improve the Teams experience for your small or medium business, you can share your thoughts in our [Microsoft Teams – Small Business Community](https://techcommunity.microsoft.com/category/microsoftteams/discussions/teamssmallbusiness).

> [!IMPORTANT]
> If you need more assistance with understanding or deploying Teams Phone, contact us here: `ContactTeamsPhoneSMB@microsoft.com`.
