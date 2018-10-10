---
title: WillExecute (evento, ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a5c739ffd408a1f53539c88a3bdc4169eb4cebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483664"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="9df9b-102">WillExecute (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="9df9b-102">WillExecute Event (ADO)</span></span>


<span data-ttu-id="9df9b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9df9b-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="9df9b-104">El evento **WillExecute** se utiliza (recibe una llamada) justo antes de que un comando pendiente se ejecute sobre una conexión.</span><span class="sxs-lookup"><span data-stu-id="9df9b-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9df9b-105">Syntax</span></span>

<span data-ttu-id="9df9b-106">WillExecute*origen*, *CursorType*, *LockType*, *Opciones*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="9df9b-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="9df9b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9df9b-107">Parameters</span></span>

  - <span data-ttu-id="9df9b-108">*Origen*</span><span class="sxs-lookup"><span data-stu-id="9df9b-108">*Source*</span></span>

  - <span data-ttu-id="9df9b-109">**String** que contiene un comando SQL o un nombre de procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="9df9b-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="9df9b-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="9df9b-110">*CursorType*</span></span>

  - <span data-ttu-id="9df9b-111">Valor de tipo [CursorTypeEnum](cursortypeenum.md) que contiene el tipo de cursor para el objeto **Recordset** que se abrirá.</span><span class="sxs-lookup"><span data-stu-id="9df9b-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="9df9b-112">Con este parámetro, puede cambiar el cursor a cualquier tipo durante una operación de [apertura](open-method-ado-recordset.md) del **objeto Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9df9b-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="9df9b-113">*CursorType* se omitirá para cualquier otra operación.</span><span class="sxs-lookup"><span data-stu-id="9df9b-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="9df9b-114">*LockType*</span><span class="sxs-lookup"><span data-stu-id="9df9b-114">*LockType*</span></span>

  - <span data-ttu-id="9df9b-115">Valor de tipo [LockTypeEnum](locktypeenum.md) que contiene el tipo de bloqueo para el objeto **Recordset** que se abrirá.</span><span class="sxs-lookup"><span data-stu-id="9df9b-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="9df9b-116">Con este parámetro, es posible cambiar el bloqueo a cualquier tipo durante una operación del método **Open** de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9df9b-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="9df9b-117">*LockType* se omitirá para cualquier otra operación.</span><span class="sxs-lookup"><span data-stu-id="9df9b-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="9df9b-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="9df9b-118">*Options*</span></span>

  - <span data-ttu-id="9df9b-119">Valor de tipo **Long** que indica las opciones que se pueden usar para ejecutar el comando o abrir el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9df9b-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="9df9b-120">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="9df9b-120">*adStatus*</span></span>

  - [<span data-ttu-id="9df9b-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="9df9b-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="9df9b-122">Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores, o en **adStatusCancel** para solicitar la cancelación de la operación que provocó el evento.</span><span class="sxs-lookup"><span data-stu-id="9df9b-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="9df9b-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="9df9b-123">*pCommand*</span></span>

  - <span data-ttu-id="9df9b-124">Objeto [Command](command-object-ado.md) al que se aplica esta notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="9df9b-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="9df9b-125">*Connection*</span><span class="sxs-lookup"><span data-stu-id="9df9b-125">*pRecordset*</span></span>

  - <span data-ttu-id="9df9b-126">Objeto [Recordset](recordset-object-ado.md) al que se aplica esta notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="9df9b-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="9df9b-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="9df9b-127">*pConnection*</span></span>

  - <span data-ttu-id="9df9b-128">Objeto [Connection](connection-object-ado.md) al que se aplica esta notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="9df9b-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df9b-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9df9b-129">Remarks</span></span>

<span data-ttu-id="9df9b-130">Un evento **WillExecute** puede ocurrir debido a un **conexión.** [Ejecutar](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **comando.** [Ejecutar](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), o **Recordset.** Método [Open](open-method-ado-recordset.md) el parámetro *pConnection* siempre debe contener una referencia válida a un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="9df9b-130">A **WillExecute** event may occur due to a **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="9df9b-131">Si el evento es debido a **Connection.Execute**, los parámetros *pRecordset* y *pCommand* se establecen en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="9df9b-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="9df9b-132">Si el evento es debido a **un método Recordset.Open**, el parámetro *pRecordset* hará referencia al objeto de **conjunto de registros** y el parámetro *pCommand* se establece en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="9df9b-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="9df9b-133">Si el evento es debido a **un método Command.Execute**, el parámetro *pCommand* hará referencia al objeto de **comando** y el parámetro *pRecordset* se establece en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="9df9b-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="9df9b-p104">**WillExecute** permite examinar y modificar los parámetros pendientes de ejecución. Este evento puede devolver una petición para cancelar el comando pendiente.</span><span class="sxs-lookup"><span data-stu-id="9df9b-p104">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>
