---
title: RelationAttributeEnum Enumeration (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c4d7a2b622e382461bcf1b4171a5aa85f036854
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486064"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="27a5a-102">RelationAttributeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="27a5a-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="27a5a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27a5a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27a5a-104">Se utiliza con la propiedad **Attributes** para determinar los atributos de un objeto **Relation**.</span><span class="sxs-lookup"><span data-stu-id="27a5a-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27a5a-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="27a5a-105">Name</span></span></p></th>
<th><p><span data-ttu-id="27a5a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="27a5a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="27a5a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a5a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27a5a-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="27a5a-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="27a5a-109">4096</span><span class="sxs-lookup"><span data-stu-id="27a5a-109">4096</span></span></p></td>
<td><p><span data-ttu-id="27a5a-110">Eliminaciones en cascada.</span><span class="sxs-lookup"><span data-stu-id="27a5a-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a5a-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="27a5a-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="27a5a-112">2</span><span class="sxs-lookup"><span data-stu-id="27a5a-112">2</span></span></p></td>
<td><p><span data-ttu-id="27a5a-113">Relación no exigida (sin integridad referencial).</span><span class="sxs-lookup"><span data-stu-id="27a5a-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a5a-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="27a5a-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="27a5a-115">4</span><span class="sxs-lookup"><span data-stu-id="27a5a-115">4</span></span></p></td>
<td><p><span data-ttu-id="27a5a-116">La relación existe en la base de datos que contiene las dos tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="27a5a-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a5a-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="27a5a-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="27a5a-118">16777216</span><span class="sxs-lookup"><span data-stu-id="27a5a-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="27a5a-p101">Microsoft Access únicamente. En la vista Diseño, muestre una operación LEFT JOIN como tipo de combinación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="27a5a-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a5a-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="27a5a-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="27a5a-122">33554432</span><span class="sxs-lookup"><span data-stu-id="27a5a-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="27a5a-p102">Microsoft Access únicamente. En la vista Diseño, muestre una operación RIGHT JOIN como tipo de combinación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="27a5a-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a5a-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="27a5a-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="27a5a-126">1</span><span class="sxs-lookup"><span data-stu-id="27a5a-126">1</span></span></p></td>
<td><p><span data-ttu-id="27a5a-127">Relación uno a uno.</span><span class="sxs-lookup"><span data-stu-id="27a5a-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a5a-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="27a5a-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="27a5a-129">256</span><span class="sxs-lookup"><span data-stu-id="27a5a-129">256</span></span></p></td>
<td><p><span data-ttu-id="27a5a-130">Actualizaciones en cascada.</span><span class="sxs-lookup"><span data-stu-id="27a5a-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

