---
title: ExecuteComplete (evento, ADO)
TOCTitle: ExecuteComplete Event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 231cfcf42cead3074996870971488dadb60583ae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605425"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="da0d0-102">ExecuteComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="da0d0-102">ExecuteComplete Event (ADO)</span></span>


<span data-ttu-id="da0d0-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="da0d0-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="da0d0-104">Al evento **ExecuteComplete** se le llama después de que un comando haya terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="da0d0-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da0d0-105">Syntax</span></span>

<span data-ttu-id="da0d0-106">De ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*y *pConnection*</span><span class="sxs-lookup"><span data-stu-id="da0d0-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="da0d0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da0d0-107">Parameters</span></span>

  - <span data-ttu-id="da0d0-108">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="da0d0-108">*RecordsAffected*</span></span>

  - <span data-ttu-id="da0d0-109">Valor **Long** que indica el número de registros afectados por el comando.</span><span class="sxs-lookup"><span data-stu-id="da0d0-109">A **Long** value indicating the number of records affected by the command.</span></span>

  - <span data-ttu-id="da0d0-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="da0d0-110">*pError*</span></span>

  - <span data-ttu-id="da0d0-p101">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="da0d0-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="da0d0-113">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="da0d0-113">*adStatus*</span></span>

  - [<span data-ttu-id="da0d0-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="da0d0-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="da0d0-115">Antes de que este evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="da0d0-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="da0d0-116">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="da0d0-116">*pCommand*</span></span>

  - <span data-ttu-id="da0d0-p102">Objeto [Command](command-object-ado.md) que se ejecutó. Contiene un objeto **Command** incluso al llamar a **Connection.Execute** o a **Recordset.Open** sin crear explícitamente un objeto **Command**; en tales casos, ADO crea internamente el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="da0d0-p102">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>

  - <span data-ttu-id="da0d0-119">*Connection*</span><span class="sxs-lookup"><span data-stu-id="da0d0-119">*pRecordset*</span></span>

  - <span data-ttu-id="da0d0-p103">Objeto [Recordset](recordset-object-ado.md) resultado del comando ejecutado. Este **Recordset** puede estar vacío. No debería nunca destruir este objeto Recordset desde dentro de este controlador de evento. Si lo hace, se producirá una infracción de acceso cuando ADO intente obtener acceso a un objeto que ya no existe.</span><span class="sxs-lookup"><span data-stu-id="da0d0-p103">A [Recordset](recordset-object-ado.md) object that is the result of the executed command. This **Recordset** may be empty. You should never destroy this Recordset object from within this event handler. Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>

  - <span data-ttu-id="da0d0-124">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="da0d0-124">*pConnection*</span></span>

  - <span data-ttu-id="da0d0-p104">Objeto [Connection](connection-object-ado.md). La conexión sobre la que se ejecutó la operación.</span><span class="sxs-lookup"><span data-stu-id="da0d0-p104">A [Connection](connection-object-ado.md) object. The connection over which the operation was executed.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0d0-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da0d0-127">Remarks</span></span>

<span data-ttu-id="da0d0-128"><<<<<<< HEAD un evento **ExecuteComplete** puede ocurrir debido a la **conexión.** [Ejecutar](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **comando.** [Ejecutar](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), **Recordset.** [Open](open-method-ado-recordset.md), **Recordset.** [Requery](requery-method-ado.md), o **Recordset.** Métodos de [NextRecordset](nextrecordset-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="da0d0-128"><<<<<<< HEAD An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>
<span data-ttu-id="da0d0-129">=== Un evento **ExecuteComplete** puede ocurrir debido a la **conexión.** [Ejecutar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **comando.** [Ejecutar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.** [Open](open-method-ado-recordset.md), **Recordset.** [Requery](requery-method-ado.md), o **Recordset.** Métodos de [NextRecordset](nextrecordset-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="da0d0-129">======= An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>
>>>>>>> <span data-ttu-id="da0d0-130">master</span><span class="sxs-lookup"><span data-stu-id="da0d0-130">master</span></span>

