---
title: Propiedad QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42bd391cea721176973ce4dd30c9ddc7d15471b8
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937025"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="6e388-102">Propiedad QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e388-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="6e388-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e388-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e388-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6e388-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e388-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e388-106">Syntax</span></span>

<span data-ttu-id="6e388-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="6e388-107">*expression* .Type</span></span>

<span data-ttu-id="6e388-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="6e388-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e388-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e388-109">Remarks</span></span>

<span data-ttu-id="6e388-110">Para un objeto **QueryDef**, los valores o valores enteros posibles se muestran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6e388-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e388-111">Constante</span><span class="sxs-lookup"><span data-stu-id="6e388-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="6e388-112">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="6e388-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e388-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-114">Acción</span><span class="sxs-lookup"><span data-stu-id="6e388-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e388-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-116">Anexar</span><span class="sxs-lookup"><span data-stu-id="6e388-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e388-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-118">Compuesta</span><span class="sxs-lookup"><span data-stu-id="6e388-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e388-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-120">Tabla de referencias cruzadas</span><span class="sxs-lookup"><span data-stu-id="6e388-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e388-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-122">Definición de datos</span><span class="sxs-lookup"><span data-stu-id="6e388-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e388-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-124">Delete</span><span class="sxs-lookup"><span data-stu-id="6e388-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e388-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-126">Creación de tabla</span><span class="sxs-lookup"><span data-stu-id="6e388-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e388-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-128">Procedimiento (sólo áreas de trabajo de ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="6e388-128">Procedure (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <span data-ttu-id="6e388-p102">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6e388-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e388-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-132">Selección</span><span class="sxs-lookup"><span data-stu-id="6e388-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e388-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-134">Unión</span><span class="sxs-lookup"><span data-stu-id="6e388-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e388-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-136">Utilizada con <strong>dbQSQLPassThrough</strong> para especificar una consulta que no devuelve registros (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="6e388-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e388-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-138">Paso a través (sólo para áreas de trabajo de Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="6e388-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e388-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="6e388-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="6e388-140">Update</span><span class="sxs-lookup"><span data-stu-id="6e388-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e388-141">Cuando se anexa un nuevo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** o **[Property](property-object-dao.md)** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="6e388-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

