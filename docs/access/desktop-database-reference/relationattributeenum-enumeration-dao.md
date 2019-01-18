---
title: RelationAttributeEnum (enumeración) (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711122"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="82f57-102">RelationAttributeEnum (enumeración) (DAO)</span><span class="sxs-lookup"><span data-stu-id="82f57-102">RelationAttributeEnum enumeration (DAO)</span></span>


<span data-ttu-id="82f57-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82f57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82f57-104">Se utiliza con la propiedad **Attributes** para determinar los atributos de un objeto **Relation**.</span><span class="sxs-lookup"><span data-stu-id="82f57-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82f57-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="82f57-105">Name</span></span></p></th>
<th><p><span data-ttu-id="82f57-106">Valor</span><span class="sxs-lookup"><span data-stu-id="82f57-106">Value</span></span></p></th>
<th><p><span data-ttu-id="82f57-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="82f57-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82f57-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="82f57-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="82f57-109">4096</span><span class="sxs-lookup"><span data-stu-id="82f57-109">4096</span></span></p></td>
<td><p><span data-ttu-id="82f57-110">Eliminaciones en cascada.</span><span class="sxs-lookup"><span data-stu-id="82f57-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f57-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="82f57-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="82f57-112">2</span><span class="sxs-lookup"><span data-stu-id="82f57-112">2</span></span></p></td>
<td><p><span data-ttu-id="82f57-113">Relación no exigida (sin integridad referencial).</span><span class="sxs-lookup"><span data-stu-id="82f57-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f57-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="82f57-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="82f57-115">4</span><span class="sxs-lookup"><span data-stu-id="82f57-115">4</span></span></p></td>
<td><p><span data-ttu-id="82f57-116">La relación existe en la base de datos que contiene las dos tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="82f57-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f57-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="82f57-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="82f57-118">16777216</span><span class="sxs-lookup"><span data-stu-id="82f57-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="82f57-p101">Microsoft Access únicamente. En la vista Diseño, muestre una operación LEFT JOIN como tipo de combinación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="82f57-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f57-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="82f57-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="82f57-122">33554432</span><span class="sxs-lookup"><span data-stu-id="82f57-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="82f57-p102">Microsoft Access únicamente. En la vista Diseño, muestre una operación RIGHT JOIN como tipo de combinación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="82f57-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f57-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="82f57-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="82f57-126">1</span><span class="sxs-lookup"><span data-stu-id="82f57-126">1</span></span></p></td>
<td><p><span data-ttu-id="82f57-127">Relación uno a uno.</span><span class="sxs-lookup"><span data-stu-id="82f57-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f57-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="82f57-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="82f57-129">256</span><span class="sxs-lookup"><span data-stu-id="82f57-129">256</span></span></p></td>
<td><p><span data-ttu-id="82f57-130">Actualizaciones en cascada.</span><span class="sxs-lookup"><span data-stu-id="82f57-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

