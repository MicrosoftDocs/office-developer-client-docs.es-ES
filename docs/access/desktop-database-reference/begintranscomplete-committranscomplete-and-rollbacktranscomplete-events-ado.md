---
title: Eventos de RollbackTransComplete BeginTransComplete, CommitTransComplete, (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702897"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="73b63-102">BeginTransComplete, CommitTransComplete y RollbackTransComplete (eventos, ADO)</span><span class="sxs-lookup"><span data-stu-id="73b63-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="73b63-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73b63-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73b63-104">A estos eventos se les llama después de que la operación asociada sobre el objeto [Connection](connection-object-ado.md) haya terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="73b63-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="73b63-105">A **BeginTransComplete** se le llama después de la operación [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="73b63-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="73b63-106">A **CommitTransComplete** se le llama después de la operación [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="73b63-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="73b63-107">A **RollbackTransComplete** se le llama después de la operación [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="73b63-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b63-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73b63-108">Syntax</span></span>

<span data-ttu-id="73b63-109">De BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="73b63-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="73b63-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="73b63-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="73b63-111">A RollbackTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="73b63-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="73b63-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73b63-112">Parameters</span></span>

|<span data-ttu-id="73b63-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="73b63-113">Parameter</span></span>|<span data-ttu-id="73b63-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="73b63-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="73b63-115">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="73b63-115">*TransactionLevel*</span></span> |<span data-ttu-id="73b63-116">Valor **Long** que contiene el nuevo nivel de transacción de la operación **BeginTrans** que causó este evento.</span><span class="sxs-lookup"><span data-stu-id="73b63-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="73b63-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="73b63-117">*pError*</span></span> |<span data-ttu-id="73b63-118">Objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="73b63-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="73b63-119">Describe el error que se produjo si el valor de EventStatusEnum es **adStatusErrorsOccurred**; de lo contrario, no se establece.</span><span class="sxs-lookup"><span data-stu-id="73b63-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="73b63-120">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="73b63-120">*adStatus*</span></span> |<span data-ttu-id="73b63-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="73b63-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="73b63-122">Estos eventos pueden impedir notificaciones posteriores si se establece este parámetro en **adStatusUnwantedEvent** antes de que el evento vuelva.</span><span class="sxs-lookup"><span data-stu-id="73b63-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="73b63-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="73b63-123">*pConnection*</span></span> |<span data-ttu-id="73b63-124">El objeto **Recordset** para el que se produjo este evento.</span><span class="sxs-lookup"><span data-stu-id="73b63-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="73b63-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73b63-125">Remarks</span></span>

<span data-ttu-id="73b63-p103">En Visual C++, varios objetos **Connection** pueden compartir el mismo método de control de evento. El método utiliza el objeto \*\* Connection\*\* devuelto para determinar qué objeto causó el evento.</span><span class="sxs-lookup"><span data-stu-id="73b63-p103">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="73b63-p104">Si la propiedad [Attributes](attributes-property-ado.md) se establece en **adXactCommitRetaining** o **adXactAbortRetaining**, se iniciará una transacción nueva después de confirmar o deshacer una transacción. Utilice el evento **BeginTransComplete** para omitir todo excepto el primer evento de inicio de transacción.</span><span class="sxs-lookup"><span data-stu-id="73b63-p104">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

