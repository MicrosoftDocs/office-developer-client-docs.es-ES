---
title: 'Error de servidor de Internet: Acceso denegado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132ecc75c01cdc54eb2d7664227b7abb1578cc2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876543"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="1d7e7-102">Error de servidor de Internet: Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="1d7e7-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="1d7e7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d7e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d7e7-104">Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d7e7-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="1d7e7-105">HTTP\_estado\_denegado 401</span><span class="sxs-lookup"><span data-stu-id="1d7e7-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="1d7e7-106">Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="1d7e7-107">RDS se puede comunicar con un servidor web IIS que se ejecuta en uno de los tres modos de autenticación de contraseña: anónimo, básica o desafío/respuesta de NT (denominado autenticación integrada de Windows en Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="1d7e7-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="1d7e7-108">Además, el servidor web debe tener permisos en el equipo de origen de datos si es un equipo de Windows NT y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

