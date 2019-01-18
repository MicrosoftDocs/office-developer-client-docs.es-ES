---
title: Update (método, ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710639"
---
# <a name="update-method-ado"></a><span data-ttu-id="fa415-102">Update (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="fa415-102">Update method (ADO)</span></span>

<span data-ttu-id="fa415-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa415-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa415-104">Guarda los cambios realizados en la fila actual de un objeto [Recordset](recordset-object-ado.md) o la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fa415-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa415-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa415-105">Syntax</span></span>

<span data-ttu-id="fa415-106">*conjunto de registros*. Actualizar los*campos*, *valores*</span><span class="sxs-lookup"><span data-stu-id="fa415-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="fa415-107">*registro*.</span><span class="sxs-lookup"><span data-stu-id="fa415-107">*record*.</span></span> <span data-ttu-id="fa415-108">*Los campos*. Actualización</span><span class="sxs-lookup"><span data-stu-id="fa415-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="fa415-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa415-109">Parameters</span></span>

|<span data-ttu-id="fa415-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fa415-110">Parameter</span></span>|<span data-ttu-id="fa415-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa415-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fa415-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="fa415-112">*Fields*</span></span> |<span data-ttu-id="fa415-p102">Es opcional. **Variant** que representa un solo nombre, o bien, matriz de tipo **Variant** que representa los nombres o las posiciones ordinales del campo o de los campos que se van a modificar.</span><span class="sxs-lookup"><span data-stu-id="fa415-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="fa415-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="fa415-115">*Values*</span></span> |<span data-ttu-id="fa415-p103">Es opcional. **Variant** que representa un solo valor, o bien, matriz de tipo **Variant** que representa los valores del campo o de los campos en el registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="fa415-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fa415-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa415-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="fa415-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="fa415-119">Recordset</span></span>

<span data-ttu-id="fa415-p104">Use el método **Update** para guardar los cambios efectuados en el registro actual de un objeto **Recordset** desde la llamada al método [AddNew](addnew-method-ado.md) o desde el cambio de alguno de los valores de campo de un registro existente. El objeto **Recordset** debe ser compatible con las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="fa415-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="fa415-122">Para establecer los valores de campo, siga uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="fa415-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="fa415-123">Asigne valores a la propiedad [Value](field-object-ado.md) de un objeto [Field](value-property-ado.md) y llame al método **Update**.</span><span class="sxs-lookup"><span data-stu-id="fa415-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="fa415-124">Pase un nombre de campo y un valor como argumentos con la llamada a **Update**.</span><span class="sxs-lookup"><span data-stu-id="fa415-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="fa415-125">Pase una matriz de nombres de campo y una matriz de valores con la llamada a **Update**.</span><span class="sxs-lookup"><span data-stu-id="fa415-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="fa415-p105">Cuando utiliza matrices de campos y valores, debe haber el mismo número de elementos en ambas matrices. Además, el orden de los nombres de campo debe coincidir con el orden de los valores de campo. Si no coinciden el número ni el orden de los campos y valores, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="fa415-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="fa415-p106">Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llama al método [UpdateBatch](updatebatch-method-ado.md). Si está modificando el registro actual o agregando un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir al proveedor los cambios por lotes.</span><span class="sxs-lookup"><span data-stu-id="fa415-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="fa415-p107">Si sale del registro que está agregando o editando antes de llamar al método **Update**, ADO llamará automáticamente al método **Update** para guardar los cambios. Debe llamar al método [CancelUpdate](cancelupdate-method-ado.md) si desea cancelar los cambios realizados en el registro actual o descartar un registro que acaba de agregar.</span><span class="sxs-lookup"><span data-stu-id="fa415-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="fa415-133">El registro actual se mantiene actual después de llamar al método **Update**.</span><span class="sxs-lookup"><span data-stu-id="fa415-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="fa415-134">Record</span><span class="sxs-lookup"><span data-stu-id="fa415-134">Record</span></span>

<span data-ttu-id="fa415-135">El método **Update** finaliza las adiciones, eliminaciones y actualizaciones realizadas en los campos de la colección [Fields](fields-collection-ado.md) de un objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="fa415-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="fa415-p108">Por ejemplo, los campos eliminados con el método **Delete** quedan inmediatamente marcados para su eliminación pero permanecen en la colección. Es preciso llamar al método **Update** para eliminar realmente estos campos de la colección del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fa415-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

