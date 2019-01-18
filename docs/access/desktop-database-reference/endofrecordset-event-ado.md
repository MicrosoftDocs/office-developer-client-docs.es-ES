---
title: EndOfRecordset (evento, ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721363"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="b90ed-102">EndOfRecordset (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="b90ed-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="b90ed-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b90ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b90ed-104">Al evento **EndOfRecordset** se le llama cuando se intenta pasar a una fila más allá del final del objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b90ed-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b90ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b90ed-105">Syntax</span></span>

<span data-ttu-id="b90ed-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="b90ed-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="b90ed-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b90ed-107">Parameters</span></span>

|<span data-ttu-id="b90ed-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b90ed-108">Parameter</span></span>|<span data-ttu-id="b90ed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b90ed-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b90ed-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="b90ed-110">*fMoreData*</span></span> |<span data-ttu-id="b90ed-111">A **VARIANT\_BOOL** valor que, si se establece en VARIANT\_TRUE, indica que se han agregado más filas para el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="b90ed-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="b90ed-112">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="b90ed-112">*adStatus*</span></span> |<span data-ttu-id="b90ed-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="b90ed-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="b90ed-114">Al llamar a **EndOfRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b90ed-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="b90ed-115">Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación que provocó este evento.</span><span class="sxs-lookup"><span data-stu-id="b90ed-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="b90ed-116">Antes de que **EndOfRecordset** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para evitar notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b90ed-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="b90ed-117">*Connection*</span><span class="sxs-lookup"><span data-stu-id="b90ed-117">*pRecordset*</span></span> | <span data-ttu-id="b90ed-p102">Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="b90ed-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b90ed-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b90ed-120">Remarks</span></span>

<span data-ttu-id="b90ed-121">Un evento **EndOfRecordset** puede ocurrir si se produce un error en la operación [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b90ed-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="b90ed-122">El controlador del evento recibe una llamada cuando se realiza un intento de avanzar más allá del final del objeto **Recordset**, quizá debido a una llamada a **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="b90ed-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="b90ed-123">Sin embargo, mientras ocurre este evento, todavía se podrían recuperar más registros de una base de datos y agregarlos al final del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b90ed-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="b90ed-124">En ese caso, establezca *fMoreData* en VARIANT\_es TRUE y devolución de **EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="b90ed-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="b90ed-125">A continuación, llame de nuevo a **MoveNext** para obtener acceso a los registros recién recuperados.</span><span class="sxs-lookup"><span data-stu-id="b90ed-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

