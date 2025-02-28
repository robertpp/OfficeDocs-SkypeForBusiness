---
title: "Manage phone numbers for your organization"
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: pavellatif
ms.date: 2/27/2025
ms.topic: conceptual
ms.assetid: 6b61cb3c-361c-48a8-a9ef-d81bddde27bb
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
  - Skype for Business
  - Microsoft Teams
ms.localizationpriority: Medium
f1.keywords:
- CSH
ms.custom: 
  - ms.teamsadmincenter.voice.phonenumbers.overview
  - ms.teamsadmincenter.voice.searchandacquire.PSTNpartner
  - ms.lync.lac.NewNumberManualAcquisitionOpenSupportTicket
  - ms.lync.lac.VASAMissingGeoCodes
  - Calling Plans
  - seo-marvel-apr2020
description: Learn how to get and manage user (subscriber) and service (toll and toll-free) telephone numbers for Microsoft Teams for your organization.
---

# Manage telephone numbers for your organization

This article provides an overview for phone number management, including where to get started with acquiring numbers through your specific PSTN connectivity solution, where to manage those numbers and how to assign them to users.

## Planning  

Typical considerations when planning how you will orchestrate delivery of PSTN numbers to your enterprise include answering the following questions:

- Which countries or regions need new telephone numbers?
  - Which PSTN solutions are available in these countries or regions?
    - For Microsoft Teams Calling Plans, see the following article: [Country and region availability for Calling Plans](calling-plan-overview.md)
    - For other PSTN connectivity solutions, see your service provider.
- What use-cases and personas are getting telephone numbers?
  - Could one PSTN solution offer a better user experience than another for the given persona?
    - Example: Teams Phone Mobile may be ideal for field personnel, while Direct Routing may be ideal for remote offices.
- Which type of telephone numbers (subscriber or service) do I need?
  - For Microsoft Teams Calling Plans, see the section: [Considerations for acquiring Microsoft Calling Plan numbers](#considerations-for-acquiring-microsoft-calling-plan-numbers)
  - For other PSTN connectivity solutions, see your service provider.
- How do I port existing telephone numbers?
  - For porting to Microsoft Teams Calling Plans, see the following article: [Port planning](./phone-number-calling-plans/port-order-overview.md)
  - For porting to other service providers, see your service provider.

## Acquiring and managing telephone numbers

How you acquire and manage telephone numbers depends on the option of your Public Switched Telephone Network (PSTN) connectivity solution. Use the following table to navigate to your PSTN solution:

|PSTN connectivity solution |Guidance for acquiring and managing numbers |
|:-----|:-----|
|Microsoft Calling Plan |[Set up telephone numbers with Microsoft Calling Plans](manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md) |
|Operator Connect |[Set up telephone numbers with Operator Connect](operator-connect-configure.md#set-up-phone-numbers) |
|Teams Phone Mobile |[Set up telephone numbers with Teams Phone Mobile](operator-connect-mobile-configure.md#step-2-manage-phone-numbers-and-assign-licenses)|
|Direct Routing |[Set up telephone numbers with Direct Routing](direct-routing-enable-users.md#configure-the-phone-number-and-enable-enterprise-voice) |

## Assigning telephone numbers to users

Once numbers are acquired and available in your tenant, regardless of PSTN connectivity solution, they can be managed in the following interfaces:

- Teams admin center (TAC)
- Teams PowerShell
- On-premises Active Directory (for Direct Routing numbers)

To review more details, see [Manage phone numbers for users](assign-change-or-remove-a-phone-number-for-a-user.md).

### Considerations for acquiring Microsoft Calling Plan numbers

Currently, Microsoft Calling Plan licenses support two telephone number types for resources in your tenant; **user** numbers and **service** numbers.

#### User telephone numbers

[**User numbers**](#user-telephone-numbers), also called subscriber numbers, are numbers that are assigned to users and shared devices in your organization.

There are two categories of user telephone numbers, which can be assigned to users in your organization:  
  
- **Geographic numbers** have a relationship to a geographic area and are the most common. For example, geographic telephone numbers in most cases can only be used within a certain address, city, state, or region of the country/region.

- **Non-geographic numbers** are known as national numbers or sometimes VoIP numbers. These numbers don't have a relationship to a geographic area within a country/region. For example, non-geographic numbers often have the same cost when calling the number from anywhere within the country/region. Also, some countries/regions, such as Denmark, only have non-geographic numbers available.

#### Service numbers

**Service numbers** are numbers that are assigned to services, such as [Audio Conferencing](deploy-audio-conferencing-teams-landing-page.md), [Auto Attendants](plan-auto-attendant-call-queue.md), or [Call Queues](plan-auto-attendant-call-queue.md).

Service numbers have a higher concurrent call capacity than user numbers. Service number availability varies by country/region and the type of number (whether it's a toll or toll-free number). Microsoft’s telephony licenses in each country/region dictate what the number can be used for.

There are two categories of service telephone numbers provided by Microsoft--**toll** and **toll-free**--.

- **Toll service numbers** - There are two types of toll service numbers, which may incur a toll cost to the caller:

  - **Geographic numbers** Geographic numbers have a relationship to a geographic area. For example, geographic telephone numbers in most cases can only be used within a certain address, city, state, or region of the country.

  - **Non-geographic numbers** Non-geographic numbers are national numbers that don't have a relationship to a geographic area within a country/region. For example, non-geographic numbers often have the same cost when calling the number from anywhere within the country/region.

- **Toll-free service numbers** - These service numbers don't typically incur a toll cost to the caller. Teams provides national toll-free numbers in over 60 countries/regions.

> [!CAUTION]
> Some countries/regions and originating number types, such as calls originating from mobile phones, may incur a toll cost to the caller.

If you need additional or other number types other than those numbers seen in the Microsoft Teams admin center, you can submit a telephone number request to the [Phone Number Service Center](https://pstnsd.powerappsportals.com/).

For information about service numbers provided by Operator Connect or Direct Routing, contact your provider.

### Considerations for Direct Routing numbers

Direct Routing phone numbers can be managed in on-premises Active Directory or in Microsoft 365.

#### Direct Routing numbers managed in an on-premises Active Directory

If you have or had a Skype for Business Server hybrid deployment,
your on-premises Active Directory is most likely synchronizing with Microsoft 365. This means that directory attributes on user and resource accounts are managed in the on-premises Active Directory and synchronized into Microsoft 365.

If the Direct Routing phone number is managed on the user or resource account in the on-premises Active Directory, the msRTCSIP-Line parameter on the account contains a value. You can use a tool such as ADSI Edit to view the msRTCSIP-Line parameter for a user or resource account that has a Direct Routing phone number assigned in on-premises Active Directory.

After this parameter is automatically synchronized to the user or resource account in Microsoft 365 through the directory synchronization process (Microsoft Entra Connect), you can view the phone number by looking at the OnPremLineURi parameter in the output from the [Get-CsOnlineUser](/powershell/module/teams/get-csonlineuser) cmdlet.

| Where | Parameter | Value |
| :------------| :-------| :---------|
| On-premises AD | msRTCSIP-Line | tel:+14255551234 |
| Microsoft 365 | OnPremLineURi | tel:+14255551234 |

#### Direct Routing numbers managed in Microsoft 365

If you're not managing Direct Routing phone numbers in the on-premises Active Directory, then they're only managed in Microsoft 365. Because the phone numbers are not synching from on-premises to Microsoft 365, there is no visible value in the OnPremLineUri parameter in the output from the Get-CsOnlineUser cmdlet run for the user or resource account.

You can manage Direct Routing numbers in Microsoft 365 with Teams PowerShell, using the [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) and [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment) cmdlets.

#### Direct Routing numbers managed in both an on-premises Active Directory and Microsoft 365

It's possible to manage Direct Routing phone numbers of some user and resource accounts in an on-premises Active Directory and Direct Routing phone numbers of other accounts in Microsoft 365. This capability depends on whether the attribute msRTCSIP-Line is set on the user or resource account in the on-premises Active Directory.

#### Change where Direct Routing phone numbers are managed

To move management of Direct Routing phone numbers from on-premises Active Directory to Microsoft 365, you need to remove the phone number from the msRTCSIP-Line attribute on the user or resource account in the on-premises Active Directory.

Note that the phone number needs to be re-assigned to the user or resource account in Microsoft 365.

After the removal has been synchronized to Microsoft 365, the OnPremLineUri attribute in the output from Get-CsOnlineUser on the user or resource account will be empty.

For more information, see [Clear Skype for Business attributes for all on-premises users in Active Directory](/skypeforbusiness/hybrid/cloud-consolidation-managing-attributes#method-2---clear-skype-for-business-attributes-for-all-on-premises-users-in-active-directory.md).

## Related articles

- [Set up telephone numbers with Calling Plans](manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md)

- [Set up telephone numbers with Operator Connect](operator-connect-configure.md#set-up-phone-numbers)

- [Set up telephone numbers with Teams Phone Mobile](operator-connect-mobile-configure.md#step-2-manage-phone-numbers-and-assign-licenses)

- [Set up telephone numbers with Direct Routing](direct-routing-enable-users.md#configure-the-phone-number-and-enable-enterprise-voice)

- [Manage phone numbers for users](assign-change-or-remove-a-phone-number-for-a-user.md)

- [Plan Direct Routing](direct-routing-plan.md)

- [Configure Direct Routing](direct-routing-configure.md)
