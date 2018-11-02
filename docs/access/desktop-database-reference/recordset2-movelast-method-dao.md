---
title: Recordset2.MoveLast (método) (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5e636bf5ecae615df458754d6c4e08f00065ff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923612"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="3be6b-102">Recordset2.MoveLast (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="3be6b-102">Recordset2.MoveLast method (DAO)</span></span>


<span data-ttu-id="3be6b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3be6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3be6b-104">Se desplaza al último registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="3be6b-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be6b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3be6b-105">Syntax</span></span>

<span data-ttu-id="3be6b-106">*expresión* . MoveLast (***Opciones***)</span><span class="sxs-lookup"><span data-stu-id="3be6b-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="3be6b-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3be6b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="3be6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3be6b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3be6b-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="3be6b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3be6b-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="3be6b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3be6b-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3be6b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="3be6b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3be6b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3be6b-113">Opciones</span><span class="sxs-lookup"><span data-stu-id="3be6b-113">Options</span></span></p></td>
<td><p><span data-ttu-id="3be6b-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="3be6b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="3be6b-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="3be6b-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="3be6b-116">Establecido en <strong>dbRunAsync</strong> para ejecutar la llamada en <strong>MoveLast</strong> de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3be6b-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3be6b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3be6b-117">Remarks</span></span>

<span data-ttu-id="3be6b-118">Utilice los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="3be6b-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="3be6b-p101">Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="3be6b-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="3be6b-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="3be6b-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="3be6b-123">Si el primer o el último registro ya está activo cuando utiliza **MoveFirst** o **MoveLast**, el registro activo no cambia.</span><span class="sxs-lookup"><span data-stu-id="3be6b-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="3be6b-124">Si el objeto recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="3be6b-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="3be6b-125">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="3be6b-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="3be6b-126">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="3be6b-126">If you don't set the current index, the order of returned records is undefined.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3be6b-p104">[!NOTA] Puede usar el método <STRONG>MoveLast</STRONG> para llenar totalmente un objeto <STRONG>Recordset</STRONG> de tipo dynaset o snapshot y que proporcione el número actual de registros de <STRONG>Recordset</STRONG>. No obstante, si usa <STRONG>MoveLast</STRONG> de esta forma, puede ralentizar el rendimiento de la aplicación. Solo debe usar <STRONG>MoveLast</STRONG> para obtener el recuento de registros si es absolutamente necesario para lograr un recuento preciso en un objeto <STRONG>Recordset</STRONG> recién abierto. Si usa la constante <STRONG>dbRunAsync</STRONG> con <STRONG>MoveLast</STRONG>, la llamada al método es asincrónica. Puede usar la propiedad <STRONG>StillExecuting</STRONG> para determinar cuándo está totalmente lleno el objeto <STRONG>Recordset</STRONG> y el método <STRONG>Cancel</STRONG> para terminar la ejecución de la llamada a método <STRONG>MoveLast</STRONG> asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3be6b-p104">You can use the <STRONG>MoveLast</STRONG> method to fully populate a dynaset- or snapshot-type <STRONG>Recordset</STRONG> to provide the current number of records in the <STRONG>Recordset</STRONG>. However, if you use <STRONG>MoveLast</STRONG> in this way, you can slow down your application's performance. You should only use <STRONG>MoveLast</STRONG> to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened <STRONG>Recordset</STRONG>. If you use the <STRONG>dbRunAsync</STRONG> constant with <STRONG>MoveLast</STRONG>, the method call is asynchronous. You can use the <STRONG>StillExecuting</STRONG> property to determine when the <STRONG>Recordset</STRONG> is fully populated, and you can use the <STRONG>Cancel</STRONG> method to terminate execution of the asynchronous <STRONG>MoveLast</STRONG> method call.</span></span></P>



<span data-ttu-id="3be6b-132">No puede usar los métodos **MoveFirst**, **MoveLast**ni **MovePrevious** en un objeto **Recordset** de tipo forward – only.</span><span class="sxs-lookup"><span data-stu-id="3be6b-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="3be6b-133">Para mover hacia delante o hacia atrás la posición del registro actual en un objeto **Recordset** un número determinado de registros, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="3be6b-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

