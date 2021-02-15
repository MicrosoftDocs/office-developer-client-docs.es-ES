---
title: Propiedad InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291244"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="d4a40-102">Propiedad InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="d4a40-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="d4a40-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4a40-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4a40-104">Indica el número de milisegundos que se debe esperar antes de que una solicitud exceda el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="d4a40-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d4a40-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d4a40-105">Settings and return values</span></span>

<span data-ttu-id="d4a40-106">Establece o devuelve un valor de tipo **Long** que representa el número de milisegundos antes de que una solicitud exceda el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="d4a40-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4a40-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4a40-107">Remarks</span></span>

<span data-ttu-id="d4a40-108">Esta propiedad se aplica sólo a solicitudes enviadas mediante los protocolos HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d4a40-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="d4a40-p101">Las solicitudes de un entorno de tres niveles pueden tardar varios minutos en ejecutarse. Use esta propiedad para especificar tiempo adicional para aquellas solicitudes de ejecución larga.</span><span class="sxs-lookup"><span data-stu-id="d4a40-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

