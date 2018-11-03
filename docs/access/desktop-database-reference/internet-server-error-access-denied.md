---
title: 'Error en servidor Internet: acceso denegado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 885bdc14e5d5d346a17e018a509acf5b6c52108d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944882"
---
# <a name="internet-server-error-access-denied"></a>Error en servidor Internet: acceso denegado


**Se aplica a**: Access 2013, Office 2013

Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:

HTTP\_estado\_denegado 401

Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados. RDS se puede comunicar con un servidor web IIS que se ejecuta en uno de los tres modos de autenticación de contraseña: anónimo, básica o desafío/respuesta de NT (denominado autenticación integrada de Windows en Windows 2000). Además, el servidor web debe tener permisos en el equipo de origen de datos si es un equipo de Windows NT y Windows 2000.

