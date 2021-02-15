---
title: Propiedad Database.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21d775c0abac5d2afddd6b0930816c8d6d381ff0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295019"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="0797c-102">Propiedad Database.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="0797c-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="0797c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0797c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0797c-p101">Devuelve un valor que especifica la secuencia del criterio de ordenación en texto para comparación u ordenación de la cadena (sólo para áreas de trabajo de Microsoft Access). **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0797c-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0797c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0797c-106">Syntax</span></span>

<span data-ttu-id="0797c-107">*expresión* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="0797c-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="0797c-108">*expression* Variable que representa un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="0797c-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0797c-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0797c-109">Remarks</span></span>

<span data-ttu-id="0797c-110">El valor que se devuelve es una constante o valor **Long** que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0797c-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0797c-111">Constante</span><span class="sxs-lookup"><span data-stu-id="0797c-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0797c-112">Criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="0797c-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0797c-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-114">General (inglés, francés, alemán, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="0797c-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="0797c-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-118">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="0797c-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-120">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="0797c-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-122">Ruso</span><span class="sxs-lookup"><span data-stu-id="0797c-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-124">Checo</span><span class="sxs-lookup"><span data-stu-id="0797c-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-126">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="0797c-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-128">Griego</span><span class="sxs-lookup"><span data-stu-id="0797c-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-130">Hebreo</span><span class="sxs-lookup"><span data-stu-id="0797c-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="0797c-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-134">Islandés</span><span class="sxs-lookup"><span data-stu-id="0797c-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-136">Japonés</span><span class="sxs-lookup"><span data-stu-id="0797c-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="0797c-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-140">Neutro</span><span class="sxs-lookup"><span data-stu-id="0797c-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-142">Noruego o danés</span><span class="sxs-lookup"><span data-stu-id="0797c-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-144">Paradox internacional</span><span class="sxs-lookup"><span data-stu-id="0797c-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-146">Noruego o danés Paradox</span><span class="sxs-lookup"><span data-stu-id="0797c-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-148">Sueco o finés Paradox</span><span class="sxs-lookup"><span data-stu-id="0797c-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-149"><strong>dbSortEsish</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-150">Polaco</span><span class="sxs-lookup"><span data-stu-id="0797c-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="0797c-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-154">Español</span><span class="sxs-lookup"><span data-stu-id="0797c-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-156">Sueco o finés</span><span class="sxs-lookup"><span data-stu-id="0797c-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-158">Tailandés</span><span class="sxs-lookup"><span data-stu-id="0797c-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0797c-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-160">Turco</span><span class="sxs-lookup"><span data-stu-id="0797c-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0797c-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="0797c-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="0797c-162">No definido o desconocido</span><span class="sxs-lookup"><span data-stu-id="0797c-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0797c-163">El valor de la propiedad **CollatingOrder** corresponde al argumento de configuración regional del método **CreateDatabase** cuando se creó la base de datos o al método **CompactDatabase** cuando la base de datos se compactó más recientemente.</span><span class="sxs-lookup"><span data-stu-id="0797c-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="0797c-p102">Compruebe el valor de la propiedad **CollatingOrder** de un objeto **Database** o **Field** para determinar el método de comparación de cadenas para la base de datos o campo. Puede establecer la propiedad **CollatingOrder** de un objeto **Field** nuevo no anexado si desea que el valor del objeto **Field** sea diferente del valor del objeto **Database** que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="0797c-p102">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field. You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

