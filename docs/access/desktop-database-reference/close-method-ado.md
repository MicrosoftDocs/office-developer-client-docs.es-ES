---
title: 'Close (método): ActiveX data objects (ADO)'
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296314"
---
# <a name="close-method-ado"></a><span data-ttu-id="0e4e1-102">Método Close (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e4e1-102">Close method (ADO)</span></span>


<span data-ttu-id="0e4e1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e4e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e4e1-104">Cierra un objeto abierto y cualquier objeto dependiente.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e4e1-105">Syntax</span></span>

<span data-ttu-id="0e4e1-106">*object*.Close</span><span class="sxs-lookup"><span data-stu-id="0e4e1-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="0e4e1-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e4e1-107">Remarks</span></span>

<span data-ttu-id="0e4e1-108">Use el método **Close** para cerrar un objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md), [Recordset](recordset-object-ado.md) o [Stream](stream-object-ado.md) para liberar recursos del sistema asociado.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="0e4e1-109">Cerrar un objeto no lo quita de la memoria; puede cambiar su configuración de propiedad y abrirlo más tarde.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="0e4e1-110">Para eliminar completamente un objeto de la memoria, establezca la variable de objeto en *Nothing* (en Visual Basic) después de cerrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="0e4e1-111">**Connection**</span><span class="sxs-lookup"><span data-stu-id="0e4e1-111">**Connection**</span></span>

<span data-ttu-id="0e4e1-p102">El uso del método **Close** para cerrar un objeto **Connection** también cierra cualquier objeto **Recordset** activo asociado con la conexión. Un objeto [Command](command-object-ado.md) asociado con el objeto **Connection** que está cerrando continuará, pero no se asociará con un objeto **Connection**; es decir, su propiedad [ActiveConnection](activeconnection-property-ado.md) se establecerá en **Nothing**. Además, la colección **Parameters** del objeto [Command](parameters-collection-ado.md) no tendrá ningún parámetro definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-p102">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection. A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**. Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="0e4e1-p103">Luego puede llamar al método [Open](open-method-ado-connection.md) para restablecer la conexión al mismo o a otro origen de datos. Mientras que el objeto **Connection** está cerrado, llamar a cualquier método que requiere una conexión abierta al origen de datos genera un error.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-p103">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source. While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="0e4e1-p104">Cerrar un objeto **Connection** mientras hay objetos **Recordset** abiertos en la conexión revierte cualquier cambio pendiente en todos los objetos **Recordset**. Cerrar explícitamente un objeto **Connection** (llamar al método **Close** ) mientras una transacción está en progreso genera un error. Si un objeto **Connection** se va de alcance mientras una transacción está en progreso, ADO automáticamente revierte la transacción.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-p104">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects. Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error. If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="0e4e1-120">**Recordset, Record, Stream**</span><span class="sxs-lookup"><span data-stu-id="0e4e1-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="0e4e1-p105">El uso del método **Close** para cerrar un objeto **Recordset**, **Record** o **Stream** libera los datos asociados y cualquier acceso exclusivo que pudo haber tenido a los datos a través de este objeto particular. Puede luego llamar al método [Open](open-method-ado-recordset.md) para volver a abrir el objeto con los mismos atributos, o modificados.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-p105">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object. You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="0e4e1-123">Mientras un objeto **Recordset** está cerrado, llamar a cualquier método que requiera un cursor activo genera un error.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="0e4e1-p106">Si una modificación está en progreso en modo de actualización inmediata, llamar al método **Close** genera un error; en cambio, llame al método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md) primero. Si cierra el objeto **Recordset** en modo de actualización por lotes, se pierden todos los cambios desde la última llamada [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0e4e1-p106">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first. If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="0e4e1-126">Si usa el método [Clone](clone-method-ado.md) para crear copias de un objeto **Recordset** abierto, cerrar el original o el clon no afecta cualquier otra copia.</span><span class="sxs-lookup"><span data-stu-id="0e4e1-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

