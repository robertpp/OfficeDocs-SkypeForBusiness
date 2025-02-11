---
title: Set up Classwork in Teams for Education
author: MicrosoftHeidi
ms.author: heidip
manager: jtremper
ms.topic: article
ms.service: msteams
audience: admin
ms.collection: 
  - M365-collaboration
  - tier3
search.appverid: MET150
ms.date: 12/18/2024
f1.keywords:
description: The Classwork feature in Teams for Education allows educators to create and organize class resources.
ms.localizationpriority: medium
appliesto: 
  - Microsoft Teams
---

# Set up Classwork in Teams for Education

The Classwork feature in Teams for Education allows educators to create and organize class resources, including Assignments, OneNote Class Notebook pages, web links, files, and Teams channels. With Classwork, educators can curate a view of content and resources that will help students navigate a class and see everything in one place.

[Learn more about Classwork Teams for Education](https://support.microsoft.com/topic/8a7f61e2-09ef-4fc9-8c16-c0e1a07166dd#ID0EBD=Manage_course_content).

### Permission support

For details about delegated and application permissions, see [Permission types](/graph/permissions-overview). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

#### EduCurricula.Read

| Category | Application | Delegated |
|--|--|--|
| Identifier | - | 484859e8-b9e2-4e92-b910-84db35dadd29 |
| DisplayText | - | Read the user's class modules and resources |
| Description | - | Allows the app to read the user's modules and resources on behalf of the signed-in user. |
| AdminConsentRequired | - | Yes |

---

#### EduCurricula.Read.All

| Category | Application | Delegated |
|--|--|--|
| Identifier | 6cdb464c-3a03-40f8-900b-4cb7ea1da9c0 | - |
| DisplayText | Read all class modules and resources | - |
| Description | Allows the app to read all modules and resources, without a signed-in user. | - |
| AdminConsentRequired | Yes | - |

---

#### EduCurricula.ReadWrite

| Category | Application | Delegated |
|--|--|--|
| Identifier | - | 4793c53b-df34-44fd-8d26-d15c517732f5 |
| DisplayText | - | Read and write the user's class modules and resources |
| Description | - | Allows the app to read and write user's modules and resources on behalf of the signed-in user. |
| AdminConsentRequired | - | Yes |

---

#### EduCurricula.ReadWrite.All

| Category | Application | Delegated |
|--|--|--|
| Identifier | 6a0c2318-d59d-4c7d-bf2e-5f3902dc2593 | - |
| DisplayText | Read and write all class modules and resources | - |
| Description | Allows the app to read and write all modules and resources, without a signed-in user. | - |
| AdminConsentRequired | Yes | - |

### Remove Classwork for a specific user or your entire tenant

To remove Classwork for an individual user, go to the **Teams Admin Center** and navigate to **Teams apps** > **Permission policies** to create a new app permission policy definition. When creating the new policy definition, set the **Microsoft apps** policy to **Block specific apps and allow all others** and add **Classwork** to the list of blocked applications. Once your new policy definition is saved, assign it to the appropriate users.

To remove Classwork for your entire tenant, go to **Teams Admin Center**, navigate to **Teams apps** > **Manage apps**, and search for and select **Classwork** from the application list. Change the status setting within the application's settings page to **Blocked**.

