---
title: Tipos de bloqueos (referencia de base de datos de escritorio de Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47b212be1922f783889f1e5be436a616909dc5c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314164"
---
# <a name="types-of-locks"></a><span data-ttu-id="a2f37-102">Tipos de bloqueos</span><span class="sxs-lookup"><span data-stu-id="a2f37-102">Types of locks</span></span>


<span data-ttu-id="a2f37-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2f37-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="a2f37-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="a2f37-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="a2f37-p101">Indica actualizaciones optimistas por lotes. Se requiere para el modo de actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="a2f37-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span>

<span data-ttu-id="a2f37-p102">Muchas aplicaciones recuperan muchas filas a la vez y deben efectuar, a continuación, actualizaciones coordinadas que incluyen el conjunto completo de filas que se van a insertar, actualizar o eliminar. Con cursores por lotes, sólo es necesario un viaje de ida y vuelta al servidor, mejorando así el rendimiento de la actualización y reduciendo el tráfico de red. Mediante el uso de una biblioteca de cursores por lotes puede crear un cursor estático y, a continuación, desconectar del origen de datos. En este punto, puede realizar cambios en las filas y, posteriormente, volver a conectarse y enviar los cambios al origen de datos en un lote.</span><span class="sxs-lookup"><span data-stu-id="a2f37-p102">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted. With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic. Using a batch cursor library, you can create a static cursor and then disconnect from the data source. At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="a2f37-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="a2f37-111">adLockOptimistic</span></span>

<span data-ttu-id="a2f37-p103">Indica que el proveedor utiliza bloqueo optimista, bloqueando registros sólo cuando se llama al método **Update**. Es decir, existe una posibilidad de que los datos los pueda modificar otro usuario entre el instante en que se modificó el registro y el momento en que se llama a **Update**, algo que crea conflictos. Utilice este tipo de bloqueo en situaciones en las que son pocas las posibilidades de que se produzca un conflicto o cuando los conflictos se puedan resolver fácilmente.</span><span class="sxs-lookup"><span data-stu-id="a2f37-p103">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method. This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts. Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="a2f37-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="a2f37-115">adLockPessimistic</span></span>

<span data-ttu-id="a2f37-p104">Indica un bloqueo pesimista, registro por registro. El proveedor realiza las acciones necesarias para garantizar la modificación correcta de los registros, normalmente bloqueando los registros en el origen de datos inmediatamente antes de la modificación. Por supuesto, esto significa que los registros no están disponibles para otros usuarios una vez que se empieza a modificar hasta que se libera el bloqueo llamando a **Update**. Utilice este tipo de bloqueo en un sistema donde no se pueden permitir cambios concurrentes en los datos (por ejemplo, un sistema de reservas).</span><span class="sxs-lookup"><span data-stu-id="a2f37-p104">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing. Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.** Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="a2f37-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="a2f37-120">adLockReadOnly</span></span>

<span data-ttu-id="a2f37-p105">Indica registros de sólo lectura. No es posible alterar los datos. Un bloqueo de sólo lectura es el tipo de bloqueo "más rápido", ya que no requiere que el servidor mantenga un bloqueo sobre los registros.</span><span class="sxs-lookup"><span data-stu-id="a2f37-p105">Indicates read-only records. You cannot alter the data. A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="a2f37-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="a2f37-124">adLockUnspecified</span></span>

<span data-ttu-id="a2f37-125">No especifica ningún tipo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a2f37-125">Does not specify a type of lock.</span></span>

