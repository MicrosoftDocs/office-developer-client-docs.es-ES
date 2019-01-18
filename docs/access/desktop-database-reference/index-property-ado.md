---
title: Index (propiedad, ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709106"
---
# <a name="index-property-ado"></a><span data-ttu-id="4d79f-102">Index (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4d79f-102">Index property (ADO)</span></span>


<span data-ttu-id="4d79f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d79f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d79f-104">Indica el nombre del índice en vigor para un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d79f-104">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4d79f-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4d79f-105">Settings and return values</span></span>

<span data-ttu-id="4d79f-106">Establece o devuelve un valor de tipo **String** que es el nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="4d79f-106">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d79f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d79f-107">Remarks</span></span>

<span data-ttu-id="4d79f-p101">El índice denominado por la propiedad **Index** debe haber sido declarado previamente en la tabla base subyacente al objeto **Recordset**. Es decir, el índice debe haber sido declarado mediante programación como un objeto [Index](index-object-adox.md) de ADOX o al crear la tabla base.</span><span class="sxs-lookup"><span data-stu-id="4d79f-p101">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object. That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="4d79f-p102">Si no se puede establecer el índice, se producirá un error en tiempo de ejecución. No se puede establecer la propiedad **Index**:</span><span class="sxs-lookup"><span data-stu-id="4d79f-p102">A run-time error will occur if the index cannot be set. The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="4d79f-112">En un controlador de eventos [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) o **RecordsetChangeComplete**.</span><span class="sxs-lookup"><span data-stu-id="4d79f-112">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="4d79f-113">Si el objeto **Recordset** sigue ejecutando una operación (lo que se determina mediante la propiedad [Estado (State)](state-property-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="4d79f-113">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="4d79f-114">Si se ha establecido un filtro en el objeto **Recordset** con la propiedad [Filter](filter-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d79f-114">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="4d79f-115">La propiedad **Index** siempre se puede establecer correctamente si el objeto **Recordset** está cerrado; sin embargo, el objeto **Recordset** no se abrirá correctamente o el índice no será útil si el proveedor subyacente no admite índices.</span><span class="sxs-lookup"><span data-stu-id="4d79f-115">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="4d79f-p103">Si se puede establecer el índice, la posición actual de la fila puede cambiar. Eso provocará una actualización de la propiedad [AbsolutePosition](absoluteposition-property-ado.md), así como la generación de eventos **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) y [MoveComplete](willmove-and-movecomplete-events-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d79f-p103">If the index can be set, the current row position may change. This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="4d79f-p104">Si es posible establecer el índice y la propiedad [LockType](locktype-property-ado.md) es **adLockPessimistic** o **adLockOptimistic**, se realiza una operación implícita [UpdateBatch](updatebatch-method-ado.md). Eso libera al grupo actual y a los afectados. Se liberan todos los filtros existentes y la posición actual de la fila se cambia por la primera fila del reordenado objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4d79f-p104">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed. This releases the current and affected groups. Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="4d79f-121">La propiedad **Index** se usa junto con el método [Seek](seek-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d79f-121">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="4d79f-122">Si el proveedor subyacente no es compatible con la propiedad **Index** ni con el método **Seek**, considere la posibilidad de usar el método [Find](find-method-ado.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4d79f-122">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="4d79f-123">Determinar si el objeto **Recordset** admite índices con el método **(adIndex)** [admite](supports-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d79f-123">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="4d79f-124">La propiedad integrada **Index** no está relacionada con la propiedad dinámica [Optimize](optimize-property-dynamic-ado.md), aunque ambas tienen que ver con los índices.</span><span class="sxs-lookup"><span data-stu-id="4d79f-124">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

