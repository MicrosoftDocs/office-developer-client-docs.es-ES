---
title: Configurar servidores virtuales en IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8ab3bf8e6ffec2b72744d3abacceb4725c98b02
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946730"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="30f8a-102">Configurar servidores virtuales en IIS</span><span class="sxs-lookup"><span data-stu-id="30f8a-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="30f8a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30f8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30f8a-104">Al crear servidores virtuales en Internet Information Services 4.0, los dos pasos adicionales siguientes son necesarios para configurar el servidor virtual para trabajar con RDS:</span><span class="sxs-lookup"><span data-stu-id="30f8a-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="30f8a-105">Al configurar el servidor, marque "Permitir ejecución".</span><span class="sxs-lookup"><span data-stu-id="30f8a-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="30f8a-106">Mueva msadcs.dll a *vroot*\\msadc, donde *vroot* es el directorio principal del servidor virtual.</span><span class="sxs-lookup"><span data-stu-id="30f8a-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

