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
# <a name="configuring-virtual-servers-on-iis"></a>Configurar servidores virtuales en IIS

**Se aplica a**: Access 2013, Office 2013

Al crear servidores virtuales en Internet Information Services 4.0, los dos pasos adicionales siguientes son necesarios para configurar el servidor virtual para trabajar con RDS:

1.  Al configurar el servidor, marque "Permitir ejecución".

2.  Mueva msadcs.dll a *vroot*\\msadc, donde *vroot* es el directorio principal del servidor virtual.

