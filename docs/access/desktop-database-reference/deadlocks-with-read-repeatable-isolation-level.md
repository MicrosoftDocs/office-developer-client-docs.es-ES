---
title: Interbloqueos con nivel de aislamiento de lectura repetible
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de936da2772b809199d3890140683afd5ef01659
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483920"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="9aae8-102">Interbloqueos con nivel de aislamiento de lectura repetible</span><span class="sxs-lookup"><span data-stu-id="9aae8-102">Deadlocks With Read Repeatable Isolation Level</span></span>


<span data-ttu-id="9aae8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aae8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9aae8-p101">Si un objeto de negocio personalizado usa un nivel de aislamiento de lectura repetible para obtener acceso a un servidor SQL Server, y el objeto de negocio recibe simultáneamente la llamada de dos clientes que envían una consulta y se actualizan en la misma transacción, se puede producir un interbloqueo. El Servicio de datos remotos (RDS) está diseñado de modo que permite que uno de los procesos termine su espera y libere el interbloqueo, aunque se produce un error en la actualización para aquel cliente.</span><span class="sxs-lookup"><span data-stu-id="9aae8-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="9aae8-106">Utilice la propiedad dinámica**Command Time Out** de [Servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md)para modificar la duración del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="9aae8-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

