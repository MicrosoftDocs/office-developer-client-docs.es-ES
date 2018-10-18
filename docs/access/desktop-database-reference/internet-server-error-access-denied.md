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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="fc59f-102">Error de servidor de Internet: Acceso denegado</span><span class="sxs-lookup"><span data-stu-id="fc59f-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="fc59f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc59f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc59f-104">Si obtiene este error, suele significar que Servicios de Microsoft Internet Information Server (IIS) devolvió el estado siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc59f-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="fc59f-105">HTTP\_estado\_denegado 401</span><span class="sxs-lookup"><span data-stu-id="fc59f-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="fc59f-106"><<<<<<< HEAD Asegúrese de que los directorios para obtener acceso a IIS tienen los permisos correctos.</span><span class="sxs-lookup"><span data-stu-id="fc59f-106"><<<<<<< HEAD Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="fc59f-107">RDS se puede comunicar con un servidor web de IIS que se ejecute en cualquiera de los tres modos de autenticación de contraseña: Anónimo, Básico o Desafío/Respuesta de NT (en Windows 2000 se denomina Autenticación de Windows integrada).</span><span class="sxs-lookup"><span data-stu-id="fc59f-107">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="fc59f-108">Además, el servidor web debe tener permisos en el equipo del origen de datos si es un equipo con Windows NT o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fc59f-108">Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
<span data-ttu-id="fc59f-109">=== Asegúrese de seguro de que los directorios para obtener acceso a IIS tienen los permisos correctos.</span><span class="sxs-lookup"><span data-stu-id="fc59f-109">======= Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="fc59f-110">RDS se puede comunicar con un servidor web IIS que se ejecuta en uno de los tres modos de autenticación de contraseña: anónimo, básica o desafío/respuesta de NT (denominado autenticación integrada de Windows en Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="fc59f-110">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="fc59f-111">Además, el servidor web debe tener permisos en el equipo de origen de datos si es un equipo de Windows NT y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fc59f-111">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
>>>>>>> <span data-ttu-id="fc59f-112">master</span><span class="sxs-lookup"><span data-stu-id="fc59f-112">master</span></span>

