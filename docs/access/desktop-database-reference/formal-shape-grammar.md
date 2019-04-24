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

  - Los términos opcionales están delimitados por corchetes\[ \]("").

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
<td><p>&lt;comando de forma&gt;</p></td>
<td><p>Shape [&lt;Table-exp&gt; [[as] &lt;alias&gt;]] [&lt;Shape-Action&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;tabla-exp&gt;</p></td>
<td><p>{&lt;Provider-Command-&gt;Text} |<br />
(&lt;comando&gt;Shape) |<br />
Nombre &lt;entre comillas de tabla&gt; |<br />
&lt;nombre entre comillas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Shape-Action&gt;</p></td>
<td><p>ANEXAr &lt;lista de campos con alias&gt; |</p>
<p>CALCULAR &lt;aliased Field-List&gt; [por &lt;lista&gt;de campos]</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos con alias&gt;</p></td>
<td><p>&lt;campo&gt; con alias [, &lt;campo con alias... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;campo con alias&gt;</p></td>
<td><p>&lt;Campo-Exp&gt; [[como] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Campo-Exp&gt;</p></td>
<td><p>(&lt;relación-exp&gt;) |</p>
<p>&lt;calculado-exp&gt; |</p>
<p>&lt;agregado-exp&gt; |</p>
<p>&lt;New-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;Table-exp&gt; [[as] &lt;alias&gt;]</p>
<p>&lt;Table-exp&gt; [[as] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relación-Cond-List&gt;</p></td>
<td><p>&lt;relación-Cond&gt; [, &lt;relación-Cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relación-Cond&gt;</p></td>
<td><p>&lt;campo-nombre&gt; a &lt;Ref-Child&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;referencia-secundaria&gt;</p></td>
<td><p>&lt;nombre de campo&gt; |</p>
<p>PARÁMETRO &lt;param-Ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-Ref&gt;</p></td>
<td><p>&lt;números&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;lista de campos&gt;</p></td>
<td><p>&lt;nombre&gt; de campo [, &lt;nombre&gt;de campo]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;agregado-exp&gt;</p></td>
<td><p>SUM (&lt;Qualified-Field-name&gt;) |</p>
<p>AVG (&lt;Qualified-Field-name&gt;) |</p>
<p>MÍN (&lt;Qualified-Field-name&gt;) |</p>
<p>MAX (&lt;Qualified-Field-name&gt;) |</p>
<p>COUNT (&lt;&gt; | &lt;nombre&gt;completo de alias cualificado) |</p>
<p>STDEV (&lt;Qualified-Field-name&gt;) |</p>
<p>ANY (&lt;Qualified-Field-name&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculado-exp&gt;</p></td>
<td><p>CALC (&lt;expresión&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Qualified-Field-Name&gt;</p></td>
<td><p>&lt;alias&gt;. [&lt;alias&gt;...] &lt;nombre de campo&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Seudónimo&gt;</p></td>
<td><p>&lt;nombre entre comillas&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre de campo&gt;</p></td>
<td><p>&lt;quoted-&gt; Name [[as &lt;]&gt;alias]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nombre entre comillas&gt;</p></td>
<td><p>&quot;&lt;cadena&gt;&quot; |</p>
<p>'&lt;cadena&gt;' |</p>
<p>[&lt;cadena&gt;] |</p>
<p>&lt;denomina&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre completo&gt;</p></td>
<td><p>alias [. alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;denomina&gt;</p></td>
<td><p>alfa [alfa | dígito | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;números&gt;</p></td>
<td><p>dígito [dígito...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;New-exp&gt;</p></td>
<td><p>New &lt;campo-tipo&gt; [(&lt;número&gt; [, &lt;número&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;tipo de campo&gt;</p></td>
<td><p>Un tipo de datos OLE DB o ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>Unicode-Char [Unicode-Char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expresión&gt;</p></td>
<td><p>Una expresión de Visual Basic para Aplicaciones cuyos operandos son otras columnas que no sean CALC en la misma fila.</p></td>
</tr>
</tbody>
</table>

