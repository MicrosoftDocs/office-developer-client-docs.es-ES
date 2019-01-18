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
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703135"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="3b8fd-102">Propiedad Index.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b8fd-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="3b8fd-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b8fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b8fd-104">Establece o devuelve un valor que indica si un objeto **[Field](field-object-dao.md)** requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="3b8fd-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b8fd-105">Syntax</span></span>

<span data-ttu-id="3b8fd-106">*expresión* . Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3b8fd-106">*expression* .Required</span></span>

<span data-ttu-id="3b8fd-107">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="3b8fd-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b8fd-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b8fd-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="3b8fd-p101">[!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto **Index** como para un objeto **Field**, establézcala para el objeto **Field**. La validez del valor de la propiedad para un objeto **Field** se comprueba antes que para un objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="3b8fd-p101">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="3b8fd-111">La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección [Fields](fields-collection-dao.md), como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3b8fd-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b8fd-112">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="3b8fd-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="3b8fd-113">Entonces Required</span><span class="sxs-lookup"><span data-stu-id="3b8fd-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b8fd-114">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fd-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b8fd-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="3b8fd-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b8fd-116">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fd-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b8fd-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b8fd-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b8fd-118">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fd-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b8fd-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b8fd-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b8fd-120">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fd-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b8fd-121">No admitido</span><span class="sxs-lookup"><span data-stu-id="3b8fd-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b8fd-122">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fd-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b8fd-123">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="3b8fd-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

