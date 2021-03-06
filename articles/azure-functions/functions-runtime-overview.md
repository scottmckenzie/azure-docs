---
title: Azure Functions Runtime Overview | Microsoft Docs
description: Overview of the Azure Functions Runtime Preview
services: functions
documentationcenter: ''
author: apwestgarth
manager: stefsch
editor: ''

ms.assetid:
ms.service: functions
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: multiple
ms.topic: article
ms.date: 05/08/2017
ms.author: anwestg
---

# Azure Functions Runtime Overview

The Azure Functions Runtime provides a new way for you to take advantage of the simplicity and flexibility of the Azure Functions programming model on-premises. Built on the same open source roots as Azure Functions, Azure Functions Runtime is deployed on-premises to provide a nearly identical development experience as the cloud service.

![Azure Functions Runtime Preview Portal][1]

The Azure Functions Runtime provides a way for you to experience Azure Functions before committing to the cloud. In this way, the code assets you build can then be taken with you to the cloud when you migrate.  The runtime also opens up new options for you, such as using the spare compute power of your on-premises computers to run batch processes overnight. You can also use devices within your organization to conditionally send data to other systems, both on-premises and in the cloud.

The Azure Functions Runtime consists of two pieces:
* Azure Functions Runtime Management Role
* Azure Functions Runtime Worker Role

## Azure Functions Management Role

The Azure Functions Management Role provides a host for the management of your Functions on-premises. This role performs the following tasks:

* Hosting of the Azure Functions Management Portal, which is the the same one you see in the [Azure portal](https://portal.azure.com). This lets you develop your functions in the same way as you would in the Azure portal.
* Distributing functions across multiple Functions workers.
* Providing a publishing endpoint so that you can publish your functions direct from Microsoft Visual Studio.

## Azure Functions Worker Role

The Azure Functions Worker Roles are deployed in Windows Containers and this is where your function code executes.  You can deploy multiple Worker Roles throughout your organization and is a key way in which customers can make use of spare compute power.

## Minimum Requirements

To get started with the Azure Functions Runtime you must have a machine with **Windows Server 2016 or Windows 10 Creators Update** with access to a **SQL Server** instance.

## Next Steps

Install the [Azure Functions Runtime preview](https://aka.ms/azafr)

<!--Image references-->
[1]: ./media/functions-runtime-overview/AzureFunctionsRuntime_Portal.png
