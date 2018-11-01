---
title: Modo inmediato (referencia de escritorio de la base de datos de Access)
TOCTitle: Immediate Mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9448844afa167af3e34e609145ba50d549a9930a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884908"
---
# <a name="immediate-mode"></a><span data-ttu-id="86ee3-102">Modo Inmediato</span><span class="sxs-lookup"><span data-stu-id="86ee3-102">Immediate Mode</span></span>


<span data-ttu-id="86ee3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86ee3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86ee3-p101">El modo inmediato está activo cuando la propiedad **LockType** se ha establecido en **adLockOptimistic** o **adLockPessimistic**. En modo inmediato, los cambios en un registro se propagan al origen de datos en cuanto se declara completo el trabajo en una fila llamando al método **Update**.</span><span class="sxs-lookup"><span data-stu-id="86ee3-p101">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**. In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="86ee3-106">Llamar a Update</span><span class="sxs-lookup"><span data-stu-id="86ee3-106">Calling Update</span></span>

<span data-ttu-id="86ee3-p102">Si se mueve del registro que está agregando o editando antes de llamar al método **Update**, ADO llama automáticamente a **Update** para guardar los cambios. Debe llamar al método **CancelUpdate** antes de desplazarse si desea cancelar los cambios realizados en el registro activo o descartar un registro recién agregado.</span><span class="sxs-lookup"><span data-stu-id="86ee3-p102">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="86ee3-109">El registro activo lo sigue estando después de llamar al método **Update**.</span><span class="sxs-lookup"><span data-stu-id="86ee3-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="86ee3-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="86ee3-110">CancelUpdate</span></span>

<span data-ttu-id="86ee3-p103">Utilice el método **CancelUpdate** para cancelar los cambios realizados en la fila activa o descartar una fila recién agregada. Después de llamar al método **Update**, no se pueden cancelar los cambios en la fila activa o en una nueva fila a menos que dichos cambios sean parte de una transacción que se pueda deshacer con el método **RollbackTrans** o parte de una actualización por lotes. En el caso de una actualización por lotes, puede cancelar la **actualización** con el método **CancelUpdate** o **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="86ee3-p103">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="86ee3-114">Si va a agregar una fila nueva cuando llame al método **CancelUpdate**, la fila activa pasará a ser la fila que estaba activa antes de la llamada a **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="86ee3-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="86ee3-115">Si no ha modificado la fila activa o si no ha agregado ninguna fila nueva, la llamada al método **CancelUpdate** genera un error.</span><span class="sxs-lookup"><span data-stu-id="86ee3-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

