---
title: Considerations for Calling Plans
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: roykuntz
ms.date: 05/08/2024
ms.topic: article
ms.assetid: 589bf5f5-490a-4215-8588-99bab7d33e31
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
audience: Admin
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
ms.custom:
  - Calling Plans
description: "Learn about emergency calling considerations for Microsoft Calling Plans."
---

# Emergency calling considerations for Microsoft Calling Plans

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Microsoft Calling Plans

This article describes emergency calling considerations for Microsoft Calling Plan users. Before reading this article, see emergency calling concepts and definitions in [Plan and manage emergency calling](what-are-emergency-locations-addresses-and-call-routing.md).

To find out if Microsoft Calling Plans are the right solution for your business, see [Public Switched Telephone Network (PSTN) connectivity options](pstn-connectivity.md) and [Microsoft Calling Plans for Teams](calling-plans-for-office-365.md).

## Emergency call enablement for Calling Plans

Each Calling Plan user is automatically enabled for emergency calling and is required to have a registered emergency address associated with their assigned telephone number.

The point in time when the location is associated to the telephone number depends on the country/region:

- In the United States and Canada, an emergency location is required when a number is assigned to a user.

- For other countries/regions&mdash;such as in Europe, the Middle East, and Africa (EMEA)&mdash;an emergency location is required when you get the phone number from Microsoft 365, or when the number is transferred from another service provider or carrier.

## Dynamic emergency calling for Calling Plans

Dynamic emergency calling for Calling Plans provides the capability to configure and route emergency calls based on the current location of the Teams client. The ability to automatically route to the appropriate Public Safety Answering Point (PSAP), or to notify security desk personnel, varies depending on the country/region of the Teams user.

Dynamic location for routing emergency calls is supported in the United States as follows.

- If a Teams client for a United States Calling Plan user dynamically acquires an emergency address within the United States, that address is used for emergency routing instead of the registered address. The call is automatically routed to the PSAP in the serving area of the address.

- If a Teams client for a United States Calling Plan user doesn't dynamically acquire an emergency address within the United States, then the registered emergency address is used to help screen and route the call. Calls from Common Area Phones and Microsoft Teams Rooms route directly to the PSAP. Otherwise, the call is screened to determine if an updated address is required before connecting the caller to the appropriate PSAP.

Dynamic location for routing emergency calls is supported in Canada the same as in the United States with the following exception: all emergency calls are screened nationally before being transferred to the PSAP.

For more information, see [Plan and configure dynamic emergency calling](configure-dynamic-emergency-calling.md).

## Emergency call routing for Calling Plans

When a Calling Plan user dials an emergency number, how the call is routed to the PSAP depends on the following:

- Whether the emergency address is dynamically determined by the Teams client

- Whether the emergency address is the registered address associated with the user's phone number

- The emergency calling network of that country/region

## Emergency call routing for different countries/regions

This section describes how emergency call routing is supported for Microsoft Calling Plans in different countries/regions.

CLI - Calling Line Identifier<br>
DID - Direct Inward Dialing<br>
EDB - Emergency DataBase<br>
LAC - Location Area Code<br>
PSAP - Public Safety Answering Point<br>

| Country  | How emergency calling works | 
| -------------------- | ----------- | 
| Australia | Emergency addresses are configured and routed by the carrier partner.  | 
| Austria | All outbound calls to Emergency Services are routed to the correct PSAP based on the LAC/first digits of the caller’s number. In Austria, there is no national EDB. The PSAPs will contact the operator in case they are not able to get the address from the caller.| 
| Belgium | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the PSAP system looks up the address against the number and displays it to the PSAP operator.  |
| Canada |  All outbound calls to Emergency Services are first screened to determine the current location of the user before being routed to the local PSAP. |
| Croatia | All outbound calls to Emergency Services are sent to the local PSAP based on the phone number prefix. For non-geo numbers, calls are routed to the national PSAP.  |
| Czech Republic | All outbound calls to Emergency Services are routed to the incumbent Operator, then routed to the East or West Call Centers, and then distributed to the appropriate Emergency Services Provider.  |
| Denmark | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB – when a call is made to the PSAP with the CLI, the Local PSAP system looks up the address against the number and displays it to the PSAP operator.  | 
| Estonia | All outbound calls to Emergency Services are sent to the local PSAP based on the phone number prefix. For non-geo numbers, calls are routed to the national PSAP.  |
| Finland | All outbound calls to Emergency Services are routed to the Local PSAP, and then distributed to the appropriate Emergency Services Provider.   |
| France | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the PSAP system looks up the address against the number and displays it to the PSAP operator.  |
| Germany | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the PSAP system looks up the address against the number and displays it to the PSAP operator.  |
| Hungary | All outbound calls to Emergency Services are routed to the Local PSAP, and then distributed to the appropriate Emergency Services Provider.   |
| Ireland | All outbound calls to Emergency Services are first screened to determine the current location of the user before being routed to the local PSAP. | 
| Italy | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the PSAP system looks up the address against the number and displays it to the PSAP operator.  |  
| Japan  | Emergency calling is not supported.  |
| Latvia | All outbound calls to Emergency Services are sent to the local PSAP based on the phone number prefix. For non-geo numbers, calls are routed to the national PSAP.  |
| Lithuania | All outbound calls to Emergency Services are sent to the local PSAP based on the phone number prefix.  |
| Luxembourg | All outbound calls to Emergency Services are first screened to determine the current location of the user before being routed to the local PSAP. |
| Netherlands| All outbound calls to Emergency Services are routed to the correct PSAP based on the LAC/first digits of the caller’s number. | 
| New Zealand |  All outbound calls to Emergency Services are first screened to determine the current location of the user before being routed to the local PSAP.  |
| Norway | Emergency calls are routed directly to the PSAP serving the emergency address associated with the number. If no address was provided, the call will be routed based on the old geographic number plan to the nearest emergency center.  |
| Poland  | All outbound calls to Emergency Services are routed to the Local PSAP, and then distributed to the appropriate Emergency Services Provider.   |
| Portugal | All outbound calls to Emergency Services are routed to the correct PSAP based on the LAC/first digits of the caller’s number.  |
| Romania | All outbound calls to Emergency Services are routed to the Local PSAP, and then distributed to the appropriate Emergency Services Provider. All Emergency Calls from a VoIP number are routed to a National Call Center in Bucharest. The National Call Center operator consults with the caller to identify the location and re-route to the Local PSAP.   |
| Singapore | All outbound calls to Emergency Services are routed to the Emergency Call Center based on the number dialed. The Operator requires the caller to provide the Address Information.   |
| Slovakia | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the PSAP system looks up the address against the number and displays it to the PSAP operator.   |
| Slovenia | All outbound calls to Emergency Services are sent to local PSAP based on phone number prefix. For non-geo numbers, calls are routed to the national PSAP. |
| South Africa | All outbound calls to Emergency services are dependent on the address of the caller. All outgoing calls to Emergency Services are routed to the nearest center covering the calling DID area code.  |
| Spain | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the PSAP system looks up the address against the number and displays it to the PSAP operator.   |  
| Sweden | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the Local PSAP system looks up the address against the number and displays it to the PSAP operator. |
| Switzerland | All outbound calls to Emergency Services are dependent on the address of the caller. The address registered to the number is stored in a national EDB. When a call is made to the PSAP with the CLI, the Local PSAP system looks up the address against the number and displays it to the PSAP operator.  |
| United Kingdom | All outbound calls to Emergency Services are first screened to determine the current location of the user before being routed to the local PSAP.  |
| United States | - If a Teams client is located at a tenant-defined dynamic emergency location, emergency calls from that client are automatically routed to the PSAP serving that geographic location. <br><br> - If a Teams client is not located at a tenant-defined dynamic emergency location, emergency calls from that client are screened by a national call center to determine the location of the caller before transferring the call to the PSAP serving that geographic location. <br><br> - If an emergency caller is unable to update their emergency location to the screening center, the call will be transferred to the PSAP serving the caller's registered address.  |

For more information, see:

- [Calling Plans](calling-plan-landing-page.md)
- [Set up Calling Plans](set-up-calling-plans.md)
- [Different kinds of phone numbers used for Calling Plans](different-kinds-of-phone-numbers-used-for-calling-plans.md)
- [Emergency calling terms and conditions](emergency-calling-terms-and-conditions.md)

## Related topics

- [Plan and manage emergency calling](what-are-emergency-locations-addresses-and-call-routing.md)
- [Manage emergency calling policies](manage-emergency-calling-policies.md)
- [Manage emergency call routing policies](manage-emergency-call-routing-policies.md)
- [Plan and configure dynamic emergency calling](configure-dynamic-emergency-calling.md)
- [Microsoft Calling Plans for Teams](calling-plans-for-office-365.md)
