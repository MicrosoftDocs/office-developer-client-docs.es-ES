---
title: Index.Required Property (DAO)
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
ms.openlocfilehash: 0797ed5f930d4475d03f492109c977f8494591ce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485848"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="10d04-102">Index.Required Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="10d04-102">Index.Required Property (DAO)</span></span>


<span data-ttu-id="10d04-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="10d04-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="10d04-104">Establece o devuelve un valor que indica si un objeto **[Field](field-object-dao.md)** requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="10d04-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10d04-105">Syntax</span></span>

<span data-ttu-id="10d04-106">*expresión* . Obligatorio</span><span class="sxs-lookup"><span data-stu-id="10d04-106">*expression* .Required</span></span>

<span data-ttu-id="10d04-107">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="10d04-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d04-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10d04-108">Remarks</span></span>


> [!NOTE]
> <P><span data-ttu-id="10d04-p101">[!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto <STRONG>Index</STRONG> como para un objeto <STRONG>Field</STRONG>, establézcala para el objeto <STRONG>Field</STRONG>. La validez del valor de la propiedad para un objeto <STRONG>Field</STRONG> se comprueba antes que para un objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="10d04-p101">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



<span data-ttu-id="10d04-111">La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección [Fields](fields-collection-dao.md), como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="10d04-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10d04-112">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="10d04-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="10d04-113">Entonces Required</span><span class="sxs-lookup"><span data-stu-id="10d04-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10d04-114">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="10d04-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="10d04-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="10d04-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10d04-116">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="10d04-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="10d04-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="10d04-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10d04-118">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="10d04-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="10d04-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="10d04-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10d04-120">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="10d04-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="10d04-121">No admitido</span><span class="sxs-lookup"><span data-stu-id="10d04-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10d04-122">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="10d04-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="10d04-123">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="10d04-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

