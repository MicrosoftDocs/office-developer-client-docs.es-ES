---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcce8eefad7fcad7dee7e46274ffc45125dc36c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485688"
---
# <a name="cursordriverenum-enumeration-dao"></a>CursorDriverEnum Enumeration (DAO)


**Se aplica a**: Access 2013 | Office 2013

Especifica el tipo de controlador de cursor.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUseClientBatchCursor</p></td>
<td><p>3</p></td>
<td><p>Utiliza siempre la biblioteca de cursores de FoxPro. Esta opción es necesaria para realizar actualizaciones por lotes.</p></td>
</tr>
<tr class="even">
<td><p>dbUseDefaultCursor</p></td>
<td><p>-1</p></td>
<td><p>(Valor predeterminado) Utiliza cursores de servidor si este los admite; en caso contrario, utiliza la biblioteca de cursores de ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseNoCursor</p></td>
<td><p>4</p></td>
<td><p>Abre todos los cursores (es decir, objetos <strong>Recordset</strong> ) como tipo de sólo avance, sólo lectura, con un tamaño de conjunto de filas de la 1. También conocido como &quot;consultas sin cursor.&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1</p></td>
<td><p>Utiliza siempre la biblioteca de cursores de ODBC. Esta opción proporciona mejor rendimiento para conjuntos de resultados pequeños, pero el rendimiento disminuye rápidamente en el caso de conjuntos de resultados más grandes.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseServerCursor</p></td>
<td><p>2</p></td>
<td><p>Utiliza siempre cursores de servidor. En la mayoría de las operaciones grandes, esta opción proporciona mejor rendimiento, pero puede dar lugar a un tráfico de red más intenso.</p></td>
</tr>
</tbody>
</table>

