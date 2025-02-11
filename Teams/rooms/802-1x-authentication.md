---  
title: "Implementing 802.1x Authentication for Microsoft Teams Rooms on Windows"  
author: mstonysmith
ms.author: tonysmit  
manager: pamgreen
ms.reviewer: dimehta 
ms.date: 01/16/2025  
ms.topic: article
audience: Admin
ms.service: msteams
ms.subservice: itpro-rooms
appliesto: 
  - Microsoft Teams
ms.collection: 
  - M365-collaboration
  - teams-rooms-devices
  - Tier1
ms.localizationpriority:  medium
ms.custom: QuickDraft  
search.appverid: MET150  
f1.keywords: 
  - NOCSH
ai-usage: ai-assisted
description: This article serves as a comprehensive guide to assist you in configuring and implementing 802.1x authentication for Microsoft Teams Rooms.
---  

# Implementing 802.1x Authentication for Microsoft Teams Rooms on Windows

For customers looking to implement 802.1x in network environments especially Zero Trust networks, Microsoft Teams Rooms for Windows offers support similar to that of other Windows devices. This article outlines the necessary steps for setting up and deploying 802.1x authentication.

> [!IMPORTANT]
> 802.1x authentication is currently not supported on Teams Rooms for Android. Verify your Android device's support for 802.1x on wired connections with your Teams Rooms device OEM.

## Prerequisites

Before you begin, ensure that your network devices and AAA/RADIUS server are enabled for 802.1x LAN authentication. Configuration details vary depending upon your chosen vendor for these solutions. 802.1x is currently not supported on Teams Rooms for Android due to the lack of support for LAN profiles in Intune for Android. Refer to your device manufacturer to verify that your device can operate in a 802.1x LAN environment.

## Steps to Configure 802.1x Authentication

The following steps assume a ground up configuration to enable 802.1x for your Teams Rooms devices. Review these steps carefully and only implement those items applicable to your network.

### Step 1: Enable 802.1x LAN Authentication

Ensure that your network devices and AAA/RADIUS server are enabled for 802.1x LAN authentication. Configuration details vary depending on your chosen vendor for these solutions.

### Step 2: Configure Intune for Certification Distribution and Authentication

Use a PKCS certificate profile to provision devices with certificates in Microsoft Intune. For detailed instructions, refer to [Use a PKCS certificate profile to provision devices with certificates in Microsoft Intune](/mem/intune/protect/certificates-pfx-configure).

### Step 3: Create a Wired Network Profile within Intune

Configure 802.1x wired network settings for macOS and Windows devices in Microsoft Intune. For detailed instructions, refer to [Configure 802.1x wired network settings for macOS and Windows devices in Microsoft Intune](/mem/intune/configuration/wi-fi-settings-windows).

### Step 4: Enroll Your Teams Rooms Devices to Intune

Ensure your Teams Rooms devices are enrolled in Intune. For detailed instructions, refer to [Enrolling Microsoft Teams Rooms on Windows devices with Microsoft Endpoint Manager](https://techcommunity.microsoft.com/t5/microsoft-teams/enrolling-microsoft-teams-rooms-on-windows-devices-with-microsoft/ba-p/1744120).

### Step 5: Configure EAP on Your Teams Rooms on Windows

Configure Extensible Authentication Protocol (EAP) on your Teams Rooms on Windows. For detailed instructions, refer to [Configure EAP profiles and settings in Windows](/windows-server/networking/technologies/extensible-authentication-protocol/configure-eap-profiles?tabs=netsh-wifi%2Cpowershell-vpn%2Csettings-wifi%2Cgroup-policy-wifi).

With these steps in place, your 802.1x environment and Teams Rooms on Windows devices will be configured to ensure your Teams Rooms devices are managed and identified on your network.

## Related Articles

- [Troubleshooting PKCS certificate deployment in Intune](/troubleshoot/mem/intune/certificates/troubleshoot-pkcs-certificate-profiles)
- [Configure 802.1x wired network settings for macOS and Windows devices in Microsoft Intune](/mem/intune/configuration/wired-networks-configure)
- [Enrolling Microsoft Teams Rooms on Windows devices with Microsoft Endpoint Manager](https://techcommunity.microsoft.com/t5/microsoft-teams/enrolling-microsoft-teams-rooms-on-windows-devices-with-microsoft/ba-p/1744120)