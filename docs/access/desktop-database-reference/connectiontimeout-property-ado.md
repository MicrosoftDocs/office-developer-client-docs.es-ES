---
title: ConnectionTimeout (propiedad, ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab98e60e88a9685f138262a59a83f2b311c636da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890935"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="6e5eb-102">ConnectionTimeout (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6e5eb-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="6e5eb-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e5eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e5eb-104">Indica el tiempo que se va a esperar durante el establecimiento de una conexión para que finalice el intento y se genere un error.</span><span class="sxs-lookup"><span data-stu-id="6e5eb-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6e5eb-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6e5eb-105">Settings and return values</span></span>

<span data-ttu-id="6e5eb-p101">Establece o devuelve un valor de tipo **Long** que indica, en segundos, el tiempo que se va a esperar a que se abra la conexión. El valor predeterminado es 15.</span><span class="sxs-lookup"><span data-stu-id="6e5eb-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open. Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e5eb-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e5eb-108">Remarks</span></span>

<span data-ttu-id="6e5eb-p102">Use la propiedad **ConnectionTimeout** en un objeto [Connection](connection-object-ado.md) si, debido a demoras en el tráfico de red o la sobrecarga del servidor, es preciso abandonar un intento de establecer conexión. Si transcurre el tiempo especificado por la propiedad **ConnectionTimeout** antes de que se abra la conexión, se genera un error y ADO cancela el intento. Si la propiedad tiene el valor cero, ADO esperará indefinidamente a que se abra la conexión. Asegúrese de que el proveedor en el que está escribiendo código admite la funcionalidad **ConnectionTimeout**.</span><span class="sxs-lookup"><span data-stu-id="6e5eb-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="6e5eb-113">La propiedad **ConnectionTimeout** es de lectura y escritura cuando está cerrada la conexión, y es de sólo lectura cuando la conexión está abierta.</span><span class="sxs-lookup"><span data-stu-id="6e5eb-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

