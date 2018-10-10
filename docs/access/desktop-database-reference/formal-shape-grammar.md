---
title: Gramática formal del comando Shape
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06548b96a3c23014f23b5123965476c5d1149b6d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486404"
---
# <a name="formal-shape-grammar"></a>Gramática formal del comando Shape


**Se aplica a**: Access 2013 | Office 2013

Es la gramática formal para crear cualquier comando Shape:

  - Los términos gramáticos requeridos son cadenas de texto delimitadas por corchetes angulares ("\<\>").

  - Los términos opcionales están delimitados por corchetes ("\[ \]").

  - Las alternativas se indican mediante una barra vertical ("|").

  - Las alternativas extensibles se indican mediante puntos suspensivos ("...").

  - *Alpha* indica una cadena de letras alfabéticas.

  - *Digit* indica una cadena de números.

  - *Unicode-digit* indica una cadena de dígitos unicode.

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
<td><p>&lt;comando Shape&gt;</p></td>
<td><p>FORMA [&lt;tabla exp&gt; [[AS] &lt;alias&gt;]] [&lt;acción de forma&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;tabla exp&gt;</p></td>
<td><p>{&lt;texto de comando de proveedor&gt;} |<br />
(&lt;comando shape&gt;) |<br />
TABLA &lt;nombre entre comillas&gt; |<br />
&lt;nombre entre comillas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;acción de forma&gt;</p></td>
<td><p>APPEND &lt;lista de campos con alias&gt; |</p>
<p>COMPUTE &lt;lista de campos con alias&gt; [BY &lt;lista de campos&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos con alias&gt;</p></td>
<td><p>&lt;campo de un alias&gt; [, &lt;campo sin suavizado... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;campo de un alias&gt;</p></td>
<td><p>&lt;campo exp&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;campo exp&gt;</p></td>
<td><p>(&lt;relation exp&gt;) |</p>
<p>&lt;exp calcula&gt; |</p>
<p>&lt;agregado exp&gt; |</p>
<p>&lt;nueva exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;tabla exp&gt; [[AS] &lt;alias&gt;]</p>
<p>&lt;tabla exp&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de condición de relaciones&gt;</p></td>
<td><p>&lt;relación-cond&gt; [, &lt;relation cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;condición de relación&gt;</p></td>
<td><p>&lt;nombre de campo&gt; para &lt;secundarios ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;secundarios ref&gt;</p></td>
<td><p>&lt;nombre de campo&gt; |</p>
<p>PARÁMETRO &lt;param ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;parámetros ref&gt;</p></td>
<td><p>&lt;número&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos&gt;</p></td>
<td><p>&lt;nombre de campo&gt; [, &lt;nombre de campo&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;agregado exp&gt;</p></td>
<td><p>SUMA (&lt;nombre de campo completo&gt;) |</p>
<p>AVG (&lt;nombre de campo completo&gt;) |</p>
<p>MIN (&lt;nombre de campo completo&gt;) |</p>
<p>MAX (&lt;nombre de campo completo&gt;) |</p>
<p>COUNT (&lt;alias completo&gt; | &lt;nombre completo&gt;) |</p>
<p>STDEV (&lt;nombre de campo completo&gt;) |</p>
<p>CUALQUIER (&lt;nombre de campo completo&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;exp calcula&gt;</p></td>
<td><p>CALC(&lt;expresión&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre de campo completo&gt;</p></td>
<td><p>&lt;alias&gt;. [&lt;alias&gt;...] &lt;nombre de campo&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;nombre entre comillas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre de campo&gt;</p></td>
<td><p>&lt;nombre entre comillas&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nombre entre comillas&gt;</p></td>
<td><p>&quot;&lt;cadena&gt;&quot; |</p>
<p>'&lt;cadena&gt;' |</p>
<p>[&lt;cadena&gt;] |</p>
<p>&lt;nombre&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre completo&gt;</p></td>
<td><p>alias [.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nombre&gt;</p></td>
<td><p>alfa [alpha | dígito | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;número&gt;</p></td>
<td><p>dígito [dígitos...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nueva exp&gt;</p></td>
<td><p>NUEVO &lt;tipo de campo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;tipo de campo&gt;</p></td>
<td><p>Un tipo de datos OLE DB o ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;cadena&gt;</p></td>
<td><p>Unicode-char [unicode char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</p></td>
</tr>
</tbody>
</table>

