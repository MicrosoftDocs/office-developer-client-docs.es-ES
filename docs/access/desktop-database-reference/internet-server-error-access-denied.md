---
title: 'Error de servidor de Internet: Acceso denegado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c874b7a2c4facb9f5969bf9a2150c86773a2687a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603346"
---
# <a name="internet-server-error-access-denied"></a>Error de servidor de Internet: Acceso denegado


**Se aplica a**: Access 2013 | Office 2013

Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:

HTTP\_estado\_denegado 401

<<<<<<< HEAD Asegúrese de que los directorios para obtener acceso a IIS tienen los permisos correctos. RDS se puede comunicar con un servidor web de IIS que se ejecute en cualquiera de los tres modos de autenticación de contraseña: Anónimo, Básico o Desafío/Respuesta de NT (en Windows 2000 se denomina Autenticación de Windows integrada). Además, el servidor web debe tener permisos en el equipo del origen de datos si es un equipo con Windows NT o Windows 2000.
=== Asegúrese de seguro de que los directorios para obtener acceso a IIS tienen los permisos correctos. RDS se puede comunicar con un servidor web IIS que se ejecuta en uno de los tres modos de autenticación de contraseña: anónimo, básica o desafío/respuesta de NT (denominado autenticación integrada de Windows en Windows 2000). Además, el servidor web debe tener permisos en el equipo de origen de datos si es un equipo de Windows NT y Windows 2000.
>>>>>>> master

