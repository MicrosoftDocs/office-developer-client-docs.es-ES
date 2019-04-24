---
title: Bloque de datos ParaCadaRegistro
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292331"
---
# <a name="foreachrecord-data-block"></a>Bloque de datos ParaCadaRegistro

**Se aplica a:** Access 2013, Office 2013

Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio.

> [!NOTE]
> El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos.

## <a name="setting"></a>Configuración

La acción **ParaCadaRegistro** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatorio</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>A</strong></p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que identifica el dominio de los registros en los que se operará. El argumento <em>in</em> puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</p><p><strong>Nota</strong>: el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>No</p></td>
<td><p>Expresión de cadena que se usa para restringir el intervalo de datos en el que se ejecuta el bloque de datos <strong>ParaCadaRegistro</strong> . Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE. Si se omite criteria, el bloque de datos <strong>ParaCadaRegistro</strong> opera en todo el dominio especificado por el argumento <em>in</em> . Cualquier campo que se incluya en los criterios debe ser también un campo del argumento <em>En</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>No</p></td>
<td><p>Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento <em>in</em> . Se suele usar para acortar el nombre de la tabla para las referencias subsiguientes para evitar posibles referencias ambiguas. Si no se especifica ningún <em>alias</em> , se utilizará el nombre de la tabla o consulta como alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.

