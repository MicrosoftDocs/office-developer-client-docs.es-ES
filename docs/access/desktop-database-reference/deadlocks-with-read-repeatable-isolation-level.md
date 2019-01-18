---
title: Interbloqueos con nivel de aislamiento repetible de lectura
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703779"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="e5a11-102">Interbloqueos con nivel de aislamiento repetible de lectura</span><span class="sxs-lookup"><span data-stu-id="e5a11-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="e5a11-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5a11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5a11-p101">Si un objeto de negocio personalizado usa un nivel de aislamiento de lectura repetible para obtener acceso a un servidor SQL Server, y el objeto de negocio recibe simultáneamente la llamada de dos clientes que envían una consulta y se actualizan en la misma transacción, se puede producir un interbloqueo. El Servicio de datos remotos (RDS) está diseñado de modo que permite que uno de los procesos termine su espera y libere el interbloqueo, aunque se produce un error en la actualización para aquel cliente.</span><span class="sxs-lookup"><span data-stu-id="e5a11-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="e5a11-106">Utilice la propiedad dinámica**Command Time Out** de [Servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md)para modificar la duración del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e5a11-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

