---
title: Propiedad QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300948"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="bb1af-102">Propiedad QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="bb1af-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="bb1af-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb1af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb1af-104">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="bb1af-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="bb1af-105">Integer de solo **lectura.**</span><span class="sxs-lookup"><span data-stu-id="bb1af-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1af-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb1af-106">Syntax</span></span>

<span data-ttu-id="bb1af-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="bb1af-107">*expression* .Type</span></span>

<span data-ttu-id="bb1af-108">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="bb1af-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1af-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb1af-109">Remarks</span></span>

<span data-ttu-id="bb1af-110">Para un objeto **QueryDef**, los valores o valores enteros posibles se muestran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bb1af-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb1af-111">Constante</span><span class="sxs-lookup"><span data-stu-id="bb1af-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="bb1af-112">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="bb1af-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-114">Acción</span><span class="sxs-lookup"><span data-stu-id="bb1af-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb1af-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-116">Anexar</span><span class="sxs-lookup"><span data-stu-id="bb1af-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-118">Compuesto</span><span class="sxs-lookup"><span data-stu-id="bb1af-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb1af-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-120">Crosstab</span><span class="sxs-lookup"><span data-stu-id="bb1af-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-122">Definición de datos</span><span class="sxs-lookup"><span data-stu-id="bb1af-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb1af-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-124">Eliminar</span><span class="sxs-lookup"><span data-stu-id="bb1af-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-126">Creación de tabla</span><span class="sxs-lookup"><span data-stu-id="bb1af-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb1af-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-128">Procedimiento (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="bb1af-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="bb1af-129"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bb1af-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bb1af-130">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bb1af-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-132">Select</span><span class="sxs-lookup"><span data-stu-id="bb1af-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb1af-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-134">Union</span><span class="sxs-lookup"><span data-stu-id="bb1af-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-136">Utilizada con <strong>dbQSQLPassThrough</strong> para especificar una consulta que no devuelve registros (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="bb1af-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb1af-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-138">Paso a través (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="bb1af-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb1af-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="bb1af-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="bb1af-140">Actualizar</span><span class="sxs-lookup"><span data-stu-id="bb1af-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb1af-141">Cuando se anexa un nuevo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** o **[Property](property-object-dao.md)** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="bb1af-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

