---
title: WillExecute (evento, ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4025645e5f8b12325ba20497ca6ef2b70175df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919454"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="27c65-102">WillExecute (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="27c65-102">WillExecute event (ADO)</span></span>


<span data-ttu-id="27c65-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27c65-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="27c65-104">El evento **WillExecute** se utiliza (recibe una llamada) justo antes de que un comando pendiente se ejecute sobre una conexión.</span><span class="sxs-lookup"><span data-stu-id="27c65-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c65-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27c65-105">Syntax</span></span>

<span data-ttu-id="27c65-106">WillExecute*origen*, *CursorType*, *LockType*, *Opciones*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="27c65-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="27c65-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27c65-107">Parameters</span></span>

  - <span data-ttu-id="27c65-108">*Origen*</span><span class="sxs-lookup"><span data-stu-id="27c65-108">*Source*</span></span>

  - <span data-ttu-id="27c65-109">**String** que contiene un comando SQL o un nombre de procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="27c65-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="27c65-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="27c65-110">*CursorType*</span></span>

  - <span data-ttu-id="27c65-111">Valor de tipo [CursorTypeEnum](cursortypeenum.md) que contiene el tipo de cursor para el objeto **Recordset** que se abrirá.</span><span class="sxs-lookup"><span data-stu-id="27c65-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="27c65-112">Con este parámetro, puede cambiar el cursor a cualquier tipo durante una operación de [apertura](open-method-ado-recordset.md) del **objeto Recordset** .</span><span class="sxs-lookup"><span data-stu-id="27c65-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="27c65-113">*CursorType* se omitirá para cualquier otra operación.</span><span class="sxs-lookup"><span data-stu-id="27c65-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="27c65-114">*LockType*</span><span class="sxs-lookup"><span data-stu-id="27c65-114">*LockType*</span></span>

  - <span data-ttu-id="27c65-115">Valor de tipo [LockTypeEnum](locktypeenum.md) que contiene el tipo de bloqueo para el objeto **Recordset** que se abrirá.</span><span class="sxs-lookup"><span data-stu-id="27c65-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="27c65-116">Con este parámetro, es posible cambiar el bloqueo a cualquier tipo durante una operación del método **Open** de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="27c65-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="27c65-117">*LockType* se omitirá para cualquier otra operación.</span><span class="sxs-lookup"><span data-stu-id="27c65-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="27c65-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="27c65-118">*Options*</span></span>

  - <span data-ttu-id="27c65-119">Valor de tipo **Long** que indica las opciones que se pueden usar para ejecutar el comando o abrir el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="27c65-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="27c65-120">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="27c65-120">*adStatus*</span></span>

  - [<span data-ttu-id="27c65-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="27c65-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="27c65-122">Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores, o en **adStatusCancel** para solicitar la cancelación de la operación que provocó el evento.</span><span class="sxs-lookup"><span data-stu-id="27c65-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="27c65-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="27c65-123">*pCommand*</span></span>

  - <span data-ttu-id="27c65-124">Objeto [Command](command-object-ado.md) al que se aplica esta notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="27c65-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="27c65-125">*Connection*</span><span class="sxs-lookup"><span data-stu-id="27c65-125">*pRecordset*</span></span>

  - <span data-ttu-id="27c65-126">Objeto [Recordset](recordset-object-ado.md) al que se aplica esta notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="27c65-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="27c65-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="27c65-127">*pConnection*</span></span>

  - <span data-ttu-id="27c65-128">Objeto [Connection](connection-object-ado.md) al que se aplica esta notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="27c65-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c65-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27c65-129">Remarks</span></span>

<span data-ttu-id="27c65-130">Un evento **WillExecute** puede ocurrir debido a un **conexión.** [Ejecutar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **comando.** [Ejecutar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), o **Recordset.** Método [Open](open-method-ado-recordset.md) el parámetro *pConnection* siempre debe contener una referencia válida a un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="27c65-130">A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="27c65-131">Si el evento es debido a **Connection.Execute**, los parámetros *pRecordset* y *pCommand* se establecen en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="27c65-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="27c65-132">Si el evento es debido a **un método Recordset.Open**, el parámetro *pRecordset* hará referencia al objeto de **conjunto de registros** y el parámetro *pCommand* se establece en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="27c65-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="27c65-133">Si el evento es debido a **un método Command.Execute**, el parámetro *pCommand* hará referencia al objeto de **comando** y el parámetro *pRecordset* se establece en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="27c65-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="27c65-p104">**WillExecute** permite examinar y modificar los parámetros pendientes de ejecución. Este evento puede devolver una petición para cancelar el comando pendiente.</span><span class="sxs-lookup"><span data-stu-id="27c65-p104">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

