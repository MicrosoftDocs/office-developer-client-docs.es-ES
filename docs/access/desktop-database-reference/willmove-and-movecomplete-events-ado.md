---
title: WillMove y MoveComplete (eventos, ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5388601f1ac88e281a6abc5cfe1e644bdeebef28
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923570"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="4f05a-102">WillMove y MoveComplete (eventos, ADO)</span><span class="sxs-lookup"><span data-stu-id="4f05a-102">WillMove and MoveComplete events (ADO)</span></span>


<span data-ttu-id="4f05a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f05a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f05a-p101">El evento **WillMove** recibe una llamada antes de que una operación pendiente cambie la posición actual en el objeto [Recordset](recordset-object-ado.md). El evento **MoveComplete** recibe una llamada después de que la posición actual del objeto **Recordset** cambie.</span><span class="sxs-lookup"><span data-stu-id="4f05a-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f05a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f05a-106">Syntax</span></span>

<span data-ttu-id="4f05a-107">WillMove*adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="4f05a-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="4f05a-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="4f05a-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="4f05a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f05a-109">Parameters</span></span>

  - <span data-ttu-id="4f05a-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="4f05a-110">*adReason*</span></span>

  - <span data-ttu-id="4f05a-p102">Valor de [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** o **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="4f05a-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="4f05a-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="4f05a-113">*pError*</span></span>

  - <span data-ttu-id="4f05a-p103">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4f05a-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="4f05a-116">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="4f05a-116">*adStatus*</span></span>

  - [<span data-ttu-id="4f05a-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="4f05a-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="4f05a-p104">Cuando se realiza una llamada a **WillMove**, este parámetro se establece a **adStatusOK** si la operación que provocó el evento se realizó correctamente.Se establece en **adStatusCantDeny** si este evento no puede solicitar cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="4f05a-p104">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="4f05a-120">Cuando se llama a **MoveComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="4f05a-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="4f05a-121">Antes de que **WillMove** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f05a-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="4f05a-122">Antes de que **MoveComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f05a-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="4f05a-123">*Connection*</span><span class="sxs-lookup"><span data-stu-id="4f05a-123">*pRecordset*</span></span>

  - <span data-ttu-id="4f05a-p105">Objeto [Recordset](recordset-object-ado.md). El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="4f05a-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f05a-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f05a-126">Remarks</span></span>

<span data-ttu-id="4f05a-p106">Un evento **WillMove** o **MoveComplete** se puede producir debido a las siguientes operaciones con **Recordsets**: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) y [Requery](requery-method-ado.md). Estos eventos se pueden producir a causa de las propiedades siguientes: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) y [AbsolutePosition](absoluteposition-property-ado.md). Estos eventos también se producen si un objeto **Recordset** secundario tiene eventos de **Recordset** conectados y se mueve su **Recordset** principal.</span><span class="sxs-lookup"><span data-stu-id="4f05a-p106">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md). These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md). These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="4f05a-130">Deberá establecer el parámetro **adStatus** en **adStatusUnwantedEvent** para cada valor adReason posible con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro adReason.</span><span class="sxs-lookup"><span data-stu-id="4f05a-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>

