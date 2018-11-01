---
title: s WillChangeRecord y RecordChangeComplete (evento, ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 895a80cf4810088b5f18f4a9416e7eadc54a004f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878132"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a><span data-ttu-id="8e3ad-102">s WillChangeRecord y RecordChangeComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="8e3ad-102">WillChangeRecord and RecordChangeComplete Events (ADO)</span></span>


<span data-ttu-id="8e3ad-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e3ad-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8e3ad-p101">El evento **WillChangeRecord** se usa (recibe una llamada) antes de cualquier cambio en uno o más registros (filas) del objeto [Recordset](recordset-object-ado.md). El evento **RecordChangeComplete** recibe una llamada después de cualquier cambio en uno o más registros.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-p101">The **WillChangeRecord** event is called before one or more records (rows) in the [Recordset](recordset-object-ado.md) change. The **RecordChangeComplete** event is called after one or more records change.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3ad-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e3ad-106">Syntax</span></span>

<span data-ttu-id="8e3ad-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="8e3ad-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="8e3ad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e3ad-109">Parameters</span></span>

  - <span data-ttu-id="8e3ad-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-110">*adReason*</span></span>

  - <span data-ttu-id="8e3ad-p102">Valor [EventReasonEnum](eventreasonenum.md) que especifica el motivo para este evento. El valor puede ser **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, \*\* adRsnUndoUpdate\*\*, **adRsnUndoAddNew**, **adRsnUndoDelete** o **adRsnFirstChange**.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, or **adRsnFirstChange**.</span></span>

  - <span data-ttu-id="8e3ad-113">*cRecords*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-113">*cRecords*</span></span>

  - <span data-ttu-id="8e3ad-114">Valor **Long** que indica el número de registros cambiados (afectados).</span><span class="sxs-lookup"><span data-stu-id="8e3ad-114">A **Long** value that indicates the number of records changing (affected).</span></span>

  - <span data-ttu-id="8e3ad-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-115">*pError*</span></span>

  - <span data-ttu-id="8e3ad-p103">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="8e3ad-118">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-118">*adStatus*</span></span>

  - [<span data-ttu-id="8e3ad-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="8e3ad-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="8e3ad-p104">Cuando se realiza una llamada a **WillChangeRecord**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-p104">When **WillChangeRecord** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="8e3ad-122">Cuando se llama a **RecordChangeComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-122">When **RecordChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="8e3ad-123">Antes de que **WillChangeRecord** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación que causó este evento, o en adStatusUnwantedEvent para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-123">Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="8e3ad-124">Antes de que **RecordChangeComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-124">Before **RecordChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="8e3ad-125">*Connection*</span><span class="sxs-lookup"><span data-stu-id="8e3ad-125">*pRecordset*</span></span>

  - <span data-ttu-id="8e3ad-p105">Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3ad-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e3ad-128">Remarks</span></span>

<span data-ttu-id="8e3ad-129">Un evento **WillChangeRecord** o **RecordChangeComplete** se puede producir para el primer campo cambiados de una fila debido a las operaciones del objeto **Recordset** siguientes: [ Update ](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) y [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ad-129">A **WillChangeRecord** or **RecordChangeComplete** event may occur for the first changed field in a row due to the following **Recordset** operations: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [CancelBatch](cancelbatch-method-ado.md).</span></span> <span data-ttu-id="8e3ad-130">El valor de [CursorType](cursortype-property-ado.md) del **Recordset** determina qué operaciones hacen que se producen los eventos.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-130">The value of the **Recordset** [CursorType](cursortype-property-ado.md) determines which operations cause the events to occur.</span></span>

<span data-ttu-id="8e3ad-131">Durante el evento **WillChangeRecord** , la propiedad de [filtro](filter-property-ado.md) de **conjunto de registros** se establece en **adFilterAffectedRecords**.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-131">During the **WillChangeRecord** event, the **Recordset** [Filter](filter-property-ado.md) property is set to **adFilterAffectedRecords**.</span></span> <span data-ttu-id="8e3ad-132">No es posible cambiar esta propiedad mientras se procesa el evento.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-132">You cannot change this property while processing the event.</span></span>

<span data-ttu-id="8e3ad-133">Deberá establecer el parámetro adStatus en adStatusUnwantedEvent para cada valor posible de adReason con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro adReason.</span><span class="sxs-lookup"><span data-stu-id="8e3ad-133">You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.</span></span>

