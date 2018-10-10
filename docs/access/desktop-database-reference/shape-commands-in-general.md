---
title: Comandos Shape en general
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33570bec65de4ff88667ad90b591c4f288c86d96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485190"
---
# <a name="shape-commands-in-general"></a>Comandos Shape en general


**Se aplica a**: Access 2013 | Office 2013

La aplicación de forma a los datos define las columnas de un objeto **Recordset** con forma, las relaciones entre las entidades representadas por las columnas y la forma en que se rellena el objeto **Recordset** con datos.

Un objeto **Recordset** con forma puede constar de los siguientes tipos de columna.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de columna</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>data</p></td>
<td><p>Campos de un objeto <strong>Recordset</strong> devueltos por un comando de consulta a un proveedor de datos, una tabla o un objeto <strong>Recordset</strong> al que se ha aplicado forma anteriormente.</p></td>
</tr>
<tr class="even">
<td><p>capítulo</p></td>
<td><p>Referencia a otro objeto <strong>Recordset</strong>, que se denomina <em>capítulo</em>. Las columnas de capítulo permiten definir una relación de <em>objeto primario-objeto secundario</em> donde el <em>objeto primario</em> es el objeto <strong>Recordset</strong> que contiene la columna de capítulo y el <em>objeto secundario</em> es el objeto <strong>Recordset</strong> representado por el capítulo.</p></td>
</tr>
<tr class="odd">
<td><p>agregado</p></td>
<td><p>El valor de la columna se deriva ejecutando una <em>función de agregado</em> en todas las filas o una columna de todos las filas de un objeto <strong>Recordset</strong> secundario. (Vea Funciones de agregado en el tema siguiente, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funciones de agregado, función CALC y palabra clave NEW</a>.)</p></td>
</tr>
<tr class="even">
<td><p>expresión calculada</p></td>
<td><p>El valor de la columna se deriva calculando una expresión de Visual Basic para Aplicaciones en las columnas de la misma fila del objeto <strong>Recordset</strong>. La expresión es el argumento de la función CALC. (Vea Expresión calculada en el siguiente tema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funciones de agregado, función CALC y palabra clave NEW</a>, y en <a href="visual-basic-for-applications-functions.md">Funciones de Visual Basic para Aplicaciones</a>.)</p></td>
</tr>
<tr class="odd">
<td><p>nuevo</p></td>
<td><p>Campos creados vacíos, que se pueden rellenar con datos más adelante. La columna se define con la palabra clave NEW. (Vea la palabra clave NEW en el tema siguiente, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funciones de agregado, función CALC y palabra clave NEW</a>.)</p></td>
</tr>
</tbody>
</table>


Un comando Shape puede contener una cláusula que especifica un comando de consulta a un proveedor de datos subyacente que va a devolver un objeto **Recordset**. La sintaxis de la consulta depende de los requisitos del proveedor de datos subyacente. Normalmente será el Lenguaje de consulta estructurado (SQL), si bien ADO no requiere el uso de ningún lenguaje de consulta en particular.

Se puede usar una cláusula SQL JOIN para relacionar dos tablas; sin embargo, un objeto **Recordset** jerárquico puede representar la información más eficazmente. Cada fila de un objeto **Recordset** que se ha creado mediante JOIN repite de manera redundante la información de una de las tablas. Un objeto **Recordset** jerárquico tiene solo un objeto **Recordset** primario por cada uno de los múltiples objetos **Recordset** secundarios.

Los comandos Shape los pueden emitir los objetos **Recordset** o se pueden emitir estableciendo la propiedad [CommandText](commandtext-property-ado.md) del objeto [Command](command-object-ado.md) y, a continuación, llamando al método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).

Los comandos Shape se pueden anidar. Es decir, el *comando a primario* o el *comando a secundario* puede ser otro comando shape.

El proveedor de formas siempre devuelve un cursor de cliente, incluso si el usuario especifica una ubicación de cursor de ** adUseServer**.

Para obtener información sobre cómo desplazarse por un objeto **Recordset** jerárquico, vea [ Obtener acceso a las filas de un objeto Recordset jerárquico ](accessing-rows-in-a-hierarchical-recordset.md).

Para obtener información precisa sobre los comandos Shape sintácticamente correctos, vea [Gramática formal del comando Shape](formal-shape-grammar.md).

