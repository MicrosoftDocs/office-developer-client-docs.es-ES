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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291258"
---
# <a name="internet-server-error-access-denied"></a>Error de servidor de Internet: Acceso denegado


**Se aplica a:** Access 2013, Office 2013

Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:

ESTADO HTTP \_ \_ DENEGADO 401

Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados. RDS puede comunicarse con un servidor web de IIS que se ejecute en cualquiera de los tres modos de autenticación de contraseña: Anónimo, Básico o Desafío/Respuesta de NT (denominado Autenticación integrada de Windows en Windows 2000). Además, el servidor web debe tener permisos en el equipo de origen de datos si es un equipo con Windows NT/Windows 2000.

