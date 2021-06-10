---
title: Eventos WillMove y MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306058"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="61f62-102">Eventos WillMove y MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="61f62-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="61f62-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61f62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61f62-p101">El evento **WillMove** recibe una llamada antes de que una operación pendiente cambie la posición actual en el objeto [Recordset](recordset-object-ado.md). El evento **MoveComplete** recibe una llamada después de que la posición actual del objeto **Recordset** cambie.</span><span class="sxs-lookup"><span data-stu-id="61f62-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f62-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61f62-106">Syntax</span></span>

<span data-ttu-id="61f62-107">WillMove *adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="61f62-107">WillMove *adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="61f62-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="61f62-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="61f62-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61f62-109">Parameters</span></span>

|<span data-ttu-id="61f62-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="61f62-110">Parameter</span></span>|<span data-ttu-id="61f62-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="61f62-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="61f62-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="61f62-112">*adReason*</span></span> |<span data-ttu-id="61f62-p102">Valor de [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** o **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="61f62-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="61f62-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="61f62-115">*pError*</span></span> |<span data-ttu-id="61f62-p103">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="61f62-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="61f62-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="61f62-118">*adStatus*</span></span> |<span data-ttu-id="61f62-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="61f62-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="61f62-120">Cuando **se llama a WillMove,** este parámetro se establece en **adStatusOK** si la operación que provocó el evento se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="61f62-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="61f62-121">Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="61f62-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="61f62-122">Cuando se llama a **MoveComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="61f62-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="61f62-123">Antes de que **WillMove** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61f62-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="61f62-124">Antes de que **MoveComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61f62-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="61f62-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="61f62-125">*pRecordset*</span></span> |<span data-ttu-id="61f62-p105">Objeto [Recordset](recordset-object-ado.md). El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="61f62-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="61f62-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61f62-128">Remarks</span></span>

<span data-ttu-id="61f62-129">Puede producirse un evento **WillMove** **o MoveComplete** debido a las siguientes **operaciones recordset:**</span><span class="sxs-lookup"><span data-stu-id="61f62-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="61f62-130">Open</span><span class="sxs-lookup"><span data-stu-id="61f62-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="61f62-131">Move</span><span class="sxs-lookup"><span data-stu-id="61f62-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="61f62-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="61f62-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="61f62-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="61f62-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="61f62-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="61f62-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="61f62-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="61f62-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="61f62-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="61f62-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="61f62-137">Requery</span><span class="sxs-lookup"><span data-stu-id="61f62-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="61f62-138">Estos eventos pueden producirse debido a las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="61f62-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="61f62-139">Filter</span><span class="sxs-lookup"><span data-stu-id="61f62-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="61f62-140">Índice</span><span class="sxs-lookup"><span data-stu-id="61f62-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="61f62-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="61f62-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="61f62-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="61f62-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="61f62-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="61f62-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="61f62-144">Estos eventos también se producen si un objeto **Recordset** secundario tiene eventos de **Recordset** conectados y se mueve su **Recordset** principal.</span><span class="sxs-lookup"><span data-stu-id="61f62-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="61f62-145">Deberá establecer el parámetro *adStatus* como **adStatusUnwantedEvent** para cada valor posible de *adReason* con el fin de detener completamente la notificación de eventos para cualquier suceso que incluya un parámetro *adReason*.</span><span class="sxs-lookup"><span data-stu-id="61f62-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

