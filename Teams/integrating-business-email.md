---
title:  Integrating your business email with Microsoft Teams
author: MicrosoftHeidi
ms.author: heidip
manager: jtremper
ms.topic: article
ms.date: 03/12/2025
ms.service: msteams
audience: admin
ms.collection: 
ms.reviewer: 
search.appverid: MET150
f1.keywords:
- NOCSH
description: How to connect your business email with Microsoft Teams, to allow meeting invites and calendar items to sync between accounts.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Integrating your business email with Microsoft Teams

> [!NOTE]
> This article is intended for Global Administrators with a Microsoft 365 subscription for work or school that includes Microsoft Teams.

> [!NOTE]
> If your primary email service provider is Google Workspace, you can enable bidirectional syncing with Microsoft Teams by following the process in [Set up calendar syncing between Google Workspace and Microsoft Teams](/microsoftteams/setup-calendar-syncing-with-google-workspace?branch=main).

If you're signing into Microsoft Teams using the default domain that Microsoft provided when you purchased Microsoft 365, for example, "yourcompany.onmicrosoft.com," then your small business’s existing domain and email aren't connected to Teams. This lack of connection creates challenges for your small business:

- You and your users need to remember multiple logins.
- You and your users need to maintain two separate calendars. Without extra setup, your Teams and existing calendar can't sync.
- Meetings created in Teams aren't sent from your *.onmicrosoft.com email address and aren't visible outside of Teams. Likewise, meetings sent or received from your existing calendar provider aren't visible in Teams, even if a Teams add-on or extension in your calendar is used.

Whether you want to use Microsoft email for your business email needs or you're already using another email service provider (for example, Google Workspace), you can connect your business to Teams to manage Teams meetings. When you set up this connection, your users can:

- Sign in to Teams and other Microsoft 365 experiences with a business email.
- Sync a Teams calendar with the calendar associated with the same business email address.
- Make sure meeting invitations created in Teams, Outlook, and Bookings are sent from your existing email address. This ensures that your business email and calendars are seamlessly connected.

## Prerequisites

- **Desktop computer**: You need to complete this setup on your desktop computer. This setup can't be completed on a mobile device.
- **Admin app/Microsoft Admin Center**: If you own Microsoft Teams Essentials, you can complete this setup in the [Admin app](https://teams.microsoft.com/l/app/b47c7387-2807-440c-9fc2-7c8f46147a20) installed in Teams. For customers with other small business licenses, [learn](https://support.microsoft.com/office/add-a-custom-domain-name-071780ac-46bb-4758-b30d-39ad0aeccf42) how you can complete these steps in the Microsoft Admin Center.
- **Global Admin**: [Global Admin](/microsoft-365/admin/add-users/about-admin-roles) permissions for your Microsoft 365 environment, which allow you to buy or verify your business domain.
- **Business domain account**: You need to be able to sign in to your business domain host (for example, GoDaddy).
  1. You need to know [how to find](/microsoft-365/admin/get-help-with-domains/find-your-domain-registrar) your domain host.
  1. If you want to buy a new domain, go to the [setup page in the Admin Center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/featureexplorer), and then select **Get your custom domain set up**.
- **Admin console**: You need to be able to sign in to the Admin console for your current email provider (such as Google Workspace).

## Connect your business domain for simplified login

1. In the Admin app in Teams, go to the **Admin** tab in the left-hand navigation, and on the **Home** tab of the Admin dashboard, select the **Use your existing email and custom domain with Teams** task.
1. You need to choose your email service provider. The options are Microsoft, Google Workspace, or another service provider. Select the **Next** button to continue when ready, or the **Back** button to return to the previous screen.
1. Now you must verify ownership of your custom business domain.

    Enter your business domain and select **Verify**. We attempt to detect your domain host provider and prompt you to sign into your account. This authorization is solely for verifying domain ownership and doesn't involve any Domain Name System (DNS) changes.

    There are two methods to verify ownership:

    **Method 1: If your domain is hosted at a common registrar, such as GoDaddy, WordPress, or 1&1 IONOS, you can also sign in to that registrar and give Microsoft permission to set up your domain for you.**

    - Select **Verify**.
    - Sign in to your registrar if prompted, and then select **Authorize Microsoft to conduct verification**.
    - Return to Microsoft Teams and the setup task.

    **Method 2: To manually verify ownership and configure DNS records, follow the instructions in [Add DNS records to connect your domain](/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider).**
1. Sign out of Teams and sign back in with your updated email. Your work remains intact and your Microsoft 365 password stays the same. If you encounter issues, allow time for the process to complete and try again.
1. After you sign back into Teams with your business email, return to the Admin app in Teams and to this setup task to update email addresses for other users.
1. To integrate your business email with your Teams calendar the steps vary if you want to use Microsoft email or another email service provider.
   - **Option 1**: Use the **Add DNS records** button to add a few DNS records to your custom business domain with your domain host provider. You'll be asked to sign in to your domain host provider. After successful login, you can select the **Connect** button in the Wizard to complete the process. Once completed, email sent to and from your custom business domain will be delivered through Microsoft 365.
   - **Option 2**: To connect your business email from another provider, such as Google, follow the Wizard's steps outlined in the next section. You need to sign in to your email provider's Admin console and use the provided links and copy and paste buttons to transfer values as needed. To ensure successful calendar synchronization, carefully follow the instructions in [Integrate your existing email and calendar with Teams](#integrate-your-existing-email-and-calendar-with-teams).

## Integrate your existing email and calendar with Teams

While Google Admin Console is used as an example, the process applies to other email providers as well.

1. To forward calendar events from Google Workspace to Teams, create a route in the Google Admin Console.

    - Go to the [Google Admin Console and manage Hosts](https://admin.google.com/ac/apps/gmail/hosts).
    - Select **Add Route**.
    - In the **Add mail route** box:
        - Enter the route name: **Microsoft Teams**.
        - Under 1, **Specify email server**, choose **Single host**, and enter the host name **[HOST NAME].protection.outlook.com** (replace [HOST NAME] with your custom business domain).
        - Enter port number **25**.
        - At the bottom of the page, select **Save**.
1. Next, configure the route in the Google Admin Console to forward calendar events from Google Workspace to Teams.

    - Go to the [Google Admin Console and manage Routing](https://admin.google.com/ac/apps/gmail/routing).
    - Under **Routing**, select **Configure**.
    - In the **Add setting** dialog box:
        - Enter this short description: **Google to Microsoft**.
        - Under 1, **Email messages to affect**, select both **Inbound** and **Internal-receiving**.
        - Under 2, **For the above type of messages**, select **Modify message**.
        - Under **Spam**, select **Bypass spam filter for this message**.
        - Under **Also deliver to**, select **Add more recipients**.
            1. Under **Recipients**, select **Add**.
            1. In the **New** box, select the down arrow, and select **Advanced**.
            1. Under **Route**, select **Change route**.
            1. Select the down arrow, and then select **Microsoft Teams** (the mail route you created earlier).
            1. Under **Attachments**, select **Remove attachments from this message**.
            1. At the bottom of the **Add setting** dialog box, select **Save**.
    - At the bottom of the **Routing Add setting** dialog box, select **Save**.
1. Add a subdomain in the Google Admin Console to receive calendar events sent from Teams.

    - Go to the [Google Admin Console and manage Domains](https://admin.google.com/ac/domains/manage).
    - Select **Add a domain**.
    - Under **Enter domain name**, enter: **teams.[CUSTOM DOMAIN NAME]** (replace [CUSTOM DOMAIN NAME] with your domain name).
    - Under **Select a domain type**, select the second choice: **User alias domain**.
    - Select **Add Domain & Start Verification**.
    - Refresh the Manage domains page to confirm the new domain you added is now listed.
    - For your new domain teams.coylo.info, under **Status**, select **Activate Gmail**.
    - In the pop-up dialog box, choose **Skip MX record setup**.
    - Select **Next**.
    - On the **Route mail to another server** dialog box, select **I use another mail server**.

   > [!NOTE]
   > The next step is adding the Google mail server to your domain provider. You don't need to copy that name because it's provided when you need it.

1. Add an MX record in your domain provider to forward calendar events from Teams to Google Workspace.

    - Open a new browser tab and sign in to the website of your domain host.
    - Select your domain (for example, fourthcoffee.com).
    - Go to the **DNS Management** page.
    - Select **Add**, and enter the following:
        - Type: **MX**.
        - Host Name: **teams**.
        - Priority: **0** (if this isn't a separate field, then add it to the above address as **0 aspmx.l.google.com**).
        - Points to address or value: **aspmx.l.google.com**.
        - TTL: **3600**.
    - After the MX record is added, select **Add record**.
1. The remainder of the steps are automated. Follow the prompts in the Wizard to finish.

## For further assistance

- Small to medium size businesses can get support [on the web](https://support.microsoft.com/en-us/smallbusiness) or by using the **Support page** in the Teams Admin app.
- For more help with connecting your domain, see [Add a custom domain name](https://support.microsoft.com/office/add-a-custom-domain-name-071780ac-46bb-4758-b30d-39ad0aeccf42).

## Customer Feedback

You can provide feedback within the Admin app in Teams using the **Give Feedback** button. You can also provide feedback in our [online portal](https://aka.ms/CalendarSyncFeedback).

## Frequently asked questions

**How do I find my domain host provider?**

- For guidance and links on finding your domain host provider, see [Find your domain registrar](/microsoft-365/admin/get-help-with-domains/find-your-domain-registrar).

**What is a custom business domain?**

- A custom business domain is a unique web address for your business presence on the internet, for example, contoso.com.
