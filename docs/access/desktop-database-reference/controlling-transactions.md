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
# <a name="controlling-transactions"></a><span data-ttu-id="0129c-102">Controlar transacciones</span><span class="sxs-lookup"><span data-stu-id="0129c-102">Controlling Transactions</span></span>


<span data-ttu-id="0129c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0129c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0129c-104">Una *transacción* delimita el principio y el final de una serie de operaciones de acceso a datos que ocurren durante una conexión.</span><span class="sxs-lookup"><span data-stu-id="0129c-104">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection.</span></span> <span data-ttu-id="0129c-105">Dependiendo de las funcionalidades transaccionales de un origen de datos, el objeto **Connection** también permite crear y administrar transacciones.</span><span class="sxs-lookup"><span data-stu-id="0129c-105">Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions.</span></span> <span data-ttu-id="0129c-106">Por ejemplo, si utiliza el proveedor de Microsoft OLE DB para SQL Server para tener acceso a una base de datos en Microsoft SQL Server 2000, puede crear varias transacciones anidadas para los comandos que ejecute.</span><span class="sxs-lookup"><span data-stu-id="0129c-106">For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="0129c-107">ADO garantiza que los cambios en un origen de datos resultantes de operaciones en una transacción se producen correctamente en conjunto o no en absoluto.</span><span class="sxs-lookup"><span data-stu-id="0129c-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="0129c-p102">Si cancela la transacción o si se produce un error en una de sus operaciones, el resultado final será equivalente a que no se haya producido ninguna de las operaciones en la transacción. El origen de datos se mantendrá igual que antes de que se iniciase la transacción.</span><span class="sxs-lookup"><span data-stu-id="0129c-p102">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred. The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="0129c-110">El modelo de objetos ADO no incluye transacciones explícitamente, pero las representa con un conjunto de métodos de objetos **Connection** (**BeginTrans**, **CommitTrans** y **RollbackTrans**).</span><span class="sxs-lookup"><span data-stu-id="0129c-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="0129c-111">Para obtener más información acerca de transacciones, vea el [Capítulo 5: Actualizar y almacenar datos.](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="0129c-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

