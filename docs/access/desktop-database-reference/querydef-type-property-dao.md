---
title: QueryDef.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5129f4a50f056259c5b556c8e8ea408358718d3c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484619"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="72417-102">QueryDef.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="72417-102">QueryDef.Type Property (DAO)</span></span>


<span data-ttu-id="72417-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72417-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72417-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="72417-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="72417-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72417-106">Syntax</span></span>

<span data-ttu-id="72417-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="72417-107">*expression* .Type</span></span>

<span data-ttu-id="72417-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="72417-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="72417-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72417-109">Remarks</span></span>

<span data-ttu-id="72417-110">Para un objeto **QueryDef**, los valores o valores enteros posibles se muestran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="72417-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72417-111">Constante</span><span class="sxs-lookup"><span data-stu-id="72417-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="72417-112">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="72417-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72417-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="72417-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-114">Acción</span><span class="sxs-lookup"><span data-stu-id="72417-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72417-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="72417-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-116">Anexar</span><span class="sxs-lookup"><span data-stu-id="72417-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72417-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="72417-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-118">Compuesta</span><span class="sxs-lookup"><span data-stu-id="72417-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72417-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="72417-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-120">Tabla de referencias cruzadas</span><span class="sxs-lookup"><span data-stu-id="72417-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72417-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="72417-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-122">Definición de datos</span><span class="sxs-lookup"><span data-stu-id="72417-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72417-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="72417-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-124">Delete</span><span class="sxs-lookup"><span data-stu-id="72417-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72417-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="72417-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-126">Creación de tabla</span><span class="sxs-lookup"><span data-stu-id="72417-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72417-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="72417-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-128">Procedimiento (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="72417-128">Procedure (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="72417-p102">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="72417-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72417-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="72417-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-132">Selección</span><span class="sxs-lookup"><span data-stu-id="72417-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72417-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="72417-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-134">Unión</span><span class="sxs-lookup"><span data-stu-id="72417-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72417-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="72417-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-136">Utilizada con <strong>dbQSQLPassThrough</strong> para especificar una consulta que no devuelve registros (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="72417-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72417-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="72417-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-138">Paso a través (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="72417-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72417-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="72417-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="72417-140">Update</span><span class="sxs-lookup"><span data-stu-id="72417-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72417-141">Cuando se anexa un nuevo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** o **[Property](property-object-dao.md)** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="72417-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

