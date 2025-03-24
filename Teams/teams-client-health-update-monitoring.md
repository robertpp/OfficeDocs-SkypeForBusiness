---
title:  Update monitoring in the Teams admin center
ms.author: heidip
author: MicrosoftHeidi
manager: jtremper
ms.topic: article
ms.date: 02/26/2025
ms.service: msteams
audience: admin
ms.collection: 
- M365-collaboration
- m365initiative-deployteams
ms.reviewer: shals
search.appverid: MET150
f1.keywords:
- NOCSH
description: Monitoring for updates for the Teams client using the Teams admin center.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Microsoft Teams update monitoring

> [!IMPORTANT]
> This article describes a Microsoft Teams feature that hasn't yet been released. It's been announced, and it's coming soon. If you're an admin, you can find out when this feature will be released in the Message Center (in the [Microsoft 365 admin center](https://portal.office.com/adminportal/home)). For more information, see [Teams client health](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=478610) and [Monitor Teams client updates](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=478609).

As an admin, it’s important that your users have the latest and the most secure version of the Teams client. Teams update monitoring in the Teams admin center allows you to proactively monitor Teams client updates and versions. It also helps identify users who aren't on latest version of Teams, so you can support them.

This dashboard highlights the client update status for the devices in your tenant and gives Microsoft recommended insights for moving users to the latest version of Teams client.

## Access the Teams update dashboard

To access the update monitoring and insights dashboard:

1. Go to the Teams admin center and login with your Admin credentials.
1. Select **Teams client health** from the navigation pane on the left-hand side of the window.

:::image type="content" source="media/teams-client-health-main-page-alt.png" alt-text="A screenshot of the Teams client health page with callouts marked. The first callout is over the page title. The second callout is on the upper middle of a table showing details. The number three is to the upper right of this table next to search, settings, and export options.":::

|Callout number |Details  |
|---------------|---------|
|Callout 1      |The Client update widget displays the overall version status distribution for all devices in your tenant. The update status widget provides statuses by three categories:</br>- Latest Build: A device is running a Teams client build newer than the last 100% released build.</br>- One or more builds behind: A device is running a Teams client build less than 30 days old and older than the last stable build.</br>- Outdated: A device is running a Teams client build less than 90 days old and more than 30 days old. |
|Callout 2      |The table under the **Health tab** shows a more detailed breakdown of this information, such as:</br>- Client versions: The exact client version number.</br>- Release Date: The date this specific client version was fully released to the general ring.</br>- Version status: The Teams client version status.</br>- Platform: The platform for the client version.</br>- Devices on this version: The total devices in the tenant currently running this client version.</br>- Users on this version: The total number of users in the tenant currently running this client version.</br>- Percentage of total users: The percentage of total users in the tenant currently running the client version.</br>- Device Crashes: The total number of devices that experienced a client crash in the last 28 days.</br>- Device launch failures: The total number of devices that experienced a client launch failure in the last 28 days. |
|Callout 3      |You can use these buttons to:</br>- Export the table to a CSV file.</br>- Filter and search by versions.</br>- Manage settings for columns in the table. |

### Client version details

You can see your organization's client version distribution and adoption of each client version and the health of each client version in your organization. To view a detailed dashboard with insights, select any version from the health table from a row in this table.

You can identify users and devices running outdated version of Teams, and review troubleshooting insights on issues preventing users from updating to a newer version of Teams.

:::image type="content" source="media/teams-client-version-details-page.png" alt-text="A screenshot of the version details page, with callouts. The first callout, on the top left-hand side, is the client version. The second callout, underneath the first, is the date of release. The third callout, to the immediate right of the second, is the Teams client version. The fourth callout, in the middle underneath the third, has charts showing trends. The fifth, center of the screenshot, shows a table with details. The sixth, to the middle right, shows search, settings, and export options.":::

|Callout number |Details                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------|
|Callout 1      |Client versions - The exact client version number.                                                                  |
|Callout 2      |Release Date - The date this specific client version was fully released to the general ring.                        |
|Callout 3      |Version status - The Teams client version status.                                                                   |
|Callout 4      |- Devices on this version trend: The trend of devices adopting this client version the last 28 days.</br>- Device crashes trend: The trend of devices experiencing client crashes on this version in the last 28 days.</br>- Device launch failure trend: The trend of devices experiencing client launch failures on this version in the last 28 days. |
|Callout 5      |Callout 5: The table provides the following data:</br>- User: The username.</br>- Ring: The ring that the user is currently using.</br>- Device: The device name.</br>- Platform: The platform the user is running Teams client on.</br>- Platform details: Operating system details.</br>- Insight: If the user experienced an update failure and is running an outdated version of Teams.</br>- Last Activity: The timestamp of the last active update. |
|Callout 6      |You can search or filter for any client versions. You can also sort and export the dashboard's table in a CSV file. |

## Client health per user

You can also monitor Client health per user from the user’s page.

1. Go to **Teams** > **Users** > **Manage users** page.
1. Select any user account.
1. Select the **Client health** tab.

:::image type="content" source="media/teams-client-per-user-view.png" alt-text="A screenshot of the per-user view, with numbered callouts. The first callout is slightly to the right of the middle of the screenshot, over the Client health tab. The second callout is directly underneath the first, above a table. The third is on the middle right of the screenshot, above the search, settings, and export options.":::

|Callout number |Details                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------|
|Callout 1      |The Client health tab, which provides key health and update information for all clients used by the user. |
|Callout 2      |The table shows the following information:</br>- Client versions: The exact client version number.</br>- Release Date: The date on which this specific client version was fully released to the general ring.</br>- Version status: The client version status of the Teams client.</br>- Devices: The device name that the user is currently running this Teams client on.</br>- Device Crashes: The number of total crashes experienced by this client version on the user’s specific device in the last seven days.</br>- Device launch failures: Total launch failures experienced by this client version on the user's specific device in the last seven days. |
|Callout 3      |You can search or filter for any client versions. You can also sort and export the dashboard's table in a CSV file. |
