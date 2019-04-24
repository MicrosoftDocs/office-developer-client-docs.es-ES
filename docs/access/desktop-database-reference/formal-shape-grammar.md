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
# <a name="formal-shape-grammar"></a><span data-ttu-id="8fb49-102">Gramática de las formas formales</span><span class="sxs-lookup"><span data-stu-id="8fb49-102">Formal shape grammar</span></span>

<span data-ttu-id="8fb49-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fb49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fb49-104">Es la gramática formal para crear cualquier comando Shape:</span><span class="sxs-lookup"><span data-stu-id="8fb49-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="8fb49-105">Los términos gramáticos requeridos son cadenas de texto delimitadas por corchetes angulares ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="8fb49-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="8fb49-106">Los términos opcionales están delimitados por corchetes\[ \]("").</span><span class="sxs-lookup"><span data-stu-id="8fb49-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="8fb49-107">Las alternativas se indican mediante una barra vertical ("|").</span><span class="sxs-lookup"><span data-stu-id="8fb49-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="8fb49-108">Las alternativas extensibles se indican mediante puntos suspensivos ("...").</span><span class="sxs-lookup"><span data-stu-id="8fb49-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="8fb49-109">*Alpha* indica una cadena de letras alfabéticas.</span><span class="sxs-lookup"><span data-stu-id="8fb49-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="8fb49-110">*Digit* indica una cadena de números.</span><span class="sxs-lookup"><span data-stu-id="8fb49-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="8fb49-111">*Unicode-digit* indica una cadena de dígitos Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fb49-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="8fb49-112">Todos los demás términos son literales.</span><span class="sxs-lookup"><span data-stu-id="8fb49-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fb49-113">Término</span><span class="sxs-lookup"><span data-stu-id="8fb49-113">Term</span></span></p></th>
<th><p><span data-ttu-id="8fb49-114">Definición</span><span class="sxs-lookup"><span data-stu-id="8fb49-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-115">&lt;comando de forma&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-116">Shape [&lt;Table-exp&gt; [[as] &lt;alias&gt;]] [&lt;Shape-Action&gt;]</span><span class="sxs-lookup"><span data-stu-id="8fb49-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-117">&lt;tabla-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-118">{&lt;Provider-Command-&gt;Text} |</span><span class="sxs-lookup"><span data-stu-id="8fb49-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="8fb49-119">(&lt;comando&gt;Shape) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="8fb49-120">Nombre &lt;entre comillas de tabla&gt; |</span><span class="sxs-lookup"><span data-stu-id="8fb49-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="8fb49-121">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-122">&lt;Shape-Action&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-123">ANEXAr &lt;lista de campos con alias&gt; |</span><span class="sxs-lookup"><span data-stu-id="8fb49-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="8fb49-124">CALCULAR &lt;aliased Field-List&gt; [por &lt;lista&gt;de campos]</span><span class="sxs-lookup"><span data-stu-id="8fb49-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-125">&lt;lista de campos con alias&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-126">&lt;campo&gt; con alias [, &lt;campo con alias... &gt;]</span><span class="sxs-lookup"><span data-stu-id="8fb49-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-127">&lt;campo con alias&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-128">&lt;Campo-Exp&gt; [[como] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="8fb49-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-129">&lt;Campo-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-130">(&lt;relación-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-131">&lt;calculado-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="8fb49-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="8fb49-132">&lt;agregado-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="8fb49-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="8fb49-133">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-135">&lt;Table-exp&gt; [[as] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="8fb49-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="8fb49-136">&lt;Table-exp&gt; [[as] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="8fb49-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-137">&lt;relación-Cond-List&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-138">&lt;relación-Cond&gt; [, &lt;relación-Cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="8fb49-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-139">&lt;relación-Cond&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-140">&lt;campo-nombre&gt; a &lt;Ref-Child&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-141">&lt;referencia-secundaria&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-142">&lt;nombre de campo&gt; |</span><span class="sxs-lookup"><span data-stu-id="8fb49-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="8fb49-143">PARÁMETRO &lt;param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-144">&lt;param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-145">&lt;números&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-146">&lt;lista de campos&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-147">&lt;nombre&gt; de campo [, &lt;nombre&gt;de campo]</span><span class="sxs-lookup"><span data-stu-id="8fb49-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-148">&lt;agregado-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-149">SUM (&lt;Qualified-Field-name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-150">AVG (&lt;Qualified-Field-name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-151">MÍN (&lt;Qualified-Field-name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-152">MAX (&lt;Qualified-Field-name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-153">COUNT (&lt;&gt; | &lt;nombre&gt;completo de alias cualificado) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-154">STDEV (&lt;Qualified-Field-name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="8fb49-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="8fb49-155">ANY (&lt;Qualified-Field-name&gt;)</span><span class="sxs-lookup"><span data-stu-id="8fb49-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-156">&lt;calculado-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-157">CALC (&lt;expresión&gt;)</span><span class="sxs-lookup"><span data-stu-id="8fb49-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-158">&lt;Qualified-Field-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-159">&lt;alias&gt;. [&lt;alias&gt;...] &lt;nombre de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-160">&lt;Seudónimo&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-161">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-162">&lt;nombre de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-163">&lt;quoted-&gt; Name [[as &lt;]&gt;alias]</span><span class="sxs-lookup"><span data-stu-id="8fb49-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-164">&lt;nombre entre comillas&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-165">&quot;&lt;cadena&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="8fb49-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="8fb49-166">'&lt;cadena&gt;' |</span><span class="sxs-lookup"><span data-stu-id="8fb49-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="8fb49-167">[&lt;cadena&gt;] |</span><span class="sxs-lookup"><span data-stu-id="8fb49-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="8fb49-168">&lt;denomina&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-169">&lt;nombre completo&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-170">alias [. alias...]</span><span class="sxs-lookup"><span data-stu-id="8fb49-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-171">&lt;denomina&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-172">alfa [alfa | dígito | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="8fb49-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-173">&lt;números&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-174">dígito [dígito...]</span><span class="sxs-lookup"><span data-stu-id="8fb49-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-175">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-176">New &lt;campo-tipo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</span><span class="sxs-lookup"><span data-stu-id="8fb49-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-177">&lt;tipo de campo&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-178">Un tipo de datos OLE DB o ADO.</span><span class="sxs-lookup"><span data-stu-id="8fb49-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fb49-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-180">Unicode-Char [Unicode-Char...]</span><span class="sxs-lookup"><span data-stu-id="8fb49-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fb49-181">&lt;expresión&gt;</span><span class="sxs-lookup"><span data-stu-id="8fb49-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="8fb49-182">Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</span><span class="sxs-lookup"><span data-stu-id="8fb49-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

