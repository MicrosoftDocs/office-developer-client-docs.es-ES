---
title: WillChangeRecordset y RecordsetChangeComplete (evento, ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f9126005d8f11f859a3f45cbfec08e6612b59ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484328"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="be3e8-102">WillChangeRecordset y RecordsetChangeComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="be3e8-102">WillChangeRecordset and RecordsetChangeComplete Events (ADO)</span></span>


<span data-ttu-id="be3e8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be3e8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="be3e8-p101">Al evento **WillChangeRecordset** se le llama antes de que una operación pendiente cambie el [Recordset](recordset-object-ado.md). Al evento **RecordsetChangeComplete** se le llama después de que el objeto **Recordset** haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="be3e8-p101">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md). The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3e8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be3e8-106">Syntax</span></span>

<span data-ttu-id="be3e8-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="be3e8-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="be3e8-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="be3e8-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="be3e8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be3e8-109">Parameters</span></span>

  - <span data-ttu-id="be3e8-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="be3e8-110">*adReason*</span></span>

  - <span data-ttu-id="be3e8-p102">Valor [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnRequery**, **adRsnResynch**, **adRsnClose** o \*\* adRsnOpen\*\*.</span><span class="sxs-lookup"><span data-stu-id="be3e8-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>

  - <span data-ttu-id="be3e8-113">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="be3e8-113">*adStatus*</span></span>

  - [<span data-ttu-id="be3e8-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="be3e8-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="be3e8-p103">Cuando se llama a **WillChangeRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="be3e8-p103">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="be3e8-117">Cuando se llama a **RecordsetChangeComplete**, este parámetro se establece en \*\* adStatusOK\*\* si la operación que provocó el evento se realizó correctamente, en **adStatusErrorsOccurred** si se produjo un error en la operación o en **adStatusCancel** si se ha cancelado la operación asociada al evento **WillChangeRecordset** anteriormente aceptado.</span><span class="sxs-lookup"><span data-stu-id="be3e8-117">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span>
    
    <span data-ttu-id="be3e8-118">Antes de que **WillChangeRecordset** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="be3e8-118">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span>
    
    <span data-ttu-id="be3e8-119">Antes de que **WillChangeRecordset** o **RecordsetChangeComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="be3e8-119">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="be3e8-120">*pError*</span><span class="sxs-lookup"><span data-stu-id="be3e8-120">*pError*</span></span>

  - <span data-ttu-id="be3e8-p104">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="be3e8-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="be3e8-123">*Connection*</span><span class="sxs-lookup"><span data-stu-id="be3e8-123">*pRecordset*</span></span>

  - <span data-ttu-id="be3e8-p105">Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="be3e8-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3e8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be3e8-126">Remarks</span></span>

<span data-ttu-id="be3e8-127">Un **WillChangeRecordset** o **RecordsetChangeComplete** evento puede producirse debido a los métodos de **Recordset** [Requery](requery-method-ado.md) u [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="be3e8-127">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="be3e8-p106">Si el proveedor no admite marcadores, se produce una notificación de evento **RecordsetChange** cada vez de que se recuperan filas nuevas del proveedor. La frecuencia de este evento depende de la propiedad **RecordsetCacheSize**.</span><span class="sxs-lookup"><span data-stu-id="be3e8-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="be3e8-130">Debe establecer el parámetro **adStatus** en **adStatusUnwantedEvent** para cada valor posible de **adReason** con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro **adReason** .</span><span class="sxs-lookup"><span data-stu-id="be3e8-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>

