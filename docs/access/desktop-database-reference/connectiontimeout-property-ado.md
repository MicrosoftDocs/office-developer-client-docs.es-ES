---
title: Propiedad ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295705"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="b0b96-102">Propiedad ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="b0b96-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="b0b96-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0b96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0b96-104">Indica el tiempo que se va a esperar durante el establecimiento de una conexión para que finalice el intento y se genere un error.</span><span class="sxs-lookup"><span data-stu-id="b0b96-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b0b96-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b0b96-105">Settings and return values</span></span>

<span data-ttu-id="b0b96-106">Establece o devuelve un valor de tipo **Long** que indica, en segundos, el tiempo que se va a esperar a que se abra la conexión.</span><span class="sxs-lookup"><span data-stu-id="b0b96-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="b0b96-107">El valor predeterminado es 15.</span><span class="sxs-lookup"><span data-stu-id="b0b96-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b96-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0b96-108">Remarks</span></span>

<span data-ttu-id="b0b96-p102">Use la propiedad **ConnectionTimeout** en un objeto [Connection](connection-object-ado.md) si, debido a demoras en el tráfico de red o la sobrecarga del servidor, es preciso abandonar un intento de establecer conexión. Si transcurre el tiempo especificado por la propiedad **ConnectionTimeout** antes de que se abra la conexión, se genera un error y ADO cancela el intento. Si la propiedad tiene el valor cero, ADO esperará indefinidamente a que se abra la conexión. Asegúrese de que el proveedor en el que está escribiendo código admite la funcionalidad **ConnectionTimeout**.</span><span class="sxs-lookup"><span data-stu-id="b0b96-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="b0b96-113">La propiedad **ConnectionTimeout** es de lectura y escritura cuando está cerrada la conexión, y es de sólo lectura cuando la conexión está abierta.</span><span class="sxs-lookup"><span data-stu-id="b0b96-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

