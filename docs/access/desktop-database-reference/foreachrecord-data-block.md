---
title: Bloque de datos ForEachRecord
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
# <a name="foreachrecord-data-block"></a>Bloque de datos ForEachRecord

**Se aplica a:** Access 2013, Office 2013

Un **bloque de datos ForEachRecord** repite un conjunto de instrucciones para cada registro de un dominio.

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
<th><p>Argumento</p></th>
<th><p>Necesario</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>In</strong></p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que identifica el dominio de los registros en los que se operará. El <em>argumento In</em> puede contener el nombre de la tabla, una consulta select o una instrucción SQL.</p><p><strong>NOTA:</strong>el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>No</p></td>
<td><p>Expresión de cadena usada para restringir el intervalo de datos en el que se realiza el bloque de datos <strong>ForEachRecord.</strong> Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE. Si se omite criteria, el bloque de datos <strong>ForEachRecord</strong> funciona en todo el dominio especificado por el <em>argumento In.</em> Cualquier campo que se incluya en los criterios debe ser también un campo del argumento <em>En</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>No</p></td>
<td><p>Cadena que proporciona un nombre alternativo para el dominio especificado por el <em>argumento In.</em> A menudo se usa para acortar el nombre de tabla de las referencias posteriores para evitar posibles referencias ambiguas. Si no se especifica <em>Alias,</em> se usará el nombre de la tabla o consulta como alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**.

