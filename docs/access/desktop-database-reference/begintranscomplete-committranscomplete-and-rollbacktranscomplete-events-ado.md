---
title: Eventos de RollbackTransComplete BeginTransComplete, CommitTransComplete, (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf38a106a8cb53c1603628f0c3c0096be4b73d52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888639"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="75db0-102">s BeginTransComplete, CommitTransComplete y RollbackTransComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="75db0-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)</span></span>


<span data-ttu-id="75db0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75db0-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="75db0-104">A estos eventos se les llama después de que la operación asociada sobre el objeto [Connection](connection-object-ado.md) haya terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="75db0-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

  - <span data-ttu-id="75db0-105">A **BeginTransComplete** se le llama después de la operación [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="75db0-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="75db0-106">A **CommitTransComplete** se le llama después de la operación [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="75db0-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="75db0-107">A **RollbackTransComplete** se le llama después de la operación [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="75db0-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="75db0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75db0-108">Syntax</span></span>

<span data-ttu-id="75db0-109">De BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="75db0-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="75db0-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="75db0-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="75db0-111">A RollbackTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="75db0-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="75db0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75db0-112">Parameters</span></span>

  - <span data-ttu-id="75db0-113">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="75db0-113">*TransactionLevel*</span></span>

  - <span data-ttu-id="75db0-114">Valor **Long** que contiene el nuevo nivel de transacción de la operación **BeginTrans** que causó este evento.</span><span class="sxs-lookup"><span data-stu-id="75db0-114">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>

  - <span data-ttu-id="75db0-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="75db0-115">*pError*</span></span>

  - <span data-ttu-id="75db0-p101">Objeto [Error](error-object-ado.md). Describe el error si el valor de EventStatusEnum es \*\* adStatusErrorsOccurred\*\*; de lo contrario, no se establece un valor para él.</span><span class="sxs-lookup"><span data-stu-id="75db0-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="75db0-118">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="75db0-118">*adStatus*</span></span>

  - [<span data-ttu-id="75db0-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="75db0-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="75db0-120">Estos eventos pueden impedir notificaciones posteriores si se establece este parámetro en **adStatusUnwantedEvent** antes de que el evento vuelva.</span><span class="sxs-lookup"><span data-stu-id="75db0-120">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>

  - <span data-ttu-id="75db0-121">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="75db0-121">*pConnection*</span></span>

  - <span data-ttu-id="75db0-122">El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="75db0-122">The **Connection** object for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="75db0-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75db0-123">Remarks</span></span>

<span data-ttu-id="75db0-p102">En Visual C++, varios objetos **Connection** pueden compartir el mismo método de control de evento. El método utiliza el objeto \*\* Connection\*\* devuelto para determinar qué objeto causó el evento.</span><span class="sxs-lookup"><span data-stu-id="75db0-p102">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="75db0-p103">Si la propiedad [Attributes](attributes-property-ado.md) se establece en **adXactCommitRetaining** o **adXactAbortRetaining**, se iniciará una transacción nueva después de confirmar o deshacer una transacción. Utilice el evento **BeginTransComplete** para omitir todo excepto el primer evento de inicio de transacción.</span><span class="sxs-lookup"><span data-stu-id="75db0-p103">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

