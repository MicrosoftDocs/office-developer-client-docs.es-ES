---
title: Propiedad QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd958c4b2123c727c3bc0a14a067fcb719ec86b3
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026389"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="0ca8c-102">Propiedad QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ca8c-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="0ca8c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ca8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ca8c-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ca8c-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca8c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ca8c-106">Syntax</span></span>

<span data-ttu-id="0ca8c-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="0ca8c-107">*expression* .Type</span></span>

<span data-ttu-id="0ca8c-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="0ca8c-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca8c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ca8c-109">Remarks</span></span>

<span data-ttu-id="0ca8c-110">Para un objeto **QueryDef**, los valores o valores enteros posibles se muestran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0ca8c-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ca8c-111">Constante</span><span class="sxs-lookup"><span data-stu-id="0ca8c-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0ca8c-112">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="0ca8c-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-114">Acción</span><span class="sxs-lookup"><span data-stu-id="0ca8c-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca8c-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-116">Anexar</span><span class="sxs-lookup"><span data-stu-id="0ca8c-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-118">Compuesta</span><span class="sxs-lookup"><span data-stu-id="0ca8c-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca8c-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-120">Tabla de referencias cruzadas</span><span class="sxs-lookup"><span data-stu-id="0ca8c-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-122">Definición de datos</span><span class="sxs-lookup"><span data-stu-id="0ca8c-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca8c-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-124">Delete</span><span class="sxs-lookup"><span data-stu-id="0ca8c-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-126">Creación de tabla</span><span class="sxs-lookup"><span data-stu-id="0ca8c-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca8c-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-128">Procedimiento (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="0ca8c-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="0ca8c-129"><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0ca8c-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0ca8c-130">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0ca8c-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-132">Selección</span><span class="sxs-lookup"><span data-stu-id="0ca8c-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca8c-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-134">Unión</span><span class="sxs-lookup"><span data-stu-id="0ca8c-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-136">Utilizada con <strong>dbQSQLPassThrough</strong> para especificar una consulta que no devuelve registros (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="0ca8c-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca8c-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-138">Paso a través (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="0ca8c-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca8c-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="0ca8c-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca8c-140">Update</span><span class="sxs-lookup"><span data-stu-id="0ca8c-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ca8c-141">Cuando se anexa un nuevo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** o **[Property](property-object-dao.md)** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="0ca8c-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

