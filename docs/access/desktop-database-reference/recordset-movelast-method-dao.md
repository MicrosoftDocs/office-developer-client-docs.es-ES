---
title: Método Recordset. moVelast (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284535"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="bcfb0-102">Método Recordset. moVelast (DAO)</span><span class="sxs-lookup"><span data-stu-id="bcfb0-102">Recordset.MoveLast method (DAO)</span></span>

<span data-ttu-id="bcfb0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bcfb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bcfb0-104">Se desplaza al último registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcfb0-105">Syntax</span></span>

<span data-ttu-id="bcfb0-106">*expresión* . MoVelast (***Opciones***)</span><span class="sxs-lookup"><span data-stu-id="bcfb0-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="bcfb0-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="bcfb0-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcfb0-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="bcfb0-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bcfb0-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="bcfb0-109">Name</span></span></p></th>
<th><p><span data-ttu-id="bcfb0-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="bcfb0-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="bcfb0-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bcfb0-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="bcfb0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcfb0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bcfb0-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="bcfb0-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="bcfb0-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="bcfb0-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="bcfb0-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="bcfb0-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="bcfb0-116">Establecido en <strong>dbRunAsync</strong> para ejecutar la llamada en <strong>MoveLast</strong> de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bcfb0-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcfb0-117">Remarks</span></span>

<span data-ttu-id="bcfb0-118">Use los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="bcfb0-p101">Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="bcfb0-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="bcfb0-123">Si el primer o el último registro ya está activo cuando utiliza **MoveFirst** o **MoveLast**, el registro activo no cambia.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="bcfb0-124">Si Recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="bcfb0-125">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="bcfb0-126">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="bcfb0-127">[!NOTA] Puede usar el método **MoveLast** para llenar totalmente un objeto **Recordset** de tipo dynaset o snapshot y que proporcione el número actual de registros de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="bcfb0-128">No obstante, si usa **MoveLast** de esta forma, puede ralentizar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="bcfb0-129">Solo debe usar **MoveLast** para obtener el recuento de registros si es absolutamente necesario para lograr un recuento preciso en un objeto **Recordset** recién abierto.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
> 
> <span data-ttu-id="bcfb0-130">Si usa la constante **dbRunAsync** con **MoveLast**, la llamada al método es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="bcfb0-131">Puede usar la propiedad **StillExecuting** para determinar cuándo está totalmente lleno el objeto **Recordset** y el método **Cancel** para terminar la ejecución de la llamada a método **MoveLast** asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="bcfb0-132">No puede usar los métodos **MoveFirst**, **MoveLast** ni **MovePrevious** en un objeto **Recordset** de tipo de solo avance.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="bcfb0-133">Para mover la posición del registro actual en un objeto **Recordset** un número específico de registros hacia delante o hacia atrás, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

