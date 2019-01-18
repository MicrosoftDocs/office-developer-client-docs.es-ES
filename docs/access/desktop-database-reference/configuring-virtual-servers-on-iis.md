---
title: Configuración de servidores virtuales en IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9c7f5782885aafd43e365ddc4f08dedd0975234
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719320"
---
# <a name="configuring-virtual-servers-on-iis"></a>Configuración de servidores virtuales en IIS

**Se aplica a**: Access 2013, Office 2013

Al crear servidores virtuales en Internet Information Services 4.0, los dos pasos adicionales siguientes son necesarios para configurar el servidor virtual para trabajar con RDS:

1.  Al configurar el servidor, marque "Permitir ejecución".

2.  Mueva msadcs.dll a *vroot*\\msadc, donde *vroot* es el directorio principal del servidor virtual.

