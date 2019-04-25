---
title: CREATE VIEW (instrucción de Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295369"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="77bbb-102">CREATE VIEW (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="77bbb-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="77bbb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77bbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77bbb-104">Crea una vista.</span><span class="sxs-lookup"><span data-stu-id="77bbb-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="77bbb-105">El motor de base de datos de Microsoft Access no admite el uso de CREATE VIEW, ni de cualquiera de las instrucciones DDL, con bases de datos distintas del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="77bbb-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bbb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77bbb-106">Syntax</span></span>

<span data-ttu-id="77bbb-107">CREATE VIEW *view* \[(*campo1*\[, *campo2*\[, …\]\])\] AS *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="77bbb-107">CREATE VIEW *view [(field1* \[[, *field2*[, …]])] AS *selectstatement*</span></span>

<span data-ttu-id="77bbb-108">La instrucción CREATE VIEW tiene estas partes:</span><span class="sxs-lookup"><span data-stu-id="77bbb-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77bbb-109">Part</span><span class="sxs-lookup"><span data-stu-id="77bbb-109">Part</span></span></p></th>
<th><p><span data-ttu-id="77bbb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="77bbb-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77bbb-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="77bbb-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="77bbb-112">El nombre de la vista que se creará.</span><span class="sxs-lookup"><span data-stu-id="77bbb-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bbb-113"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="77bbb-113"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="77bbb-114">El nombre de los campos correspondientes especificados en <em>selectstatement</em>.</span><span class="sxs-lookup"><span data-stu-id="77bbb-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bbb-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="77bbb-115">AS <em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="77bbb-116">Una instrucción SELECT de SQL.</span><span class="sxs-lookup"><span data-stu-id="77bbb-116">A SQL SELECT statement.</span></span> <span data-ttu-id="77bbb-117">Para obtener más información, vea <a href="select-statement-microsoft-access-sql.md">SELECT (instrucción)</a>.</span><span class="sxs-lookup"><span data-stu-id="77bbb-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="77bbb-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77bbb-118">Remarks</span></span>

<span data-ttu-id="77bbb-119">La instrucción SELECT que define la vista no puede ser una instrucción [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="77bbb-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="77bbb-120">La instrucción SELECT que define la vista no puede contener ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="77bbb-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="77bbb-121">El nombre de la vista no puede coincidir con el nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="77bbb-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="77bbb-122">Si la consulta definida en la instrucción SELECT se puede actualizar, la vista también se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="77bbb-122">If the query defined by the SELECT statement is updatable, then the view is also updatable.</span></span> <span data-ttu-id="77bbb-123">De lo contrario, la vista será de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="77bbb-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="77bbb-124">Si alguno de los dos campos de la consulta definida por la instrucción SELECT tienen el mismo nombre, en la definición de vista es necesario incluir una lista de campos que especifiquen nombres únicos para cada uno de los campos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="77bbb-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

