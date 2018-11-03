---
title: Propiedad Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 253be078fa6a8f5fdd4cb0c6c67fc6d5385e554c
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936542"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="a82a2-102">Propiedad Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="a82a2-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="a82a2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a82a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a82a2-p101">Devuelve un valor que indica el nombre de la tabla que es la fuente original de los datos para un objeto **Field2**. **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a82a2-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82a2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a82a2-106">Syntax</span></span>

<span data-ttu-id="a82a2-107">*expresión* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="a82a2-107">*expression* .SourceTable</span></span>

<span data-ttu-id="a82a2-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="a82a2-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a82a2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a82a2-109">Remarks</span></span>

<span data-ttu-id="a82a2-110">Para un objeto **Field2**, utilice las propiedades **SourceField** y **SourceTable** dependiendo del objeto que contenga la colección **Fields** al que el objeto **Field2** está anexado, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a82a2-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a82a2-111">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="a82a2-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="a82a2-112">Uso</span><span class="sxs-lookup"><span data-stu-id="a82a2-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a82a2-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a82a2-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a82a2-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="a82a2-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a82a2-115"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a82a2-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a82a2-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a82a2-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a82a2-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a82a2-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="a82a2-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a82a2-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a82a2-119"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="a82a2-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="a82a2-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="a82a2-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a82a2-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a82a2-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a82a2-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a82a2-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a82a2-p102">Estas propiedades indican que el campo original y los nombres de tabla están asociados con un objeto **Field2**. Por ejemplo, podría utilizar estas propiedades para determinar el origen inicial de los datos en un campo de consulta cuyo nombre no está relacionado con el nombre del campo de una tabla base.</span><span class="sxs-lookup"><span data-stu-id="a82a2-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="a82a2-125">[!NOTA] La propiedad **SourceTable** no devolverá un nombre de tabla significativo si se usa en un objeto **Field2** de la colección **Fields** de un tipo de tabla del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a82a2-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


