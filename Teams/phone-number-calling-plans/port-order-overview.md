---
title: What's a port order?
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: mikedav, roykuntz, jastark, leiaglezer
ms.date: 01/22/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
audience: Admin
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords: 
  - CSH
ms.custom: 
  - ms.teamsadmincenter.voice.phonenumbers.porting.overview
  - Calling Plans
description: Overview of port orders and planning for the transfer phone numbers from your service provider to Teams.
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
---

# What's a port order? - Planning to transfer telephone numbers to Teams

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Microsoft Calling Plans

Number porting is the process of transferring your existing phone numbers from one service provider to another, allowing you to keep the same phone numbers even after changing service providers.

You might have a scenario where you want to transfer numbers from your current service provider to Microsoft, so that they can be used with Microsoft Teams Calling Plans.

To do this, you need to create and submit a "port order."

You originate your port order with Microsoft and Microsoft manages the port order fulfillment with your current service provider while becoming the service provider of record for your phone numbers.

When the numbers are ported over, you can assign those phone numbers to your users and services such as audio conferencing (for conference bridges), auto attendants, and call queues.
  
After you port your phone numbers over to your Microsoft Teams Calling Plan, Microsoft becomes your service provider and you can disconnect your service with your old service provider or carrier.

This article provides considerations and guidance for planning and ensuring a successful number port project when [Submitting a port request](transfer-phone-numbers-to-teams.md).
  
## Information required for a port request

While service providers perform number porting in accordance with regulatory protocols, each has their own systems and processes that are unique to each of them.

Furthermore, the regulatory requirements for number porting vary between countries/regions. To ensure successful port order fulfillment, you must provide thorough details about your existing service and supply regulatory forms specific to the respective country or region.

> [!IMPORTANT]
> The success of your port request depends on the accuracy of the information that you provide to Microsoft when you create your port request.

### Port glossary and information to have ready when submitting a port request

Most of the information that you enter in Microsoft's port order request can be found on a recent invoice or official document of record from your current service provider.

Depending upon the country or region of the port request, you might also need to know additional information, which can come from country/region specific documents.

An example of the terms and definitions that are used in the porting process and that you'll encounter when submitting a port order with Microsoft, follows:

These terms are applicable in the United States and alternative terms might be used in other countries or regions.

- **List of phone numbers that you want to port**
  - Make sure that the list of numbers that you want to port aren't already with Microsoft, or part of another open port order.
  - Ports from multiple service providers require multiple port orders

- **Account Number**
  - The account number associated with the phone numbers that you're trying to port.
  - If you're currently invoiced through a reseller, you'll provide the name of the reseller in the Letter of Authorization.
  - All phone numbers in a port request using the Teams admin center (TAC) MUST belong to the same account number. See [Port request considerations](#port-request-considerations)

- **Authorizing person on account**
  - A person in your organization who is the authorized user on your account with your current service provider.

- **Service address**
  - The service address associated with the phone numbers that you want to port.
  - The service address could be different than the billing address with your current service provider.
  - All phone numbers in a port request using the Teams admin center MUST belong to the same service address.

- **Business name**
  - The business name associated with the phone numbers that you want to port.
  - All phone numbers in a port request MUST have the same business name.

- **Billing Telephone Number (BTN)**
  - The billing telephone number associated with the phone numbers that you want to port. This BTN must be on the same account as the numbers that you want to port.
  - Your current service provider has this information.
  - All phone numbers in a port request using the Teams admin center MUST have the same BTN.

- **Partial Port**
  - This means that you're only porting some of the numbers from your account with your current service provider.
  - As an example, if you have 10 numbers on your account with your current service provider, and you're porting six of them, then that means that your port is considered as a partial port.

- **Full Port**
  - This means that your current port request (that you're working to submit) includes ALL of the phone numbers from your account with your current service provider.
  - As an example, if you have 10 numbers on your account with your current service provider, and you're porting all 10 numbers, then that means that your port is considered a full port.

## Port request considerations

The following sections provide considerations for planning a port request.

### Countries or regions that support number porting to Microsoft Teams Calling Plans

You can port numbers for all countries or regions where Microsoft Teams Calling Plans are offered.

To see if Microsoft Teams Calling Plans are available for a country or region, reference [Microsoft Teams Calling Plans](../calling-plans-for-office-365.md) and [Manage phone numbers for your organization](../manage-phone-numbers.md).

Additionally, the Teams admin center's number [porting wizard](transfer-phone-numbers-to-teams.md) only displays countries where Microsoft Teams Calling Plans are available.

### Numbers eligible for porting

In general, you can transfer any phone number that's from a supported provider.

**You can transfer:**

- Land-line phone numbers
- Mobile phone numbers
- VoIP phone numbers
- Toll phone numbers
- Toll-free phone numbers
- Service phone numbers such as those used for conference bridges, auto attendants, etc.
- Fax numbers, but they can't be used for faxing. They have to be assigned to a user. If you port the phone number to Teams, you can assign this phone number to a user in your organization instead of using it for faxing.
- If you're porting hybrid phone numbers (migrating from Direct Routing or Operator Connect to Calling Plans), contact the [TNS service desk](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md) and include a note stating these phone numbers are hybrid.

Transferring mobile numbers to Microsoft Calling Plan is only available in the United States, Puerto Rico, and Canada.

User numbers can be converted to service numbers, and vice versa, but not during the port process. Once a number is ported to Microsoft, the usage type can be changed. See [Managing the usage type of a Calling Plan number](../manage-the-usage-of-a-phone-number.md).

**You can't transfer:**

- Phone numbers used for data connections like for DSL lines or broadband Internet connections
- Universal International Freephone Numbers (UIFN)
- Phone numbers dedicated to faxing
  - If you have existing dedicated phone numbers that must continue to support faxing, consider an alternative solution. You can transfer these numbers over to Teams but your fax services won't continue to work. Faxing services aren't available to Teams customers through the licenses for Phone System or any Microsoft Calling Plan.
- Any phone number or numbers that aren't from a supported country or region, including phone numbers from a VoIP phone provider.

Porting availability for Toll-free phone numbers vary by country and region. For more information, please refer to your country or region specific documents to see available support for porting service.

> [!NOTE]
> At this time in the United Kingdom, Microsoft currently doesn't support transferring UK nongeographic numbers including shared cost numbers for area codes 0843, 0844, 0845, 0870, 0871, 0872.

### How many port requests do I need?

A single port order request in the Teams admin center can support multiple telephone numbers, but those phone numbers must have the same service provider, same account number, same BTN, same number type, and same service address.

The following porting scenarios require multiple port orders:

- **Ports with multiple service providers** - A number port wizard request supports porting from one service provider at a time. For example, if you have a site whose numbers you want to port over to Microsoft, and some of those phone numbers are provided by service provider "A" while other numbers are provided by service provider "B," then you place two separate port requests with the number port wizard, one for numbers with service provider "A" and another for numbers with service provider "B."
- **Ports with multiple billing telephone numbers** - A number port wizard request supports porting numbers from one BTN at a time. For example, if your service provider groups your telephone numbers within multiple BTNs, then you need to place a separate port request for each set of numbers, respective to their parent BTN.
- **Ports with multiple number types** - A number port wizard request supports porting one number type at a time. For example, if you have a site that has nine toll numbers assigned to individual users, and one toll-free number is used as an auto attendant, then you need to place two separate port requests with the number port wizard, one for the nine toll numbers and another for the toll-free number.
- **Ports with multiple addresses** - A number port wizard request supports porting numbers for one service address at a time. For example, if you have a port project to transfer numbers at multiple addresses on the same port date, then you'll need to place a separate port request per unique service address.

> [!NOTE]
> If you aren't sure if your numbers are from the same service provider, account, or type, you can try running the wizard and listing the phone numbers you want to port. If the wizard detects different groupings, it lists the unique categories.
>
> For complex number port projects, involving multiple service providers, accounts/BTNs, number types, or service addresses, follow the [Manually submitting a port request](manually-submit-port-order.md) guidance to create a manual **Port in** request.

### Large port requests

If you have a large port request of 1,000 numbers or greater, you must bypass the number port wizard in the Teams admin center and submit your port order manually with the Telephone Number Services (TNS) - Service Desk. For more information, see [Manually submitting a port request](manually-submit-port-order.md).

### Full-port and partial-port orders

When you're submitting a port order request, you can request to transfer all the numbers in the account or some of them.

A **full-port** is when you transfer all of the numbers from your current service provider to Teams.

- For example, your account BTN is +1 425-555-1234 and this account has 25 numbers. You want to port all 25 phone numbers (+1 425-555-1235 through 1259). When you list your numbers to port, you enter: +14255551234 - +14255551259.
  - In this case, all numbers in the account are included in the list of numbers to port (including the BTN), so this example is a full-port.

A **partial-port** is when you transfer some of the numbers from your current service provider to Teams.

- For example, your account BTN is +1 425-555-1234 and this account has 25 numbers. You want to port only five of your 25 phone numbers (+1 425-555-1235 through 1259). When you list your numbers to port, you enter: +1 425 555 1235 - +1 425 555 1239.
  - In this case, you're leaving some numbers with your current service provider and transferring some numbers to Microsoft Calling Plan, so this example is a partial-port.

> [!NOTE]
> In a partial port, if the BTN isn't one of the numbers you're porting, then you don't include the BTN in the list of numbers to port. If the BTN is one of the numbers you're porting, then you can select one of the remaining numbers that you aren't porting to become the new BTN for the service provider's account.

### How port requests are processed

Port requests for the same account number are only processed *one at a time*, in series. Singular port order processing is an industry standard with all service providers. If you submit multiple port requests, one after the other, involving the same account number, all to occur simultaneously or even in overlapping timeframes, the service provider that currently owns the phone numbers only processes the first request per account number and rejects all others. If you submit more than one request for the same account number, all at the same time, then the losing carrier rejects one or all of your port requests.

For example, you have account number xyz123 with your current service provider with the following plans:

- Account xyz123 has 10 telephone numbers (TNs) under it: TN1, TN2, TN3, ... TN10.
- Assume you want to port these numbers in 2 batches
  - Batch 1 - TN1, TN2, TN3, TN4, TN5
    - This is a partial-port, with BTN remaining with current provider.
  - Batch 2 - TN6, TN7, TN8, TN9, TN10
    - This is full-port, including the BTN.

In this example, you can't submit port requests for Batch 1 and Batch 2 at the same time. You need to place a port request for Batch 1, wait for that request to be completed, and only then submit a port request for Batch 2.

### When to disconnect your existing phone lines with your current service provider

Don't arrange to disconnect the service with your current service provider before submitting your port request.

- Inactive or disconnected numbers can't be ported. Given the chance that a port might be rejected, don't arrange any service terminations with your current service provider until all of your porting activity is complete.
- In a full port, the service with your current service provider might be terminated automatically, but it's best practice to work with the service provider to audit and ensure account closure.
- Any other services (like ISDN/Broadband etc.) associated with your porting phone numbers is automatically disconnected after the port is completed. If you would like to keep these services active with your current service provider, transfer those services to phone numbers that you don't plan to port to Microsoft Teams Calling Plans.

### What happens after you submit a port order request

In a number porting process, the gaining service provider (the phone service provider that you want to port your numbers to) raises a port request on behalf of you and this request is sent to the losing service provider (the phone service provider that currently owns the phone numbers that you're trying to port).

The losing carrier processes the port request and responds by either approving or rejecting the request.

When placing a port request, you're asked to choose a target porting date and time. Choosing a target date doesn't mean that the port happens on that date - the port only occurs on the target date if the losing service provider provides approval to allow your numbers to be ported away from their system on the date that you asked for. For more information on porting date planning, see [Plan for port event date](#plan-for-port-event-date) in this article.

Once you submit your request to port your phone numbers to Microsoft, the following events take place:

- Microsoft takes your request and submits it to the service provider that currently owns your phone numbers (the losing service provider).
  - Microsoft submits your port request to the losing service provider, based on their business rules.
- Once a port request reaches the losing service provider, they have a window of time to process the request and provide a response.
  - The response SLA varies by country or region. For example, the losing service provider response SLA in the United States is 3-5 business days, and 5-7 business days in Canada.

> [!NOTE]
> Microsoft has no say in the port approval decision and can't influence the behavior of the losing service provider.

The losing carrier then approves or denies the port request.

- **Approval**:
  - The losing service provider responds to Microsoft, acknowledging compliance with the request, which is known as a **firm order commitment** (FOC).
    - In rare cases, a losing service provider can override any firm order commitment that they sent.
  - On the date of the firm order commitment, the losing service provider releases their numbers to Microsoft, and Microsoft directs the numbers to your tenant.

- **Rejection**:
  - In their response to us, the losing service provider indicates reasons for rejecting the port request.
  - In a rejected port request, the losing carrier stops processing that request until the request is fixed resubmitted.
    - Upon resubmitting an updated port request to the losing carrier, the response SLA is reset and starts over.

  > [!NOTE]
  > In a port order rejection, a losing service provider doesn't provide the expected, correct information to Microsoft. Only the categorical reason for the rejection is provided to Microsoft. If corrected information is required, you need to work directly with your losing service provider to investigate.

### Common mistakes

Number porting is easy to do. However, if the order is incomplete, inaccurate, or missing information, your current service provider will reject the port request.
Here are the most common mistakes Microsoft sees customers making when they port numbers.

- Make sure the account information you give matches exactly what your phone carrier has on record. Mismatched information is the most common cause of errors and delays to your port order. Verify the following information is true:
  - Name or person authorized to make changes to the account is correct.
  - Address is correct.
  - Account number is correct.
  - BTN is correct and included in the list of phone numbers that you're porting.
- Make sure there are no advanced call control features, for example, Call Hunt, Distinctive Ring, or other routing features, that are enabled on these phone numbers.
  - If there are advanced call control features enabled with your current service provider, arrange to have those features disabled before the number port.
- Make sure you don't have open service orders or disconnects pending with your current service provider.
- Make sure all numbers are from the same service provider and the same account.
- Make sure your service is active. Freezing the account prevents number ports. The person authorized to make changes to the account must submit an order to the current service provider to remove the freeze. This process can take one to three weeks depending on the service provider.

## Planning a number port event

Each country or region has unique names for the documents that their service providers use as the official document of record for a customer.

In the United States, the service provider's official document of record for a customer is the Customer Service Record, or CSR. In Canada, the same document is called an Equipment Record.

Browse through the following reference articles to find if the countries in your scope use official documents of record and what they're called:

> [!div class="op_single_selector"]
>
> - [Australia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-australia)
> - [Austria](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-austria)
> - [Belgium](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-belgium)
> - [Canada](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-canada)
> - [Czech Republic](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-czech-republic)
> - [Denmark](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-denmark)
> - [Estonia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-estonia)
> - [Finland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-finland)
> - [France](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-france)
> - [Germany](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-germany)
> - [Hong Kong](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-hong-kong)
> - [Hungary](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-hungary)
> - [Ireland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-ireland)
> - [Italy](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-italy)
> - [Japan](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-japan)
> - [Latvia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-latvia)
> - [Lithuania](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-lithuania)
> - [Luxembourg](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-luxembourg)
> - [Mexico](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-mexico)
> - [New Zealand](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-new-zealand)
> - [Norway](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-norway)
> - [Poland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-poland)
> - [Portugal](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-portugal)
> - [Romania](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-romania)
> - [Singapore](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-singapore)
> - [Slovakia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-slovakia)
> - [Slovenia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-slovenia)
> - [South Africa](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-south-africa)
> - [Spain](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-spain)
> - [Sweden](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-sweden)
> - [Switzerland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-switzerland)
> - [Netherlands](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-netherlands)
> - [United Kingdom](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-u-k)
> - [United States & Puerto Rico](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-u-s)

The official document of record is a document that you can and should request from your current phone service provider.

- This document contains information about your account and helps you confirm that you're creating a port request with information that matches the service provider's records.
- You can ask your service provider for the document of record at any time. It doesn't need a port request associated with it.
- In case your current service provider isn't able to provide an official document of record, you can ask them to confirm the Information to have ready when submitting a port request

**Collect and complete the documents for the country or region where you are porting numbers.**

> [!NOTE]
> If you're using the number port wizard in the Teams admin center to submit your port request, you don't need to write the numbers you're porting in the Letter of Authorization document, as the numbers are captured when you list them in the wizard.

### Remove any freeze on your current account

Some service providers support placing accounts on a 'freeze' status, to protect the account from unauthorized port activity.

If there's a freeze on your account, your port order is rejected, so confirm your account's status with the service provider. If frozen, remove the freeze before submitting your port order.

### Plan lead-time for port request processing

After submitting your port order request, it typically takes between 7-14 days to be processed, start to finish. Depending on your current service provider, it might take up to 30 days. After the phone numbers are ported over, you'll get an email from Microsoft's Telephone Number Services team to let you know about next steps.

To check the status of your port order, in the left navigation of the Microsoft Teams admin center, go to **Voice** > **Phone numbers**, and then select **Order history**. Each port order status is listed in the Status column.

- In the US, a minimum five-day lead time is required.
- In Canada, a minimum ten-day lead time is required.
- For requests over 200 phone numbers, expect additional time.

> [!NOTE]
> You can't choose a target porting date that is further than 30 (calendar) days out.

### Plan for port event date

When it comes to choosing your target porting date, you can choose an aggressive or conservative target date. Each comes with its own advantages and disadvantages.

#### Approach 1: Choosing an aggressive target date

With the aggressive target date approach, you choose a target date that is only a few business days away from your date of submission. Any target date less than seven business days away (US) / 10 business days away (Canada) from your date of submission can be considered an aggressive target date.

The upside of this is that if all the information in your port request is accurate, and if the losing carrier can process your request in time, then your ports can be completed quickly.

However, the downside of this approach is that you're basically choosing speed over predictability.

- If your port request receives a rejection from the losing carrier, it's almost certain that a new target port date is required and the response time that the losing carrier is reset.
- This means that you now have to recommunicate the status of your project with your end users and your stakeholders and replan day-of-port activities, often at the last minute.

#### Approach 2: Choosing a conservative target date

With the conservative target date approach, you choose a target date that is at least 15 business days away from your date of submission.

When compared to Approach 1, the downside here's that your ports take longer to complete.

However, the upside is that this approach builds in some buffer time in case Microsoft's Telephone Number Services team runs into rejections and enables us to have higher confidence that the numbers port on your initial requested target date. While your ports do take longer, you don't have to deal with the hassle of recommunicating with your stakeholders and replanning your day-of-port activities.

With Approach 2, you're choosing predictability over speed.

Microsoft recommends Approach 2 for all your ports.

### Plan for port event to process during business hours

Service providers (including your current phone service provider and Microsoft) process port requests during business hours only.

With most service providers in all countries and regions where Microsoft offers Calling Plans, business hours are 9am to 5pm, in the time zone that their porting team is located.

For United States user numbers, you can choose any target porting time between 8am (U.S. Eastern Time) to 8pm (U.S. Eastern Time).

For Canada numbers, including user and Toll-Free numbers, and for USA Toll-Free numbers, port times are scheduled at 11:30am (U.S. Eastern Time). If an earlier time is required, a special request can be submitted through the [Telephone Number Services - Service Desk](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md).

- Choosing a target time late in the business day means that if something goes wrong and Microsoft's Telephone Number Services team needs the help of the losing service provider to resolve the issue, you could have a scenario where Microsoft must wait until the next business day for the issue to be resolved. For example, some service provider porting teams are only available until 5pm (Eastern Time) for support.

## Related topics

- [What's the status of your port orders?](port-order-status.md)
- [Different kinds of phone numbers used for Calling Plans](../different-kinds-of-phone-numbers-used-for-calling-plans.md)
- [Manage phone numbers for your organization](../manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md)
- [Emergency calling terms and conditions](../emergency-calling-terms-and-conditions.md)
- [Emergency Calling disclaimer label](https://download.microsoft.com/download/9/9/0/990e24c1-eb49-4b52-9306-dbd4c864ed91/emergency-calling-label-(en-us)-(v.1.0).zip)
