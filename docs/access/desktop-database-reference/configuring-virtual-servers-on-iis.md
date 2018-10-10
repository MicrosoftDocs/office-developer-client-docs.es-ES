---
title: Configurar servidores virtuales en IIS
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1212a5c7e0761cf9c52a21b5abd67b7dd9841aa0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483735"
---
# <a name="configuring-virtual-servers-on-iis"></a>Configurar servidores virtuales en IIS


**Se aplica a**: Access 2013 | Office 2013

Al crear servidores virtuales en Internet Information Services 4.0, los dos pasos adicionales siguientes son necesarios para configurar el servidor virtual para trabajar con RDS:

1.  Al configurar el servidor, marque "Permitir ejecución".

2.  Mueva msadcs.dll a *vroot*\\msadc, donde *vroot* es el directorio principal del servidor virtual.

