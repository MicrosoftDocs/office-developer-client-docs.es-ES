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
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Interbloqueos con nivel de aislamiento de lectura repetible


**Se aplica a**: Access 2013 | Office 2013

Si un objeto de negocio personalizado usa un nivel de aislamiento de lectura repetible para obtener acceso a un servidor SQL Server, y el objeto de negocio recibe simultáneamente la llamada de dos clientes que envían una consulta y se actualizan en la misma transacción, se puede producir un interbloqueo. El Servicio de datos remotos (RDS) está diseñado de modo que permite que uno de los procesos termine su espera y libere el interbloqueo, aunque se produce un error en la actualización para aquel cliente.

Utilice la propiedad dinámica**Command Time Out** de [Servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md)para modificar la duración del tiempo de espera.

