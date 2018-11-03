---
title: EndOfRecordset (evento, ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89ca397c4e95dd6f18de41862e9383f77fe14aa8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928841"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="84798-102">EndOfRecordset (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="84798-102">EndOfRecordset event (ADO)</span></span>


<span data-ttu-id="84798-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84798-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="84798-104">Al evento **EndOfRecordset** se le llama cuando se intenta pasar a una fila más allá del final del objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84798-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84798-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84798-105">Syntax</span></span>

<span data-ttu-id="84798-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="84798-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="84798-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84798-107">Parameters</span></span>

  - <span data-ttu-id="84798-108">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="84798-108">*fMoreData*</span></span>

  - <span data-ttu-id="84798-109">A **VARIANT\_BOOL** valor que, si se establece en VARIANT\_TRUE, indica que se han agregado más filas para el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="84798-109">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>

  - <span data-ttu-id="84798-110">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="84798-110">*adStatus*</span></span>

  - [<span data-ttu-id="84798-111">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="84798-111">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="84798-p101">Al llamar a **EndOfRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación que provocó este evento.</span><span class="sxs-lookup"><span data-stu-id="84798-p101">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span>
    
    <span data-ttu-id="84798-114">Antes de que **EndOfRecordset** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para evitar notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="84798-114">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="84798-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="84798-115">*pRecordset*</span></span>

  - <span data-ttu-id="84798-p102">Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="84798-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="84798-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84798-118">Remarks</span></span>

<span data-ttu-id="84798-119">Un evento **EndOfRecordset** puede ocurrir si se produce un error en la operación [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84798-119">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="84798-120">El controlador del evento recibe una llamada cuando se realiza un intento de avanzar más allá del final del objeto **Recordset**, quizá debido a una llamada a **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="84798-120">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="84798-121">Sin embargo, mientras ocurre este evento, todavía se podrían recuperar más registros de una base de datos y agregarlos al final del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="84798-121">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="84798-122">En ese caso, establezca *fMoreData* en VARIANT\_es TRUE y devolución de **EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="84798-122">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="84798-123">A continuación, llame de nuevo a **MoveNext** para obtener acceso a los registros recién recuperados.</span><span class="sxs-lookup"><span data-stu-id="84798-123">Then call **MoveNext** again to access the newly retrieved records.</span></span>

