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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="5e334-102">Error de servidor de Internet: Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="5e334-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="5e334-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e334-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e334-104">Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e334-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="5e334-105">ESTADO HTTP \_ \_ DENEGADO 401</span><span class="sxs-lookup"><span data-stu-id="5e334-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="5e334-106">Asegúrese de que los directorios a los que obtiene acceso IIS tienen los permisos apropiados.</span><span class="sxs-lookup"><span data-stu-id="5e334-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="5e334-107">RDS puede comunicarse con un servidor web de IIS que se ejecuta en cualquiera de los tres modos de autenticación de contraseña: Desafío o respuesta anónimo, básico o NT (denominado Autenticación Windows integrada en Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="5e334-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="5e334-108">Además, el servidor web debe tener permisos para el equipo de origen de datos si es un equipo Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5e334-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

