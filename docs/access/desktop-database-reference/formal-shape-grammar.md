---
title: Gramática formal de forma
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de4f2eca0b5dd607cb9d93cc7e90f4af0ba8d89
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945540"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="67e53-102">Gramática formal de forma</span><span class="sxs-lookup"><span data-stu-id="67e53-102">Formal shape grammar</span></span>

<span data-ttu-id="67e53-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67e53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67e53-104">Es la gramática formal para crear cualquier comando Shape:</span><span class="sxs-lookup"><span data-stu-id="67e53-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="67e53-105">Los términos gramáticos requeridos son cadenas de texto delimitadas por corchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="67e53-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="67e53-106">Los términos opcionales están delimitados por corchetes ("\[ \]").</span><span class="sxs-lookup"><span data-stu-id="67e53-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="67e53-107">Las alternativas se indican mediante una barra vertical ("|").</span><span class="sxs-lookup"><span data-stu-id="67e53-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="67e53-108">Las alternativas extensibles se indican mediante puntos suspensivos ("...").</span><span class="sxs-lookup"><span data-stu-id="67e53-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="67e53-109">*Alpha* indica una cadena de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="67e53-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="67e53-110">*Digit* indica una cadena de números.</span><span class="sxs-lookup"><span data-stu-id="67e53-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="67e53-111">*Unicode-digit* indica una cadena de dígitos unicode.</span><span class="sxs-lookup"><span data-stu-id="67e53-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="67e53-112">Todos los demás términos son literales.</span><span class="sxs-lookup"><span data-stu-id="67e53-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67e53-113">Término</span><span class="sxs-lookup"><span data-stu-id="67e53-113">Term</span></span></p></th>
<th><p><span data-ttu-id="67e53-114">Definición</span><span class="sxs-lookup"><span data-stu-id="67e53-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67e53-115">&lt;comando Shape&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-116">FORMA [&lt;tabla exp&gt; [[AS] &lt;alias&gt;]] [&lt;acción de forma&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-117">&lt;tabla exp&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-118">{&lt;texto de comando de proveedor&gt;} |</span><span class="sxs-lookup"><span data-stu-id="67e53-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="67e53-119">(&lt;comando shape&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="67e53-120">TABLA &lt;nombre entre comillas&gt; |</span><span class="sxs-lookup"><span data-stu-id="67e53-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="67e53-121">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-122">&lt;acción de forma&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-123">APPEND &lt;lista de campos con alias&gt; |</span><span class="sxs-lookup"><span data-stu-id="67e53-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="67e53-124">COMPUTE &lt;lista de campos con alias&gt; [BY &lt;lista de campos&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-125">&lt;lista de campos con alias&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-126">&lt;campo de un alias&gt; [, &lt;campo sin suavizado... &gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-127">&lt;campo de un alias&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-128">&lt;campo exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-129">&lt;campo exp&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-130">(&lt;relation exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-131">&lt;exp calcula&gt; |</span><span class="sxs-lookup"><span data-stu-id="67e53-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="67e53-132">&lt;agregado exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="67e53-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="67e53-133">&lt;nueva exp&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-135">&lt;tabla exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="67e53-136">&lt;tabla exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-137">&lt;lista de condición de relaciones&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-138">&lt;relación-cond&gt; [, &lt;relation cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="67e53-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-139">&lt;condición de relación&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-140">&lt;nombre de campo&gt; para &lt;secundarios ref&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-141">&lt;secundarios ref&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-142">&lt;nombre de campo&gt; |</span><span class="sxs-lookup"><span data-stu-id="67e53-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="67e53-143">PARÁMETRO &lt;param ref&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-144">&lt;parámetros ref&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-145">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-146">&lt;lista de campos&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-147">&lt;nombre de campo&gt; [, &lt;nombre de campo&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-148">&lt;agregado exp&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-149">SUMA (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-150">AVG (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-151">MIN (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-152">MAX (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-153">COUNT (&lt;alias completo&gt; | &lt;nombre completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-154">STDEV (&lt;nombre de campo completo&gt;) |</span><span class="sxs-lookup"><span data-stu-id="67e53-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="67e53-155">CUALQUIER (&lt;nombre de campo completo&gt;)</span><span class="sxs-lookup"><span data-stu-id="67e53-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-156">&lt;exp calcula&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-157">CALC(&lt;expresión&gt;)</span><span class="sxs-lookup"><span data-stu-id="67e53-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-158">&lt;nombre de campo completo&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-159">&lt;alias&gt;. [&lt;alias&gt;...] &lt;nombre de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-161">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-162">&lt;nombre de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-163">&lt;nombre entre comillas&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="67e53-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-164">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-165">&quot;&lt;cadena&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="67e53-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="67e53-166">'&lt;cadena&gt;' |</span><span class="sxs-lookup"><span data-stu-id="67e53-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="67e53-167">[&lt;cadena&gt;] |</span><span class="sxs-lookup"><span data-stu-id="67e53-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="67e53-168">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-169">&lt;nombre completo&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-170">alias [.alias...]</span><span class="sxs-lookup"><span data-stu-id="67e53-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-171">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-172">alfa [alpha | dígito | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="67e53-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-173">&lt;número&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-174">dígito [dígitos...]</span><span class="sxs-lookup"><span data-stu-id="67e53-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-175">&lt;nueva exp&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-176">NUEVO &lt;tipo de campo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</span><span class="sxs-lookup"><span data-stu-id="67e53-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-178">Un tipo de datos OLE DB o ADO.</span><span class="sxs-lookup"><span data-stu-id="67e53-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e53-179">&lt;cadena&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-180">Unicode-char [unicode char...]</span><span class="sxs-lookup"><span data-stu-id="67e53-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67e53-181">&lt;expresión&gt;</span><span class="sxs-lookup"><span data-stu-id="67e53-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="67e53-182">Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</span><span class="sxs-lookup"><span data-stu-id="67e53-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

