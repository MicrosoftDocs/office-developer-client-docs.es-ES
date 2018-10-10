---
title: Database.CollatingOrder Property (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6101729af7f77e1451de240deece2bf789110fb7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485856"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="948fe-102">Database.CollatingOrder Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="948fe-102">Database.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="948fe-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="948fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="948fe-p101">Devuelve un valor que especifica la secuencia del criterio de ordenación en texto para comparación u ordenación de la cadena (sólo para áreas de trabajo de Microsoft Access). **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="948fe-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="948fe-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="948fe-106">Syntax</span></span>

<span data-ttu-id="948fe-107">*expresión* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="948fe-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="948fe-108">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="948fe-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="948fe-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="948fe-109">Remarks</span></span>

<span data-ttu-id="948fe-110">El valor que se devuelve es una constante o valor **Long** que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="948fe-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="948fe-111">Constante</span><span class="sxs-lookup"><span data-stu-id="948fe-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="948fe-112">Criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="948fe-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="948fe-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-114">General (inglés, francés, alemán, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="948fe-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="948fe-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-118">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="948fe-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-120">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="948fe-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-122">Ruso</span><span class="sxs-lookup"><span data-stu-id="948fe-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-124">Checo</span><span class="sxs-lookup"><span data-stu-id="948fe-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-126">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="948fe-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-128">Griego</span><span class="sxs-lookup"><span data-stu-id="948fe-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-130">Hebreo</span><span class="sxs-lookup"><span data-stu-id="948fe-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-132">Húngaro</span><span class="sxs-lookup"><span data-stu-id="948fe-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-134">Islandés</span><span class="sxs-lookup"><span data-stu-id="948fe-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-136">Japonés</span><span class="sxs-lookup"><span data-stu-id="948fe-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-138">Coreano</span><span class="sxs-lookup"><span data-stu-id="948fe-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="948fe-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-142">Noruego o danés</span><span class="sxs-lookup"><span data-stu-id="948fe-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="948fe-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-146">Noruego o danés Paradox</span><span class="sxs-lookup"><span data-stu-id="948fe-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-148">Sueco o finés Paradox</span><span class="sxs-lookup"><span data-stu-id="948fe-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-150">Polaco</span><span class="sxs-lookup"><span data-stu-id="948fe-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-152">Esloveno</span><span class="sxs-lookup"><span data-stu-id="948fe-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-154">Español</span><span class="sxs-lookup"><span data-stu-id="948fe-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-156">Sueco o finés</span><span class="sxs-lookup"><span data-stu-id="948fe-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-158">Tailandés</span><span class="sxs-lookup"><span data-stu-id="948fe-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948fe-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-160">Turco</span><span class="sxs-lookup"><span data-stu-id="948fe-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948fe-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="948fe-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="948fe-162">No definido o desconocido</span><span class="sxs-lookup"><span data-stu-id="948fe-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="948fe-163">El valor de la propiedad **CollatingOrder** corresponde al argumento locale del método **CreateDatabase** cuando se creó la base de datos o el método **CompactDatabase** cuando la base de datos se ha compactado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="948fe-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="948fe-p102">Compruebe el valor de la propiedad **CollatingOrder** de un objeto **Database** o **Field** para determinar el método de comparación de cadenas para la base de datos o campo. Puede establecer la propiedad **CollatingOrder** de un objeto **Field** nuevo no anexado si desea que el valor del objeto **Field** sea diferente del valor del objeto **Database** que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="948fe-p102">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field. You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

