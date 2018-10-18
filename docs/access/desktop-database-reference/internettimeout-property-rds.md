---
title: InternetTimeout (propiedad, RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd0fdc8f64207e1233ac56812ef009da865ce01a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603465"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="05147-102">InternetTimeout (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="05147-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="05147-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05147-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05147-104">Indica el número de milisegundos que se debe esperar antes de que una solicitud exceda el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="05147-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

<span data-ttu-id="05147-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="05147-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="05147-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="05147-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="05147-107">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="05147-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="05147-108">master</span><span class="sxs-lookup"><span data-stu-id="05147-108">master</span></span>

<span data-ttu-id="05147-109">Establece o devuelve un valor de tipo **Long** que representa el número de milisegundos antes de que una solicitud exceda el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="05147-109">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="05147-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05147-110">Remarks</span></span>

<span data-ttu-id="05147-111">Esta propiedad se aplica sólo a solicitudes enviadas mediante los protocolos HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="05147-111">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="05147-p101">Las solicitudes de un entorno de tres niveles pueden tardar varios minutos en ejecutarse. Use esta propiedad para especificar tiempo adicional para aquellas solicitudes de ejecución larga.</span><span class="sxs-lookup"><span data-stu-id="05147-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

