---
template: post
title: Monitor Office 365/Microsoft 365 License Usage
subtitle: Monitor available licenses. Trigger alerts when thresholds met
date: 2020-12-09T18:00:00Z
thumb_img_path: ''
content_img_path: ''
excerpt: Monitor available Office 365/Microsoft 365 licenses using Powershell and
  Azure Automation

---
A script to monitor the number of available licenses in your Office 365 environment and generate email alerts when the licenses fall below a specified threshold.

Prerequisites:

An Azure Automation account.

An Office 365 user account to query license information and send email alerts.

**Create the Azure Automation account**

Go to portal.azure.com and search for "Automation Accounts"

Click Add.

Enter a name for the automation account

Select a subscription and resource group

Select a location

Create Azure Run As Account: Yes (this will create a service principal with the contributor role in your subscription)

Click Create

**Store the Office 365 user account in Azure Automation**

Go to the newly created Automation Account

![](/images/screenshot-portal-azure-com-1608476623606.png)

Under Shared Resources, click Credentials

Click "Add Credential"

Enter the following information:

Name

Username

password

confirm password

Click Create

![](/images/screenshot-portal-azure-com-1608477077768.png)

The Script