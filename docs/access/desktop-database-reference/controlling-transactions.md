---
title: Controlar transacciones
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4acd03e387f50d9035c73dd2fef934f6fd6985a5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889647"
---
# <a name="controlling-transactions"></a>Controlar transacciones


**Se aplica a**: Access 2013, Office 2013

Una *transacción* delimita el principio y el final de una serie de operaciones de acceso a datos que ocurren durante una conexión. Dependiendo de las funcionalidades transaccionales de un origen de datos, el objeto **Connection** también permite crear y administrar transacciones. Por ejemplo, si utiliza el proveedor de Microsoft OLE DB para SQL Server para tener acceso a una base de datos en Microsoft SQL Server 2000, puede crear varias transacciones anidadas para los comandos que ejecute.

ADO garantiza que los cambios en un origen de datos resultantes de operaciones en una transacción se producen correctamente en conjunto o no en absoluto.

Si cancela la transacción o si se produce un error en una de sus operaciones, el resultado final será equivalente a que no se haya producido ninguna de las operaciones en la transacción. El origen de datos se mantendrá igual que antes de que se iniciase la transacción.

El modelo de objetos ADO no incluye transacciones explícitamente, pero las representa con un conjunto de métodos de objetos **Connection** (**BeginTrans**, **CommitTrans** y **RollbackTrans**).

Para obtener más información acerca de transacciones, vea el [Capítulo 5: Actualizar y almacenar datos.](chapter-5-updating-and-persisting-data.md).

