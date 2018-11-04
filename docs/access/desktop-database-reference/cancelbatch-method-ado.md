---
title: CancelBatch (método, ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88bf83cad220056d9ee21f300e5543030e5d18cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950084"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="839b4-102">CancelBatch (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="839b4-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="839b4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="839b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="839b4-104">Cancela una actualización por lotes que está pendiente.</span><span class="sxs-lookup"><span data-stu-id="839b4-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="839b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="839b4-105">Syntax</span></span>

<span data-ttu-id="839b4-106">*conjunto de registros*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="839b4-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="839b4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="839b4-107">Parameters</span></span>

|<span data-ttu-id="839b4-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="839b4-108">Parameter</span></span>|<span data-ttu-id="839b4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="839b4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="839b4-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="839b4-110">*AffectRecords*</span></span> |<span data-ttu-id="839b4-p101">Es opcional. Valor de [AffectEnum](affectenum.md) que indica el número de registros afectados por el método **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="839b4-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="839b4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="839b4-113">Remarks</span></span>

<span data-ttu-id="839b4-p102">Use el método **CancelBatch** para cancelar cualquier actualización pendiente en un objeto [Recordset](recordset-object-ado.md) en modo de actualización por lotes. Si el objeto **Recordset** está en modo de actualización inmediata y se llama a **CancelBatch** sin **adAffectCurrent**, se generará un error.</span><span class="sxs-lookup"><span data-stu-id="839b4-p102">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode. If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="839b4-p103">Si está modificando el registro actual o agregando un registro nuevo cuando llama a **CancelBatch**, ADO llamará primero al método [CancelUpdate](cancelupdate-method-ado.md) para cancelar los cambios almacenados en caché. A continuación, se cancelarán todos los cambios pendientes en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="839b4-p103">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes. After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="839b4-p104">Es posible que el registro actual sea indeterminable después de llamar a **CancelBatch**, sobre todo si se estaba agregando un registro nuevo. Por este motivo, se recomienda establecer la posición del registro actual en una ubicación conocida en el objeto **Recordset** después de la llamada a **CancelBatch**, llamando, por ejemplo al método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="839b4-p104">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record. For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call. For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="839b4-p105">Si un intento de cancelar las actualizaciones pendientes genera un error debido a un conflicto con los datos subyacentes (por ejemplo, otro usuario ha eliminado un registro), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) pero no detiene la ejecución del programa. Se produce un error en tiempo de ejecución sólo si hay conflictos en todos los registros solicitados. Utilice la propiedad [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) y la propiedad [Status](status-property-ado-recordset.md) para localizar los registros con conflictos.</span><span class="sxs-lookup"><span data-stu-id="839b4-p105">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

