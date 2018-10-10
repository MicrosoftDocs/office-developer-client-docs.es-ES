---
title: CREATE VIEW (instrucción de Microsoft Access SQL)
TOCTitle: CREATE VIEW Statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 292dddeab15c71fb188a928ac0e491063930214d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484493"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="c614f-102">CREATE VIEW (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c614f-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="c614f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c614f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c614f-104">Crea una nueva vista.</span><span class="sxs-lookup"><span data-stu-id="c614f-104">Creates a new view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c614f-105">[!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE VIEW, ni las instrucciones DDL, con bases de datos que no sean del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c614f-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span></P>



## <a name="syntax"></a><span data-ttu-id="c614f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c614f-106">Syntax</span></span>

<span data-ttu-id="c614f-107">CREATE VIEW *vista* \[(*campo1*\[, *field2*\[,... \] \])\] AS *instrucciónSelect*</span><span class="sxs-lookup"><span data-stu-id="c614f-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="c614f-108">La instrucción CREATE VIEW consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c614f-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c614f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c614f-109">Part</span></span></p></th>
<th><p><span data-ttu-id="c614f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c614f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c614f-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="c614f-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="c614f-112">Nombre de la vista que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c614f-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c614f-113"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="c614f-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="c614f-114">Nombre del campo o campos correspondientes a los campos especificados en <em>instrucciónSelect</em>.</span><span class="sxs-lookup"><span data-stu-id="c614f-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c614f-115"><em>instrucciónSelect</em></span><span class="sxs-lookup"><span data-stu-id="c614f-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="c614f-p101">Instrucción SQL SELECT. Para obtener más información, vea <a href="select-statement-microsoft-access-sql.md">SELECT (instrucción)</a>.</span><span class="sxs-lookup"><span data-stu-id="c614f-p101">A SQL SELECT statement. For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c614f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c614f-118">Remarks</span></span>

<span data-ttu-id="c614f-119">La instrucción SELECT que define la vista no puede ser una instrucción [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c614f-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="c614f-120">La instrucción SELECT que define la vista no puede contener ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="c614f-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="c614f-121">El nombre de la vista no puede ser igual que el nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="c614f-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="c614f-p102">Si la consulta definida en la instrucción SELECT se puede actualizar, la vista también se puede actualizar. De lo contrario, la vista es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c614f-p102">If the query defined by the SELECT statement is updatable, then the view is also updatable. Otherwise, the view is read-only.</span></span>

<span data-ttu-id="c614f-124">Si dos campos de la consulta definida en la instrucción SELECT tienen el mismo nombre, la definición de la vista debe incluir una lista de campos en la que se especifiquen nombres únicos para cada uno de los campos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c614f-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

