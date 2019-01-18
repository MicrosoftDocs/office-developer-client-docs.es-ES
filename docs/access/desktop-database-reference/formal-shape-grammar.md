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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708049"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="4b212-102">Gramática de las formas formales</span><span class="sxs-lookup"><span data-stu-id="4b212-102">Formal shape grammar</span></span>

<span data-ttu-id="4b212-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b212-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b212-104">Es la gramática formal para crear cualquier comando Shape:</span><span class="sxs-lookup"><span data-stu-id="4b212-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="4b212-105">Los términos gramáticos requeridos son cadenas de texto delimitadas por corchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="4b212-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="4b212-106">Los términos opcionales están delimitados por corchetes ("\[ \]").</span><span class="sxs-lookup"><span data-stu-id="4b212-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="4b212-107">Las alternativas se indican mediante una barra vertical ("|").</span><span class="sxs-lookup"><span data-stu-id="4b212-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="4b212-108">Las alternativas extensibles se indican mediante puntos suspensivos ("...").</span><span class="sxs-lookup"><span data-stu-id="4b212-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="4b212-109">*Alpha* indica una cadena de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="4b212-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="4b212-110">*Digit* indica una cadena de números.</span><span class="sxs-lookup"><span data-stu-id="4b212-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="4b212-111">*Unicode-digit* indica una cadena de dígitos unicode.</span><span class="sxs-lookup"><span data-stu-id="4b212-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="4b212-112">Todos los demás términos son literales.</span><span class="sxs-lookup"><span data-stu-id="4b212-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b212-113">Término</span><span class="sxs-lookup"><span data-stu-id="4b212-113">Term</span></span></p></th>
<th><p><span data-ttu-id="4b212-114">Definición</span><span class="sxs-lookup"><span data-stu-id="4b212-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b212-115">&lt;comando Shape&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-116">FORMA [&lt;tabla exp&gt; [[AS] &lt;alias&gt;]] [&lt;acción de forma&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-117">&lt;tabla exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-118">{&lt;texto de comando de proveedor&gt;} |</span><span class="sxs-lookup"><span data-stu-id="4b212-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="4b212-119">(&lt;comando shape&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="4b212-120">TABLA &lt;nombre entre comillas&gt; |</span><span class="sxs-lookup"><span data-stu-id="4b212-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="4b212-121">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-122">&lt;acción de forma&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-123">APPEND &lt;lista de campos con alias&gt; |</span><span class="sxs-lookup"><span data-stu-id="4b212-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="4b212-124">COMPUTE &lt;lista de campos con alias&gt; [BY &lt;lista de campos&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-125">&lt;lista de campos con alias&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-126">&lt;campo de un alias&gt; [, &lt;campo sin suavizado... &gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-127">&lt;campo de un alias&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-128">&lt;campo exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-129">&lt;campo exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-130">(&lt;relation exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-131">&lt;exp calcula&gt; |</span><span class="sxs-lookup"><span data-stu-id="4b212-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="4b212-132">&lt;agregado exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="4b212-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="4b212-133">&lt;nueva exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-135">&lt;tabla exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="4b212-136">&lt;tabla exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-137">&lt;lista de condición de relaciones&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-138">&lt;relación-cond&gt; [, &lt;relation cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="4b212-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-139">&lt;condición de relación&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-140">&lt;nombre de campo&gt; para &lt;secundarios ref&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-141">&lt;secundarios ref&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-142">&lt;nombre de campo&gt; |</span><span class="sxs-lookup"><span data-stu-id="4b212-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="4b212-143">PARÁMETRO &lt;param ref&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-144">&lt;parámetros ref&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-145">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-146">&lt;lista de campos&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-147">&lt;nombre de campo&gt; [, &lt;nombre de campo&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-148">&lt;agregado exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-149">SUMA (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-150">AVG (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-151">MIN (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-152">MAX (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-153">COUNT (&lt;alias completo&gt; | &lt;nombre completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-154">STDEV (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4b212-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4b212-155">CUALQUIER (&lt;nombre de campo completo&gt;)</span><span class="sxs-lookup"><span data-stu-id="4b212-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-156">&lt;exp calcula&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-157">CALC(&lt;expresión&gt;)</span><span class="sxs-lookup"><span data-stu-id="4b212-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-158">&lt;nombre de campo completo&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-159">&lt;alias&gt;. [&lt;alias&gt;...] &lt;nombre de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-161">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-162">&lt;nombre de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-163">&lt;nombre entre comillas&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="4b212-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-164">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-165">&quot;&lt;cadena&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="4b212-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="4b212-166">'&lt;cadena&gt;' |</span><span class="sxs-lookup"><span data-stu-id="4b212-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="4b212-167">[&lt;cadena&gt;] |</span><span class="sxs-lookup"><span data-stu-id="4b212-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="4b212-168">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-169">&lt;nombre completo&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-170">alias [.alias...]</span><span class="sxs-lookup"><span data-stu-id="4b212-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-171">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-172">alfa [alpha | dígito | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="4b212-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-173">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-174">dígito [dígitos...]</span><span class="sxs-lookup"><span data-stu-id="4b212-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-175">&lt;nueva exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-176">NUEVO &lt;tipo de campo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</span><span class="sxs-lookup"><span data-stu-id="4b212-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-178">Un tipo de datos OLE DB o ADO.</span><span class="sxs-lookup"><span data-stu-id="4b212-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b212-179">&lt;cadena&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-180">Unicode-char [unicode char...]</span><span class="sxs-lookup"><span data-stu-id="4b212-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b212-181">&lt;expresión&gt;</span><span class="sxs-lookup"><span data-stu-id="4b212-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b212-182">Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</span><span class="sxs-lookup"><span data-stu-id="4b212-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

