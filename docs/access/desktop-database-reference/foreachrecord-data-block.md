---
title: ParaCadaRegistro (bloque de datos)
TOCTitle: ForEachRecord Data Block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d814c4996f7779066a4dcc4cc9cb97d5e294855b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486460"
---
# <a name="foreachrecord-data-block"></a>ParaCadaRegistro (bloque de datos)


**Se aplica a**: Access 2013 | Office 2013

Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio.


> [!NOTE]
> <P>[!NOTA] El bloque de datos <STRONG>ParaCadaRegistro</STRONG> solo está disponible en macros de datos.</P>



## <a name="setting"></a>Valores

La acción **ParaCadaRegistro** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obligatorio</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>En </strong></p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que identifica el dominio de registros que se va a funcionar en. El argumento <em>en</em> puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</p>

> [!NOTE]
> <P>El dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC .</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>No</p></td>
<td><p>Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos <strong>ParaCadaRegistro</strong> se lleva a cabo. Por ejemplo, criterios con frecuencia es equivalente a la cláusula WHERE en una expresión SQL, sin la palabra donde. Si se omite criterios, el bloque de datos <strong>ParaCadaRegistro</strong> funciona en todo el dominio especificado por el argumento <em>en</em> . Cualquier campo que se incluya en criterios debe ser también un campo de <em>en</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>No</p></td>
<td><p>Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento <em>en</em> . A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas. Si no se especifica el <em>Alias</em> , se usará el nombre de la tabla o consulta como el alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.

