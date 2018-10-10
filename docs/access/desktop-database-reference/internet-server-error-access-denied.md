---
title: 'Error de servidor de Internet: Acceso denegado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db78b6f2c51e2e5df918622043e33abc6bc9e674
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484573"
---
# <a name="internet-server-error-access-denied"></a>Error de servidor de Internet: Acceso denegado


**Se aplica a**: Access 2013 | Office 2013

Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:

HTTP\_estado\_denegado 401

Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados. RDS se puede comunicar con un servidor web de IIS que se ejecute en cualquiera de los tres modos de autenticación de contraseña: Anónimo, Básico o Desafío/Respuesta de NT (en Windows 2000 se denomina Autenticación de Windows integrada). Además, el servidor web debe tener permisos en el equipo del origen de datos si es un equipo con Windows NT o Windows 2000.

