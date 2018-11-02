---
title: Propiedad Index.Required (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 44fa827be7359c598ff610313be4c2acf30d5e50
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920567"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="4d686-102">Propiedad Index.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d686-102">Index.Required property (DAO)</span></span>


<span data-ttu-id="4d686-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d686-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d686-104">Establece o devuelve un valor que indica si un objeto **[Field](field-object-dao.md)** requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="4d686-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d686-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d686-105">Syntax</span></span>

<span data-ttu-id="4d686-106">*expresión* . Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d686-106">*expression* .Required</span></span>

<span data-ttu-id="4d686-107">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="4d686-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d686-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d686-108">Remarks</span></span>


> [!NOTE]
> <P><span data-ttu-id="4d686-p101">[!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto <STRONG>Index</STRONG> como para un objeto <STRONG>Field</STRONG>, establézcala para el objeto <STRONG>Field</STRONG>. La validez del valor de la propiedad para un objeto <STRONG>Field</STRONG> se comprueba antes que para un objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4d686-p101">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



<span data-ttu-id="4d686-111">La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección [Fields](fields-collection-dao.md), como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4d686-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d686-112">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="4d686-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="4d686-113">Entonces Required</span><span class="sxs-lookup"><span data-stu-id="4d686-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d686-114">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="4d686-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4d686-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="4d686-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d686-116">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4d686-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4d686-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d686-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d686-118">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4d686-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4d686-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d686-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d686-120">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="4d686-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4d686-121">No admitido</span><span class="sxs-lookup"><span data-stu-id="4d686-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d686-122">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4d686-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4d686-123">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="4d686-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

