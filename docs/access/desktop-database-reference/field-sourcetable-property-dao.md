---
title: Propiedad Field.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292989"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="f7fec-102">Propiedad Field.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7fec-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="f7fec-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7fec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7fec-p101">Devuelve un valor que indica el nombre de la tabla que es la fuente original de los datos para un objeto **Field**. **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f7fec-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7fec-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7fec-106">Syntax</span></span>

<span data-ttu-id="f7fec-107">*expresión* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="f7fec-107">*expression* .SourceTable</span></span>

<span data-ttu-id="f7fec-108">*expression* Variable que representa un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="f7fec-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7fec-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7fec-109">Remarks</span></span>

<span data-ttu-id="f7fec-110">Para un objeto **Field**, utilice las propiedades **SourceField** y **SourceTable** dependiendo del objeto que contenga la colección **Fields** al que el objeto **Field** está anexado, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f7fec-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7fec-111">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="f7fec-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="f7fec-112">Uso</span><span class="sxs-lookup"><span data-stu-id="f7fec-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7fec-113"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="f7fec-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="f7fec-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="f7fec-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7fec-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="f7fec-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="f7fec-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f7fec-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7fec-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="f7fec-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="f7fec-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f7fec-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7fec-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="f7fec-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="f7fec-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="f7fec-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7fec-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="f7fec-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="f7fec-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f7fec-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f7fec-p102">Estas propiedades indican que el campo original y los nombres de tabla están asociados con un objeto **Field**. Por ejemplo, podría utilizar estas propiedades para determinar el origen inicial de los datos en un campo de consulta cuyo nombre no está relacionado con el nombre del campo de una tabla base.</span><span class="sxs-lookup"><span data-stu-id="f7fec-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="f7fec-125">[!NOTA] La propiedad **SourceTable** no devolverá un nombre de tabla significativo si se usa en un objeto **Field** de la colección **Fields** de un objeto **Recordset** de tipo tabla.</span><span class="sxs-lookup"><span data-stu-id="f7fec-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


