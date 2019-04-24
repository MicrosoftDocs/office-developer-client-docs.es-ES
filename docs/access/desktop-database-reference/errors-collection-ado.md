---
title: Errors (colección) (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293430"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="e1c48-102">Errors (colección) (ADO)</span><span class="sxs-lookup"><span data-stu-id="e1c48-102">Errors collection (ADO)</span></span>


<span data-ttu-id="e1c48-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1c48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1c48-104">Contiene todos los objetos [Error](error-object-ado.md) creados en respuesta a un error relacionado con un único proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1c48-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c48-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1c48-105">Remarks</span></span>

<span data-ttu-id="e1c48-p101">Toda operación que implique a objetos de ADO puede generar errores relacionados con el proveedor. Cuando se produce alguno de estos errores, se pueden colocar objetos **Error** en la colección **Errors** del objeto [Connection](connection-object-ado.md). Cuando otra operación ADO genera un error, se borra la colección **Errors** y el nuevo conjunto de objetos **Error** se puede colocar en la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="e1c48-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="e1c48-p102">Cada objeto **Error** representa el error de un proveedor específico, no un error de ADO. Los errores de ADO se exponen al mecanismo de control de excepciones en tiempo de ejecución. Por ejemplo, en Microsoft Visual Basic, la generación de un error específico de ADO desencadenará un evento [onError](onerror-event-rds.md) y aparecerá el objeto **Err**.</span><span class="sxs-lookup"><span data-stu-id="e1c48-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="e1c48-p103">Las operaciones ADO que no generan un error no afectan a la colección **Errors**. Use el método [Clear](clear-method-ado.md) para borrar manualmente la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="e1c48-p103">ADO operations that don't generate an error have no effect on the **Errors** collection. Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="e1c48-p104">El conjunto de objetos **Error** de la colección **Errors** describe todos los errores que se han producido en respuesta a una única instrucción. La enumeración de los errores específicos en la colección **Errors** permite que las rutinas de tratamiento de errores determinen de forma más precisa la causa y el origen de un error, y sigan los pasos apropiados para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="e1c48-p104">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement. Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="e1c48-p105">Algunos métodos y propiedades devuelven advertencias que aparecen como objetos **Error** en la colección **Errors** pero que no detienen la ejecución de un programa. Antes de llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) en un objeto [Recordset](recordset-object-ado.md), antes de llamar al método [Open](open-method-ado-connection.md) en un objeto **Connection**, o antes de establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset**, llame al método **Clear** en la colección **Errors**. De este modo, podrá leer la propiedad [Count](count-property-ado.md) de la colección **Errors** y comprobar si hay advertencias devueltas.</span><span class="sxs-lookup"><span data-stu-id="e1c48-p105">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="e1c48-119">[!NOTA] Para obtener una explicación más detallada de cómo una única operación ADO puede generar varios errores, vea el tema sobre el objeto **Error**.</span><span class="sxs-lookup"><span data-stu-id="e1c48-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


