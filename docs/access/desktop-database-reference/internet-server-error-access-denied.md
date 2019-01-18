---
title: 'Error de servidor de Internet: Acceso denegado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720390"
---
# <a name="internet-server-error-access-denied"></a>Error de servidor de Internet: Acceso denegado


**Se aplica a**: Access 2013, Office 2013

Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:

HTTP\_estado\_denegado 401

Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados. RDS se puede comunicar con un servidor web IIS que se ejecuta en uno de los tres modos de autenticación de contraseña: anónimo, básica o desafío/respuesta de NT (denominado autenticación integrada de Windows en Windows 2000). Además, el servidor web debe tener permisos en el equipo de origen de datos si es un equipo de Windows NT y Windows 2000.

