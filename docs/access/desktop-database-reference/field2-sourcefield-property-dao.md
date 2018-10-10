---
title: Field2.SourceField Property (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09351acfea263c41bd9cb7f857139dfacf359421
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484979"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="7e773-102">Field2.SourceField Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7e773-102">Field2.SourceField Property (DAO)</span></span>


<span data-ttu-id="7e773-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e773-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7e773-p101">Devuelve un valor que indica el nombre del campo que es la fuente original de los datos para un objeto **Field2**. **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="7e773-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e773-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e773-106">Syntax</span></span>

<span data-ttu-id="7e773-107">*expresión* . SourceField</span><span class="sxs-lookup"><span data-stu-id="7e773-107">*expression* .SourceField</span></span>

<span data-ttu-id="7e773-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="7e773-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e773-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e773-109">Remarks</span></span>

<span data-ttu-id="7e773-110">Para un objeto **Field2**, utilice las propiedades **SourceField** y **SourceTable** dependiendo del objeto que contenga la colección **Fields** al que el objeto **Field2** está anexado, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7e773-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e773-111">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="7e773-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="7e773-112">Uso</span><span class="sxs-lookup"><span data-stu-id="7e773-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e773-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="7e773-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="7e773-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="7e773-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e773-115"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="7e773-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7e773-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e773-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e773-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="7e773-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="7e773-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e773-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e773-119"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="7e773-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="7e773-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="7e773-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e773-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="7e773-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7e773-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e773-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e773-p102">Estas propiedades indican que el campo original y los nombres de tabla están asociados con un objeto **Field2**. Por ejemplo, podría utilizar estas propiedades para determinar el origen inicial de los datos en un campo de consulta cuyo nombre no está relacionado con el nombre del campo de una tabla base.</span><span class="sxs-lookup"><span data-stu-id="7e773-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

