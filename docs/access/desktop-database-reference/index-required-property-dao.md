---
title: Propiedad index. reQuired (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291702"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="87dee-102">Propiedad index. reQuired (DAO)</span><span class="sxs-lookup"><span data-stu-id="87dee-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="87dee-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87dee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87dee-104">Establece o devuelve un valor que indica si un objeto **[Field](field-object-dao.md)** requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="87dee-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="87dee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87dee-105">Syntax</span></span>

<span data-ttu-id="87dee-106">*expresión* . Necesarios</span><span class="sxs-lookup"><span data-stu-id="87dee-106">*expression* .Required</span></span>

<span data-ttu-id="87dee-107">*expresión* Variable que representa un objeto **index** .</span><span class="sxs-lookup"><span data-stu-id="87dee-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87dee-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87dee-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="87dee-p101">[!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto **Index** como para un objeto **Field**, establézcala para el objeto **Field**. La validez del valor de la propiedad para un objeto **Field** se comprueba antes que para un objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="87dee-p101">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="87dee-111">La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección [Fields](fields-collection-dao.md), como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="87dee-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87dee-112">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="87dee-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="87dee-113">Entonces Required</span><span class="sxs-lookup"><span data-stu-id="87dee-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87dee-114">
						Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="87dee-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="87dee-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="87dee-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dee-116">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="87dee-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="87dee-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="87dee-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dee-118">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="87dee-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="87dee-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="87dee-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dee-120">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="87dee-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="87dee-121">No está admitido</span><span class="sxs-lookup"><span data-stu-id="87dee-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dee-122">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="87dee-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="87dee-123">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="87dee-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

