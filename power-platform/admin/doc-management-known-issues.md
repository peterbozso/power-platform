---
title: "Known issues with document management | MicrosoftDocs"
description: "Learn about known issues with document management"
keywords: encrypt
ms.date: 10/15/2019
ms.service: powerapps
ms.custom: 
ms.topic: article
applies_to: 
  - PowerApps
ms.assetid: 
author: Mattp123
ms.author: matp
manager: kvivek
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
topic-status: Drafting
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - Powerplatform
---

# Known issues with document management
The customizations and configurations described here can cause issues with the document management feature. 

## Components from an Iframe
Opening a component from an Iframe in an entity form from a Unified Interface app will not succeed. For example, loading the **Document Associated Grid** for an entity form in an Iframe loads the grid in the Iframe but users will not be able to interact with the document records from the grid. 

## Third-party solutions that modify Document Management folders 
Deploying third-party solutions that modify the folders used with the document management feature can cause unexpected behavior. 
Examples include the following: 
- Creation of entity record level SharePoint folders. 
- Renaming of previously auto-created entity record level SharePoint folders.
- Moving previously auto-created entity record level SharePoint folders to another location.

## Document location for child entities
Documents of a child entity only appear in the parent documents folder when the parent document location has been created. To create the location, navigate to the **Documents** tab of the parent record. If no such location is created, child documents will not appear in the parent entity folder. Once the location is created, child documents will begin to appear in the parent entity folder.

## Document folder location for multiple lookups
If the entity selected for the **Based on entity** folder structure has two lookups, documents will not be stored inside the entity folder, but will be stored in the root folder. For example, if the **Based on entity** folder structure is set to **Account**, and you have an entity with two lookup accounts, such as **Work Order**, the documents related to **Work Orders** will not be stored inside any account document location, but will be stored in the root folder.

### See also
[Troubleshooting server-based authentication](troubleshooting-server-based-authentication.md) <br />
[Troubleshoot SharePoint integration](troubleshoot-set-up-sharepoint-online.md)