---
title: Propiedad Field.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dabfa13bac6973cea4bd69e0867292c4a6967
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718213"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="4bae3-102">Propiedad Field.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="4bae3-102">Field.SourceField property (DAO)</span></span>


<span data-ttu-id="4bae3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bae3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bae3-p101">Devuelve un valor que indica el nombre del campo que es el origen de los datos correspondientes a un objeto **Field**. **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4bae3-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bae3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bae3-106">Syntax</span></span>

<span data-ttu-id="4bae3-107">*expresión* . SourceField</span><span class="sxs-lookup"><span data-stu-id="4bae3-107">*expression* .SourceField</span></span>

<span data-ttu-id="4bae3-108">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="4bae3-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bae3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bae3-109">Remarks</span></span>

<span data-ttu-id="4bae3-110">Para un objeto **Field**, utilice las propiedades **SourceField** y **SourceTable** dependiendo del objeto que contenga la colección **Fields** al que el objeto **Field** está anexado, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4bae3-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bae3-111">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="4bae3-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4bae3-112">Uso</span><span class="sxs-lookup"><span data-stu-id="4bae3-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bae3-113"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="4bae3-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4bae3-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="4bae3-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bae3-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4bae3-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4bae3-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bae3-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bae3-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4bae3-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4bae3-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bae3-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bae3-119"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="4bae3-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4bae3-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="4bae3-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bae3-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4bae3-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4bae3-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bae3-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4bae3-p102">Estas propiedades indican los nombres de tabla y campo originales asociados a un objeto **Field**. Por ejemplo, puede usar estas propiedades para determinar el origen de los datos en el campo de una consulta cuyo nombre no está relacionado con el nombre del campo de la tabla base.</span><span class="sxs-lookup"><span data-stu-id="4bae3-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

