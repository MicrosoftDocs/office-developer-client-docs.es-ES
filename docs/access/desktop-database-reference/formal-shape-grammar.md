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
# <a name="formal-shape-grammar"></a>Gramática de las formas formales

**Se aplica a:** Access 2013, Office 2013

Es la gramática formal para crear cualquier comando Shape:

  - Los términos gramáticos requeridos son cadenas de texto delimitadas por corchetes angulares ("\<\>").

  - Los términos opcionales están delimitados por corchetes (" \[ \] ").

  - Las alternativas se indican mediante una barra vertical ("|").

  - Las alternativas extensibles se indican mediante puntos suspensivos ("...").

  - *Alpha* indica una cadena de letras alfabéticas.

  - *Digit* indica una cadena de números.

  - *Unicode-digit* indica una cadena de dígitos Unicode.

Todos los demás términos son literales.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Término</p></th>
<th><p>Definición</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;comando shape&gt;</p></td>
<td><p>SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{ &lt; provider-command-text &gt; } |<br />
( &lt; comando shape ) &gt; |<br />
TABLE &lt; entrecomillado de nombre&gt; |<br />
&lt;entrecomillado-nombre&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;shape-action&gt;</p></td>
<td><p>APPEND &lt; aliased-field-list&gt; |</p>
<p>COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aliased-field&gt;</p></td>
<td><p>&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-exp&gt;</p></td>
<td><p>( &lt; relation-exp &gt; ) |</p>
<p>&lt;calculated-exp&gt; |</p>
<p>&lt;aggregate-exp&gt; |</p>
<p>&lt;new-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p>
<p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-list&gt;</p></td>
<td><p>&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;field-name &gt; TO &lt; child-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;child-ref&gt;</p></td>
<td><p>&lt;field-name&gt; |</p>
<p>PARAMETER &lt; param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;número&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos&gt;</p></td>
<td><p>&lt;field-name &gt; [, &lt; field-name &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>SUM( &lt; qualified-field-name &gt; ) |</p>
<p>AVG( &lt; qualified-field-name &gt; ) |</p>
<p>MIN( &lt; qualified-field-name &gt; ) |</p>
<p>MAX( &lt; qualified-field-name &gt; ) |</p>
<p>COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</p>
<p>STDEV( &lt; qualified-field-name &gt; ) |</p>
<p>ANY( &lt; qualified-field-name &gt; )</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC( &lt; expresión &gt; )</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-field-name&gt;</p></td>
<td><p>&lt;alias &gt; .[ &lt; alias &gt; ...] &lt; field-name&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;entrecomillado-nombre&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;field-name&gt;</p></td>
<td><p>&lt;alias entrecomillado &gt; [[AS] &lt; &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;entrecomillado-nombre&gt;</p></td>
<td><p>&quot;&lt;string&gt;&quot; |</p>
<p>' &lt; string &gt; ' |</p>
<p>[ &lt; string &gt; ] |</p>
<p>&lt;name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre completo&gt;</p></td>
<td><p>alias[.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;name&gt;</p></td>
<td><p>alpha [ alpha | digit | _ | # | : | ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;número&gt;</p></td>
<td><p>digit [digit...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>NUEVO &lt; tipo de campo &gt; [( número &lt; &gt; [, número &lt; &gt; ])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;tipo de campo&gt;</p></td>
<td><p>Un tipo de datos OLE DB o ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expresión&gt;</p></td>
<td><p>Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</p></td>
</tr>
</tbody>
</table>

