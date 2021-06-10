---
title: Gramática de las formas formales
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292324"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="04305-102">Gramática de las formas formales</span><span class="sxs-lookup"><span data-stu-id="04305-102">Formal shape grammar</span></span>

<span data-ttu-id="04305-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04305-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04305-104">Es la gramática formal para crear cualquier comando Shape:</span><span class="sxs-lookup"><span data-stu-id="04305-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="04305-105">Los términos gramáticos requeridos son cadenas de texto delimitadas por corchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="04305-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="04305-106">Los términos opcionales están delimitados por corchetes (" \[ \] ").</span><span class="sxs-lookup"><span data-stu-id="04305-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="04305-107">Las alternativas se indican mediante una barra vertical ("|").</span><span class="sxs-lookup"><span data-stu-id="04305-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="04305-108">Las alternativas extensibles se indican mediante puntos suspensivos ("...").</span><span class="sxs-lookup"><span data-stu-id="04305-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="04305-109">*Alpha* indica una cadena de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="04305-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="04305-110">*Digit* indica una cadena de números.</span><span class="sxs-lookup"><span data-stu-id="04305-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="04305-111">*Unicode-digit* indica una cadena de dígitos Unicode.</span><span class="sxs-lookup"><span data-stu-id="04305-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="04305-112">Todos los demás términos son literales.</span><span class="sxs-lookup"><span data-stu-id="04305-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04305-113">Término</span><span class="sxs-lookup"><span data-stu-id="04305-113">Term</span></span></p></th>
<th><p><span data-ttu-id="04305-114">Definición</span><span class="sxs-lookup"><span data-stu-id="04305-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04305-115">&lt;shape-command&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-116">SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-118">{ &lt; provider-command-text &gt; } |</span><span class="sxs-lookup"><span data-stu-id="04305-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="04305-119">( &lt; shape-command &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="04305-120">TABLE &lt; quoted-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="04305-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="04305-121">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-122">&lt;shape-action&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-123">APPEND &lt; aliased-field-list&gt; |</span><span class="sxs-lookup"><span data-stu-id="04305-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="04305-124">COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-125">&lt;aliased-field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-126">&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-127">&lt;aliased-field&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-128">&lt;alias field-exp &gt; [[AS] &lt; &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-129">&lt;field-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-130">( &lt; relation-exp &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="04305-131">&lt;calculated-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="04305-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="04305-132">&lt;aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="04305-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="04305-133">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-135">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="04305-136">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-137">&lt;relation-cond-list&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-138">&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</span><span class="sxs-lookup"><span data-stu-id="04305-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-140">&lt;field-name &gt; TO &lt; child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-141">&lt;child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-142">&lt;field-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="04305-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="04305-143">PARÁMETRO &lt; param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-145">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-146">&lt;field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-147">&lt;field-name &gt; [, &lt; field-name &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-148">&lt;aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-149">SUM( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="04305-150">AVG( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="04305-151">MIN( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="04305-152">MAX( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="04305-153">COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="04305-154">STDEV( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="04305-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="04305-155">ANY( &lt; qualified-field-name &gt; )</span><span class="sxs-lookup"><span data-stu-id="04305-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-156">&lt;calculated-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-157">CALC( &lt; expresión &gt; )</span><span class="sxs-lookup"><span data-stu-id="04305-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-158">&lt;qualified-field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-159">&lt;alias &gt; .[ &lt; alias &gt; ...] &lt; field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-161">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-162">&lt;field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-163">&lt;alias quoted-name &gt; [[AS] &lt; &gt; ]</span><span class="sxs-lookup"><span data-stu-id="04305-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-164">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-165">&quot;&lt;string&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="04305-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="04305-166">Cadena &lt; &gt; ' ' |</span><span class="sxs-lookup"><span data-stu-id="04305-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="04305-167">[ &lt; string &gt; ] |</span><span class="sxs-lookup"><span data-stu-id="04305-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="04305-168">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-169">&lt;nombre completo&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-170">alias[.alias...]</span><span class="sxs-lookup"><span data-stu-id="04305-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-171">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-172">alpha [ alpha | digit | _ | # | : | ...]</span><span class="sxs-lookup"><span data-stu-id="04305-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-173">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-174">digit [digit...]</span><span class="sxs-lookup"><span data-stu-id="04305-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-175">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-176">NUEVO &lt; tipo de campo &gt; [( number &lt; &gt; [, number &lt; &gt; ])]</span><span class="sxs-lookup"><span data-stu-id="04305-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-178">Un tipo de datos OLE DB o ADO.</span><span class="sxs-lookup"><span data-stu-id="04305-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04305-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-180">unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="04305-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04305-181">&lt;expresión&gt;</span><span class="sxs-lookup"><span data-stu-id="04305-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="04305-182">Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</span><span class="sxs-lookup"><span data-stu-id="04305-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

