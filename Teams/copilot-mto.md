---
title: Manage Copilot access for B2B members within multitenant organizations (MTO) in Teams
ms.date: 12/30/2024
author: DaniEASmith
ms.author: danismith
manager: jtremper
ms.reviewer: sadafbadar
ms.topic: article
audience: admin
ms.service: msteams
ms.tgt.pltfrm: cloud
ms.localizationpriority: medium
search.appverid: MET150
f1.keywords:
- NOCSH
ms.collection: 
  - M365-collaboration
  - magic-ai-copilot
ms.custom:
  - admindeeplinkTEAMS
appliesto: 
  - Microsoft Teams
description: Learn how to manage B2B members' access within Multitenant Organization (MTO) for Copilot features in Teams.
---

# Manage Copilot access for B2B members within multitenant organizations (MTO) in Teams

> [!IMPORTANT]
> The support discussed in this article is only available to B2B members within the multitenant organization. It isn't available to external or federated users.

Copilot in Teams enhances users’ day-to-day work with features like AI-generated summaries in chats and suggested action items after a meeting. Microsoft now supports **B2B member access** to Copilot in Teams for licensed users in multitenant organizations to ensure they never lose access to Copilot’s benefits in Team channels and meetings.

**B2B member access** lets people in your org collaborate with members of other organizations in an external Microsoft Entra organization. This access is done by using Microsoft Entra External ID for business-to-business (B2B) collaboration and granting member-level access to Teams channels, meetings, and other resources in your org. For more information about B2B collaboration, see [B2B collaboration](/entra/external-id/user-properties).

> [!NOTE]
> B2B member access is possible only when both organizations allow access to and from each other. Therefore, you need to coordinate with the external organization’s admin to make sure their cross-tenant access settings allow sharing with you. For more information about cross-tenant access settings, see [Overview: Cross-tenant access with Microsoft Entra External ID](/entra/external-id/cross-tenant-access-overview).

Teams admins can toggle off and on the **Allow Copilot for B2B members** setting in the Teams admin center or with PowerShell. This setting is turned on by default, allowing external members from other organizations who have Copilot licenses to use Copilot when they join meetings hosted by your organization.

## Manage B2B member access to Copilot in the Teams admin center

1. Sign in to the [Teams admin center](https://go.microsoft.com/fwlink/p/?linkid=2066851) using your admin credentials.
1. Expand **Users** from the left-side navigation pane.
1. Under **Users**, select **B2B member access**.
1. Either select an existing policy or create a new one.
1. Toggle the **Allow Copilot for B2B members** setting **On** or **Off**.
1. Select the **Save** button.

## Manage B2B member access to Copilot using PowerShell

The **Allow Copilot for B2B members** setting can also be managed using PowerShell with the [Get-CsTeamsMultiTenantOrganizationConfiguration](/powershell/module/teams/get-csteamsmultitenantorganizationconfiguration) and [Set-CsTeamsMultiTenantOrganizationConfiguration](/powershell/module/teams/set-csteamsmultitenantorganizationconfiguration) cmdlets.

To learn how to manage Teams settings using PowerShell, see [Manage Teams with Microsoft Teams PowerShell](teams-powershell-managing-teams.md).

### Sample scripts

Retrieve your multitenant organization’s Teams configuration by using the following code:

```powershell
Get-CsTeamsMultiTenantOrganizationConfiguration 
```

Turn off the **Allow Copilot for B2B members** setting by using the following code:

```powershell
Set-CsTeamsMultiTenantOrganizationConfiguration -Identity Global -CopilotFromHomeTenant Disabled  
```

Turn on the **Allow Copilot for B2B members** setting by using the following code:

```powershell
Set-CsTeamsMultiTenantOrganizationConfiguration -Identity Global -CopilotFromHomeTenant Enabled  
```

## Related articles

- [B2B direct connect Microsoft Entra overview](/entra/external-id/b2b-direct-connect-overview)
- [Multitenant organization capabilities in Microsoft Entra ID](/entra/identity/multi-tenant-organizations/overview)
