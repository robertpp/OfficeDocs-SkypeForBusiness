---
title: Create and manage meeting themes for Teams meetings
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.date: 3/18/2025
ms.reviewer: margidesai
ms.topic: how-to
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
ms.collection: 
  - M365-collaboration
  - m365initiative-meetings
  - highpri
  - Tier1
appliesto: 
  - Microsoft Teams
f1.keywords:
  - CSH
ms.localizationpriority: medium
search.appverid: MET150
description: Using approved corporate branding assets like images and logos to create custom meeting themes for Teams meetings within your organization.
---

# Create and manage meeting themes for Teams meetings

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Meetings ![Image of a x for no](/office/media/icons/cancel-teams.png)Webinars ![Image of a x for no](/office/media/icons/cancel-teams.png)Town halls

[!INCLUDE[Teams Premium](includes/teams-premium-ecm.md)]

## Overview

Meeting themes include your organization’s brand colors, a custom image, and logo. As an admin, applying a custom theme allows you to customize the visual appearance of the meeting invite, pre-join screen, and lobby for your users' meetings. With the support of your brand management and corporate communications teams, you can easily set up and create meeting themes for various business units and departments within your organization. Meeting themes don't apply to webinars; instead, the webinar registration page is used to configure the webinar's branding for registration and emails.

Only organizers with a Teams Premium license can create meetings that include meeting themes. Anyone who joins these meetings can see the themes, including users in your organization without a Teams Premium license, guests, and anonymous users.

You can set up or manage meeting themes for Teams meetings with the Teams admin center or PowerShell.

:::image type="content" source="media/meeting-themes-edu-small.png" alt-text="Screenshot of Contoso Education's meeting theme featuring their brand logo, image, and colors." lightbox="media/meeting-themes-edu.png":::

> [!IMPORTANT]
> Microsoft doesn't validate the ownership of brand logos or images associated with meeting themes. When your users join meetings with other organizations, they should always verify the authenticity of the organization they're meeting with.

> [!NOTE]
> All meeting participants can see uploaded images and their associated image URL; including external users, guests, unverified users, and anyone with a link to join the meeting. To stop displaying your images, you must delete the images from your meeting theme. To remove images from a meeting theme, navigate to the **Meeting customization policy** in the Teams admin center, select the chosen meeting theme, and select **Delete theme**.

## Prerequisites

Before setting up meeting themes in Teams meetings, check to make sure you have the following items:

- The users who need to use meeting themes have a Teams Premium license.
- You’re an admin with access to the Teams admin center or you have an assigned customization policy.
- Your custom logo, image, and color meet the upload requirements detailed in the following section.

## Upload requirements

Meeting themes display the following visual assets for your theme:

- Logo - Your organization's logo that appears on key surfaces during your meeting, including the lobby screen.
- Custom image - A brand image from your organization (custom images aren't the same as [custom meeting backgrounds](custom-meeting-backgrounds.md)).
- Custom color - We recommend using either your brand's primary or secondary color - whichever one best complements your brand image and logo.

### Logos

We recommend using a square icon style logo with minimal text and the dimensions of 800 x 800 pixels. The logos you upload must comply with Microsoft accessibility contrast ratios (4:5:1) and meet the following requirements:

- PNG and JPEG image formats.
- Two variations of the logo images that appear on the Pre-Join and Lobby UI:
  - Dark theme brand logo
  - Light theme brand logo
- Maximum size of 5 MB.
- Minimum dimension of 576 x 576 pixels.
- You can upload one image per theme from your device.

### Images

We recommend using images with the dimensions of 1,440 x 810 pixels. The custom images you upload must comply with Microsoft accessibility contrast ratios (4:5:1) and meet the following requirements:

- PNG and JPEG image formats.
- Two variations of the brand images that appear on the Pre-Join and Lobby UI:
  - Dark theme brand image
  - Light theme brand image
- Maximum size of 5 MB.
- Dimensions:
  - Minimum dimensions: 1,024 x 574 pixels
  - Maximum dimensions: 3,840 x 2,160 pixels
- You can upload a minimum of 0 and a maximum of one image per theme from your device.

## Create or manage meeting themes in the Teams admin center

All Teams Premium licensed users are automatically assigned the global default policy. Any custom customization policies you create override the global default.

To create or manage meeting themes, follow these steps:

1. Open the Teams admin center.
2. Expand **Meetings** from the navigation pane.
3. Under **Meetings**, select **Customization policies**
4. Either select an existing policy or create a new one.
5. Within your chosen policy, navigate to the **Customize meeting visuals** section.
6. If you're creating a new policy, select the **Add a theme** button to upload your logo, image, and select a custom color. If you're managing an existing policy, select the **Edit meeting themes** button if you'd like to make changes to your theme.
7. In the **Meeting themes** pane, upload your images and create your custom color:

      - **Logo**: Select the **Upload logo** buttons to upload a light and dark version of your logo. These square logos appear on key surfaces during your meeting, including the lobby screen.
      - **Images**: Select the **Upload image** buttons to upload a light and dark version of your custom image. Your organization's images are shown on the meetings screen and provide a colorful backdrop.
      - **Color**: Enter the hex code value of your organization's color, which displays on key surfaces of the meeting experience. To meet accessibility standards, the final color might differ from the color you enter.
8. Select the **Preview** button to see how your theme looks on desktop.
9. Select **Apply**.
10. In the **Custom meeting visuals** table, on your theme's row, toggle the **Currently Active** setting to **Yes**.
11. Select **Save**.
12. Assign the customization policy to specific users or groups.

> [!NOTE]
> Although you can access custom meeting visuals from the meeting policies page, we recommend accessing it through customization policies to avoid navigating through global organizational default policies.

## Add multiple meeting themes to a policy (Public Preview)

Adding multiple themes to each policy gives your organizers more options, allowing them to select the appropriate branding for different meetings. You can upload a maximum of 5 themes to each policy.

To add multiple meeting themes to a policy, follow these steps:

1. Open the Teams admin center.
2. Expand **Meetings** from the navigation pane.
3. Under **Meetings**, select **Customization policies**
4. Select an existing policy.
5. Within your chosen policy, navigate to the **Customize meeting visuals** section.
6. Select the **Add new meeting theme theme** button to create extra themes. You should give each theme a descriptive name.
7. In the **Meeting themes** pane, upload your images and create your custom color. You can also select logos and images you previously uploaded.

      - **Logo**: Select the **Upload logo** buttons to upload a light and dark version of your logo. These square logos appear on key surfaces during your meeting, including the lobby screen.
      - **Images**: Select the **Upload image** buttons to upload a light and dark version of your custom image. Your organization's images are shown on the meetings screen and provide a colorful backdrop.
      - **Color**: Enter the hex code value of your organization's color, which displays on key surfaces of the meeting experience. To meet accessibility standards, the final color might differ from the color you enter.
8. Select the **Preview** button to see how your theme looks on desktop.
9. Select **Apply**.
10. In the **Custom meeting visuals** table, on your theme's row, toggle the **Currently Active** setting to **Yes**.
11. Repeat steps 6-10 to add more themes to the policy.
12. Select **Save**.

## Allow organizers to turn off meeting themes for a meeting

You can give meeting organizers the option to turn off meeting themes for specific meetings. When organizers turn off meeting themes, the meeting reverts to the default Teams theme.

To allow your meeting organizers to turn off meeting themes:

1. Navigate to the **Meeting customization policy**.
1. Toggle the **Allow organizer to control meeting theme** setting to **On**.

Meeting organizers can turn off meeting themes by:

1. Navigating to the **Meeting options** menu for a meeting.
1. Toggling the **Meeting theme** meeting option to **Off**.

> [!NOTE]
>
> - For recurring meetings or series, the meeting option applies for every instance of the meeting.
> - Meeting themes aren't disabled for meetings that are in-progress. To apply changes, your users must end the call and restart the meeting.

## Manage meeting themes in PowerShell

 To upload images, you must use the Teams admin center. You can manage meeting themes by using the following PowerShell cmdlets in Teams PowerShell:

- [Set-CsTeamsMeetingBrandingPolicy](/powershell/module/teams/set-csteamsmeetingbrandingpolicy)
- [Grant-CsTeamsMeetingBrandingPolicy](/powershell/module/teams/grant-csteamsmeetingbrandingpolicy)
- [New-CsTeamsMeetingBrandingPolicy](/powershell/module/teams/new-csteamsmeetingbrandingpolicy)

This example assigns a meeting theme policy called 'Policy Test' to a group named group@contoso.com.

```PowerShell
Grant-CsTeamsMeetingBrandingPolicy -Group group@contoso.com -PolicyName "Policy Test" -Rank 1
```

This example assigns a meeting theme policy called 'Policy Test' to a user named alice@contoso.com.

```PowerShell
Grant-CsTeamsMeetingBrandingPolicy -identity " alice@contoso.com" -PolicyName "Policy Test"
```

You can assign meeting customization policies to users or groups with a Teams Premium license in your organization.

## Where are meeting themes visible

Supported clients:

- Desktop client
- Web client (Meeting themes aren't currently supported on Safari or Firefox)
- Android (Versions 11+ only)
- iOS

> [!NOTE]
> Images aren't visible on mobile clients.

|  Asset type       | Join Launcher | Meeting Pre-Join | Meeting Lobby | Meeting Stage | Meeting invite |
| :---:          |     :---:      |         :---:  |         :---:  |         :---:  |       :---:  |
| **Logo**   | Yes | Yes| Yes| No| Yes |
| **Image**     | Yes | Yes| Yes| No| No |
| **Color**     | Yes | Yes| Yes| Yes| No |

> [!NOTE]
> Logos added to the meeting theme override any logos you upload to meeting invitations. To learn more about meeting invitations, see [Customize meeting invitations](customize-meeting-invitations.md).
> [!NOTE]
> If your users edit a meeting invite with Teams calendar after sending it, the logo might not appear when they resend the invite.

## Who can view a meeting theme

While only licensed users who are assigned a meeting customization policy can create meeting themes-enabled meetings, anyone can view the themes that are applied to a meeting. These users include:

- Teams Premium licensed users in your organization
- Users in your organization that don't have a Teams Premium license
- Guests
- External Users
- Anonymous users

## Best practices for meeting themes

- Only use your organization's official image assets. Don't use image content that you don't own.
- Work with your brand and marketing team to ensure that your image assets and colors together follow your organization's brand guidelines.
- Ensure you're using high-quality logo images, which are visible on small and large screen devices.
- Colors generated in the Teams App might differ from your brand colors. This process was created to ensure Microsoft Accessibility Standards are met.
- Users with high-contrast device settings can't see meeting themes.

### Accessibility

Here are a few points to ensure accessibility requirements are met:

- Follow existing UI patterns and structure – The current structure and text on the screen aren’t being modified with this feature.
- Image Contrast Ratio – Image assets are required to meet the 4:5:1 color contrast ratio.
- Accessible Color Generation Support – We calculate the accessible color output that is the closest match to the brand color input while maintain Microsoft Accessibility standards.
- High Contrast support – For users with high contrast settings enabled, branding doesn't apply. They continue to see the default Teams meeting experience.
- Controls – You and your organizers can prevent users with accessibility concerns from seeing the branding through:
  - Policies – To ensure users with accessibility concerns don't create branding-enabled meetings, avoid assigning them a customization policy.
  - Meeting Options – Meeting organizers can turn off themes for a meeting if a user with accessibility concerns joins their meeting.

## Use cases for multiple departments or business units in one organization

Some organizations have multiple business units under different brand identities within the same organization. In these cases, you can create meeting customization policies that are dedicated to each brand. They can also assign a department or business unit user group to a specific policy.

Contoso Ltd. has a single organization in Microsoft Teams, with everyone in their organization's user profiles across different business organizations. The company is looking to adopt custom branded meetings in Teams to increase their brand presence with their clients and encourage an internal corporate culture.

Contoso has two business units (BUs) under their organization: Contoso Technical Services and Contoso Education. Both BUs have their own distinct brand imagery, and want to display their branding during their internal and external meetings.

To support this use case, Contoso's admins can create two distinct customization policies:

- Policy A - Contoso Technical Services – houses Contoso Technical Service’s brand logo, image, and color.
- Policy B - Contoso Education – houses Contoso Education’s brand logo, image, and color.

They can proceed to assign the licensed users in Contoso Technical Services to Policy A, and licensed users of Contoso Education to Policy B.

:::image type="content" source="media/meeting-themes-tech-services-small.png" alt-text="Screenshot of policy A, Contoso Technical Services' meeting theme featuring their brand logo, image, and colors." lightbox="media/meeting-themes-tech-services.png":::

## Related topics

- [Teams Premium meetings customization options](custom-meetings-overview.md)
- [IT Admins- Manage and create custom meeting backgrounds for Teams meetings](custom-meeting-backgrounds.md)
- [Overview of custom meeting templates in Microsoft Teams](custom-meeting-templates-overview.md)
