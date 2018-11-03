---
title: UpdateCriteriaEnum (enumeración) (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6160c53dd1cab26b2b92ec023f28158635d7081
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944469"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="53c1f-102">UpdateCriteriaEnum (enumeración) (DAO)</span><span class="sxs-lookup"><span data-stu-id="53c1f-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="53c1f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53c1f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53c1f-104">Se utiliza con el método **UpdateOptions** para especificar cómo se crea una actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="53c1f-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53c1f-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="53c1f-105">Name</span></span></p></th>
<th><p><span data-ttu-id="53c1f-106">Valor</span><span class="sxs-lookup"><span data-stu-id="53c1f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="53c1f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="53c1f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53c1f-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="53c1f-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="53c1f-109">4</span><span class="sxs-lookup"><span data-stu-id="53c1f-109">4</span></span></p></td>
<td><p><span data-ttu-id="53c1f-110">Utiliza la columna o columnas de clave y todas las columnas en la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="53c1f-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53c1f-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="53c1f-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="53c1f-112">16</span><span class="sxs-lookup"><span data-stu-id="53c1f-112">16</span></span></p></td>
<td><p><span data-ttu-id="53c1f-113">Utiliza un par de instrucciones DELETE e INSERT para cada fila modificada.</span><span class="sxs-lookup"><span data-stu-id="53c1f-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53c1f-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="53c1f-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="53c1f-115">1</span><span class="sxs-lookup"><span data-stu-id="53c1f-115">1</span></span></p></td>
<td><p><span data-ttu-id="53c1f-116">Utiliza sólo la columna o columnas de clave en la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="53c1f-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53c1f-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="53c1f-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="53c1f-118">2</span><span class="sxs-lookup"><span data-stu-id="53c1f-118">2</span></span></p></td>
<td><p><span data-ttu-id="53c1f-119">Utiliza la columna o columnas de clave y todas las columnas actualizadas en la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="53c1f-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53c1f-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="53c1f-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="53c1f-121">8</span><span class="sxs-lookup"><span data-stu-id="53c1f-121">8</span></span></p></td>
<td><p><span data-ttu-id="53c1f-122">Utiliza sólo la columna de marcas de hora si está disponible (se generará un error en tiempo de ejecución si no hay ninguna columna de marcas de hora en el conjunto de resultados).</span><span class="sxs-lookup"><span data-stu-id="53c1f-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53c1f-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="53c1f-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="53c1f-124">32</span><span class="sxs-lookup"><span data-stu-id="53c1f-124">32</span></span></p></td>
<td><p><span data-ttu-id="53c1f-125">Utiliza una instrucción UPDATE para cada fila modificada.</span><span class="sxs-lookup"><span data-stu-id="53c1f-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

