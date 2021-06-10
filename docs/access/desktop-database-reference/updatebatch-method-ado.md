---
title: Método UpdateBatch (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d269a9012588a7b82505ac2e28466151715cbb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313579"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="4b201-102">Método UpdateBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="4b201-102">UpdateBatch method (ADO)</span></span>

<span data-ttu-id="4b201-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b201-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b201-104">Escribe en el disco todas las actualizaciones por lotes que están pendientes.</span><span class="sxs-lookup"><span data-stu-id="4b201-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b201-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b201-105">Syntax</span></span>

<span data-ttu-id="4b201-106">*recordset*. UpdateBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="4b201-106">*recordset*.UpdateBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="4b201-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b201-107">Parameters</span></span>

|<span data-ttu-id="4b201-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4b201-108">Parameter</span></span>|<span data-ttu-id="4b201-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b201-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4b201-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="4b201-110">*AffectRecords*</span></span> |<span data-ttu-id="4b201-p101">Es opcional. Valor de [AffectEnum](affectenum.md) que indica el número de registros afectados por el método **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="4b201-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4b201-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b201-113">Remarks</span></span>

<span data-ttu-id="4b201-114">Use el método **UpdateBatch** cuando modifique un objeto **Recordset** en modo de actualización por lotes para transmitir todos los cambios realizados en el objeto **Recordset** a la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="4b201-114">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="4b201-p102">Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llama al método **UpdateBatch**. Si está modificando el registro actual o agregando un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método [Update](update-method-ado.md) para guardar todos los cambios pendientes en el registro actual antes de transmitir al proveedor los cambios por lotes. La actualización por lotes debe utilizarse únicamente con un cursor estático o un cursor dirigido por un conjunto de claves.</span><span class="sxs-lookup"><span data-stu-id="4b201-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider. You should use batch updating with either a keyset or static cursor only.</span></span>

> [!NOTE]
> <span data-ttu-id="4b201-118">Si se especifica **adAffectGroup** como valor para este parámetro, se producirá un error cuando no haya registros visibles en el actual objeto **Recordset** (como un filtro sin registros coincidentes).</span><span class="sxs-lookup"><span data-stu-id="4b201-118">Specifying **adAffectGroup** as the value for this parameter will result in an error when there are no visible records in the current **Recordset** (such as a filter for which no records match).</span></span>

<span data-ttu-id="4b201-p103">Si un intento de transmitir los cambios de algunos o todos los registros genera un error debido a un conflicto con los datos subyacentes (por ejemplo, otro usuario ya ha eliminado un registro), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) y se genera un error en tiempo de ejecución. Utilice la propiedad [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) y la propiedad [Status](status-property-ado-recordset.md) para localizar los registros con conflictos.</span><span class="sxs-lookup"><span data-stu-id="4b201-p103">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="4b201-121">Para cancelar todas las actualizaciones por lotes que estén pendientes, utilice el método [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4b201-121">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="4b201-122">Si están establecidas las propiedades dinámicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y [Update Resync](update-resync-property-dynamic-ado.md), y el objeto **Recordset** es el resultado de la ejecución de una operación JOIN en varias tablas, la ejecución del método **UpdateBatch** va implícitamente seguida del método [Resync](resync-method-ado.md), según el valor de la propiedad **Update Resync**.</span><span class="sxs-lookup"><span data-stu-id="4b201-122">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="4b201-p104">El orden en que se ejecutan las actualizaciones individuales de un lote en el origen de datos no es necesariamente el mismo orden en que se realizan en el objeto **Recordset** local. El orden de actualización depende del proveedor. Téngalo en cuenta cuando codifique actualizaciones relacionadas entre sí, como las restricciones de clave externa en una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="4b201-p104">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**. Update order is dependent upon the provider. Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

