---
title: Propiedad Field.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d64620ccf1c0d011c060ac829223041f49bde9d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925292"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="5c6d8-102">Propiedad Field.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c6d8-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="5c6d8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c6d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c6d8-p101">Devuelve un valor que especifica la secuencia del criterio de ordenación en texto para comparación u ordenación de la cadena (sólo para áreas de trabajo de Microsoft Access). **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6d8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c6d8-106">Syntax</span></span>

<span data-ttu-id="5c6d8-107">*expresión* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="5c6d8-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="5c6d8-108">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="5c6d8-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c6d8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c6d8-109">Remarks</span></span>

<span data-ttu-id="5c6d8-110">El valor que se devuelve es una constante o valor **Long** que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c6d8-111">Constante</span><span class="sxs-lookup"><span data-stu-id="5c6d8-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="5c6d8-112">Criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="5c6d8-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-114">General (inglés, francés, alemán, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="5c6d8-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="5c6d8-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-118">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="5c6d8-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-120">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="5c6d8-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-122">Ruso</span><span class="sxs-lookup"><span data-stu-id="5c6d8-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-124">Checo</span><span class="sxs-lookup"><span data-stu-id="5c6d8-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-126">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="5c6d8-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-128">Griego</span><span class="sxs-lookup"><span data-stu-id="5c6d8-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-130">Hebreo</span><span class="sxs-lookup"><span data-stu-id="5c6d8-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="5c6d8-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-134">Islandés</span><span class="sxs-lookup"><span data-stu-id="5c6d8-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-136">Japonés</span><span class="sxs-lookup"><span data-stu-id="5c6d8-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="5c6d8-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="5c6d8-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-142">Noruego o danés</span><span class="sxs-lookup"><span data-stu-id="5c6d8-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="5c6d8-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-146">Noruego o danés Paradox</span><span class="sxs-lookup"><span data-stu-id="5c6d8-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-148">Sueco o finés Paradox</span><span class="sxs-lookup"><span data-stu-id="5c6d8-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-150">Polaco</span><span class="sxs-lookup"><span data-stu-id="5c6d8-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="5c6d8-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-154">Español</span><span class="sxs-lookup"><span data-stu-id="5c6d8-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-156">Sueco o finés</span><span class="sxs-lookup"><span data-stu-id="5c6d8-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-158">Tailandés</span><span class="sxs-lookup"><span data-stu-id="5c6d8-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-160">Turco</span><span class="sxs-lookup"><span data-stu-id="5c6d8-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="5c6d8-162">No definido o desconocido</span><span class="sxs-lookup"><span data-stu-id="5c6d8-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c6d8-163">La disponibilidad de la propiedad **CollatingOrder** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c6d8-164">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="5c6d8-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="5c6d8-165">Entonces CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="5c6d8-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-166">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5c6d8-167">No admitido</span><span class="sxs-lookup"><span data-stu-id="5c6d8-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-168">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5c6d8-169">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c6d8-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-170">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5c6d8-171">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c6d8-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c6d8-172">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5c6d8-173">No admitido</span><span class="sxs-lookup"><span data-stu-id="5c6d8-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c6d8-174">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="5c6d8-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="5c6d8-175">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c6d8-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c6d8-176">El valor de la propiedad **CollatingOrder** corresponde al argumento locale del método **CreateDatabase** cuando se creó la base de datos o el método **CompactDatabase** cuando la base de datos se ha compactado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="5c6d8-p102">Los valores de las propiedades **CollatingOrder** y **Attributes** de un objeto **Field** en una colección **Fields** de un objeto **Index** determinan la secuencia y dirección del criterio de ordenación en un índice. Sin embargo, no se puede establecer una ordenación para un índice individual, sólo se puede establecer para una tabla completa.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

