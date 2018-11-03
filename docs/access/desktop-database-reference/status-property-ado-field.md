---
title: Status (propiedad, Field de ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ba5c55e05cb8ab653a296982154bf93e1ffb08d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946261"
---
# <a name="status-property-ado-field"></a><span data-ttu-id="37952-102">Status (propiedad, Field de ADO)</span><span class="sxs-lookup"><span data-stu-id="37952-102">Status property (ADO Field)</span></span>


<span data-ttu-id="37952-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37952-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37952-104">Indica el estado de un objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37952-104">Indicates the status of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="37952-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37952-105">Return value</span></span>

<span data-ttu-id="37952-p101">Devuelve un valor [FieldStatusEnum](fieldstatusenum.md). El valor predeterminado es **adFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="37952-p101">Returns a [FieldStatusEnum](fieldstatusenum.md) value. The default value is **adFieldOK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="37952-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37952-108">Remarks</span></span>

<span data-ttu-id="37952-109">Esta propiedad siempre devuelve **adFieldOK** para los campos de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37952-109">This property always returns **adFieldOK** for fields of a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="37952-p102">Las adiciones y eliminaciones llevadas a cabo en las colecciones [Fields](fields-collection-ado.md) del objeto [Record](record-object-ado.md) se almacenan en caché hasta que se llama al método [Update](update-method-ado.md). La propiedad **Status** permite determinar qué campos se han agregado o eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="37952-p102">Additions and deletions to the [Fields](fields-collection-ado.md) collections of the [Record](record-object-ado.md) object are cached until the [Update](update-method-ado.md) method is called. The **Status** property enables you to determine which fields have been successfully added or deleted.</span></span>

<span data-ttu-id="37952-112">Para mejorar el rendimiento, los cambios de esquema se almacenan en caché hasta que se llama a **Update** y, entonces, se llevan a cabo en una actualización optimista masiva.</span><span class="sxs-lookup"><span data-stu-id="37952-112">To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update.</span></span> <span data-ttu-id="37952-113">Si no se llama al método **Update**, el servidor no se actualiza.</span><span class="sxs-lookup"><span data-stu-id="37952-113">If the **Update** method is not called, the server is not updated.</span></span> <span data-ttu-id="37952-114">Si alguna actualización produce un error, se devuelve un error y la propiedad **Status** indica los valores combinados del código de estado de la operación y el error.</span><span class="sxs-lookup"><span data-stu-id="37952-114">If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code.</span></span> <span data-ttu-id="37952-115">Por ejemplo, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span><span class="sxs-lookup"><span data-stu-id="37952-115">For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span></span> <span data-ttu-id="37952-116">La propiedad **Status** de cada objeto **Field** se puede usar para determinar el motivo por el que no se ha agregado, modificado o eliminado el objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="37952-116">The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted.</span></span> <span data-ttu-id="37952-117">**Estado** sólo forma significativa se expone en el **registro**. Colección de **campos** y no el **conjunto de registros**. Colección de **campos** .</span><span class="sxs-lookup"><span data-stu-id="37952-117">**Status** is only meaningfully exposed on the **Record**.**Fields** collection and not the **Recordset**.**Fields** collection.</span></span>

<span data-ttu-id="37952-p104">A la hora de agregar, modificar o eliminar un objeto **Field** pueden surgir dos problemas. Si el usuario elimina un objeto **Field**, se marca para eliminación en la colección **Fields**. Si el siguiente método **Update** devuelve un error debido a que el usuario ha intentado eliminar un objeto **Field** para el que no tiene permiso, **Field** tendrá un estado **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Al llamar al método [CancelUpdate](cancelupdate-method-ado.md) se restauran los valores originales y se establece **Status** en **adFieldOK**. Del mismo modo, el método **Update** puede devolver un error debido a que se haya agregado un nuevo objeto **Field** y se le haya otorgado un valor inadecuado. En ese caso, el nuevo objeto **Field** se encontrará en la colección **Fields** y tendrá un estado **adFieldPendingInsert** y quizás **adFieldCantCreate**. Es posible proporcionar un valor adecuado para el nuevo objeto **Field** y volver a llamar a **Update**. Tenga en cuenta que llamar a **Resync** en su lugar requiere al proveedor.</span><span class="sxs-lookup"><span data-stu-id="37952-p104">Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.</span></span>

