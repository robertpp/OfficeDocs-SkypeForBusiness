---
title: Best practice configurations dashboard for Microsoft Teams meetings
author: wlibebe
ms.author: wlibebe
manager: pamgreen
audience: Admin
ms.topic: article
ms.service: msteams
ms.reviewer: snigdha.chaturvedi
ms.date: 1/28/2025
f1.keywords:
- NOCSH
ms.localizationpriority: medium
search.appverid: MET150
ms.collection: 
 - M365-collaboration
 - m365initiative-meetings
 - Tier1
description: Learn how to use the Teams Premium usage report in the Teams admin center to know how often users are using each Teams Premium feature.
appliesto: 
 - Microsoft Teams
ms.custom: seo-marvel-apr2020
---

# Best practice configurations dashboard for Microsoft Teams meetings

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Meetings ![Image of a x for no](/office/media/icons/cancel-teams.png)Webinars ![Image of a x for no](/office/media/icons/cancel-teams.png)Town halls

As an admin, it’s important to ensure that your users have a reliable collaboration experience for their Teams meetings. The best practice configurations dashboard for Microsoft Teams meetings helps you manage and monitor your environment for seamless collaboration. This dashboard provides you with best practice configurations, the effect of your current settings, and actions you can take to follow Microsoft’s recommendations. The dashboard highlights locations that don’t follow Microsoft's recommended best practices. When you follow recommended actions, the trend of locations not adhering to best practices is tracked to help monitor progress. All monitored areas are evaluated over a period of seven days.

## Access the best practice configurations dashboard

To access the best practice configuration dashboard, follow these steps:

1. Go to the Teams admin center.
2. Expand **Meetings** from the navigation pane.
3. Under **Meetings**, select **Best practice configurations**.

   :::image type="content" source="media/db-landing-small.png" alt-text="Screenshot of the Best practice configuration dashboard." lightbox="media/db-landing-expand.png":::

   The **Summary** widget displays the number of best practices that need action and the number without issues.

   The **Best practice configurations** table provides statuses and insights for the following best practices:

    - Enable the correct ports and protocols
    - Update outdated Teams clients
    - Implement split tunneling for VPNs

   To view a detailed dashboard with recommendation, select a best practice from a row in this table. A list of IP addresses is shown by city, displaying the extent to which each location follows best practices. You can use the name of the city, country/region, or the IP address to search and filter for locations. You can also export the dashboard's table in a CSV file that you can share.

## Interpret the dashboards

The following sections provide details on the information in each best practice configuration's dashboard.

### Update outdated Teams clients

For the best meeting experience, your users should always use the latest version of Teams. The media streams in this dashboard show when Windows and Mac users are on a client build that's more than three months old, which can negatively affect meeting quality. The outdated Teams clients dashboard monitors desktop clients (Windows and Mac) across the organization and highlights the locations most impacted by outdated Teams clients. To learn more about Teams updates, see [Why it's important to keep Teams updated](teams-client-update.md#servicing-agreement).

To view outdated Teams clients, select **Update outdated client versions** in the **Best practice configurations** table.

:::image type="content" source="media/db-clients-small-1.png" alt-text="Screenshot of the Best practice configuration's outdated Teams clients dashboard." lightbox="media/db-clients-expand-1.png":::

|Callout |Description |
|--------|-------------|
|**1** |**Client versions trend** - Trend of cities with supported and outdated Teams clients. |
|**2** |**Recommended action** - Actions you should take to meet the recommended best practice configurations.|
|**3** |**Regions with out-of-date clients** - Visual map that includes a date for when this dashboard was generated and a count of cities with outdated clients. You can also search by country/city/region.|
|**4** |The table provides the following data: <ul><li>**Cities** - Cities and regions impacted.</li> <li>**Public IPs (reflexive)**- Public IPs of users on outdated clients.</li><li>**Percentage of out-of-date clients** - Percentage of streams coming from outdated versions of the Teams client.</li><li>**Number and percentage of streams** - Count of media streams coming from outdated clients.</li><li>**Status: Action required** - You must follow Microsoft's recommended actions to update the status.</li></li> </ul>|
|**5** |You can use these buttons to: <ul><li>Export the table to a CSV file.</li> <li>Filter by city, public IP address, and status.</li><li>Toggle the map view on or off.<li>Manage settings for columns in the table.</li></li> </ul>|

### Enable the correct ports and protocols

The media streams in the **Enable the correct ports and protocols** dashboard reflect Teams media communications conducted over Transmission Control Protocol (TCP) instead of User Datagram Protocol (UDP). This dashboard highlights locations that have a high proportion of streams using TCP.

You should open UDP ports on both the network and client firewalls to Microsoft Teams services to avoid any impact on meeting and call quality. UDP is the preferred network protocol for media streams and high rates of TCP usage can negatively affect the Teams user experience. To learn more about UDP ports and client firewalls, see [Microsoft 365 URLs and IP address ranges](/microsoft-365/enterprise/urls-and-ip-address-ranges#microsoft-teams).

To view ports and protocols, select **Enable the correct ports and protocols** in the **Best practice configurations** table.

:::image type="content" source="media/db-ports-small-1.png" alt-text="Screenshot of the Best practice configuration's ports and protocols dashboard." lightbox="media/db-ports-expand-1.png":::

|Callout |Description |
|--------|-------------|
|**1** |**Network traffic trend** - Trend of cities with TCP and UDP traffic. |
|**2** |**Recommended action** - Actions you should take to meet the recommended best practice configurations.|
|**3** |**Regions with TCP traffic** - Visual map that includes a date for when this dashboard was generated and a count of cities with TCP and UDP traffic. You can also search by country/city/region.|
|**4** |The table provides the following data: <ul><li>**Cities** - Cities and regions impacted.</li> <li>**Public IPs (reflexive)** - Count and list of public IPs (reflexive) that have high proportion of streams using TCP.</li><li>**Volume of TCP stream** - Volume of streams using TCP.</li><li>**Volume of UDP stream** - Volume of streams using UDP.</li><li>**Total streams** - Total of UDP and TCP streams.</li><li>**Percent of TCP** - Percentage of streams using TCP.</li><li>**Status: Action required** - You must follow Microsoft’s recommended actions to update the status.</li></li> </ul>|
|**5** |You can use these buttons to: <ul><li>Export the table to a CSV file.</li> <li>Filter by city, public IP address, and status.</li><li>Toggle the map view on or off.<li>Manage settings for columns in the table.</li></li> </ul>|

### Implement split tunneling for VPNs

This dashboard highlights locations that have a high proportion of streams that connect over a virtual private network (VPN) without split tunneling. For reliable connectivity to Teams, you should implement a direct connection for VPN users to Microsoft Teams services. Indirect connections introduce more latencies into media communications and can degrade a user’s media quality. To learn more about VPN split tunneling, see [Implementing VPN split tunneling for Microsoft 365](/microsoft-365/enterprise/microsoft-365-vpn-implement-split-tunnel).

To view split tunneling for VPNs, select **Implement split tunneling for VPNs** in the **Best practice configurations** table.

:::image type="content" source="media/db-vpn-small-1.png" alt-text="Screenshot of the Best practice configuration's VPN split tunneling dashboard." lightbox="media/db-vpn-expand-1.png":::

|Callout |Description |
|--------|-------------|
|**1** |**Network traffic trend** - Trend of cities with VPN streams and all other streaming types. |
|**2** |**Recommended action** - Actions you should take to meet the recommended best practice configurations.|
|**3** |**Regions with VPN streams** - Visual map that includes a date for when this dashboard was generated and a count of regions with VPN streams. You can also search by country/city/region.|
|**4** |The table provides the following data: <ul><li>**Cities** - Cities and regions impacted.</li> <li>**Public IPs (reflexive)** - Count and list of public IPs (reflexive) that have a high proportion of streams routed through VPN.</li><li>**Internet service provider** - Internet service provider for the stream.</li><li>**VPN streams** - Count of streams routed through a VPN.</li><li>**All other streams** - Count of streams that aren't routed through a VPN.</li><li>**Percent of VPN streams** - Percentage and volume of streams routed through VPN.</li><li>**Status: Action required** - You must follow Microsoft's recommended actions to update the status.</li></li> </ul>|
|**5** |You can use these buttons to: <ul><li>Export the table to a CSV file.</li> <li>Filter by city, public IP address, and status.</li><li>Toggle the map view on or off.<li>Manage settings for columns in the table.</li></li> </ul>|

## Related articles

- [Improve call quality in Microsoft Teams](monitor-call-quality-qos.md)
