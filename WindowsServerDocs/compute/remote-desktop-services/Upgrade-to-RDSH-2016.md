---
title: Upgrading your Remote Desktop Session Host to Windows Server 2016 
description: This article describes how to upgrade your existing Remote Desktop Services deployments to Windows Server 2016.
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: 
  - remote-desktop-services
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c9b98b8-4eca-4a39-b10b-2bac729f7f44
author: spatnaik
manager: scottman
---
# Upgrading your Remote Desktop Session Host to Windows Server 2016

>Applies To: Windows Server Technical Preview

> [!IMPORTANT]
> All applications must be uninstalled before the upgrade and reinstalled after the upgrade to avoid any app compatibility issues that may rise because of the upgrade.

## Supported OS upgrades with RDS role installed
Upgrades to Windows Server 2016 are supported only from Windows Server 2012 R2 and Windows Server 2016 TP5.

## Upgrading a RDS session-based collection
In order to keep the down-time to a minimum, it is best to follow the steps below while upgrading a RDS session-based collection:

1. Identify the servers to be upgraded, say, half the servers in the deployment.
2. Prevent new connections to these servers by setting **Allow New Connections** to false.
3. Log off all sessions on these servers. 
4. Remove these servers from the collection.
5. Upgrade the servers to Windows Server 2016.
6. Add the upgraded servers back to their corresponding collections.
7. Now upgrade the remaining servers in the deployment by following steps 2 through 6 above.

## Upgrading a standalone RD Session Host server
A standalone RD Session Host server can be upgraded anytime.