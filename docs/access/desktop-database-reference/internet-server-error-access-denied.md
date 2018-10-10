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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="e2a48-102">Error de servidor de Internet: Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="e2a48-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="e2a48-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2a48-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e2a48-104">Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:</span><span class="sxs-lookup"><span data-stu-id="e2a48-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="e2a48-105">HTTP\_estado\_denegado 401</span><span class="sxs-lookup"><span data-stu-id="e2a48-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="e2a48-p101">Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados. RDS se puede comunicar con un servidor web de IIS que se ejecute en cualquiera de los tres modos de autenticación de contraseña: Anónimo, Básico o Desafío/Respuesta de NT (en Windows 2000 se denomina Autenticación de Windows integrada). Además, el servidor web debe tener permisos en el equipo del origen de datos si es un equipo con Windows NT o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e2a48-p101">Make sure the directories accessed by IIS have proper permissions. RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000). Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

