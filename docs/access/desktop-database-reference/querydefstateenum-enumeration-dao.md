---
title: Enumeración Querydefstateenum ((DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303321"
---
# <a name="querydefstateenum-enumeration-dao"></a>Enumeración Querydefstateenum ((DAO)


**Se aplica a:** Access 2013, Office 2013

Se utiliza con la propiedad **Prepare** para determinar el método utilizado para especificar cómo se debe preparar una consulta.

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
<td><p>dbQPrepare</p></td>
<td><p>1</p></td>
<td><p>(Valor predeterminado) La instrucción es preparada (es decir, se llama a la API de ODBC de SQLPrepare).</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>segundo</p></td>
<td><p>La instrucción no es preparada (es decir, se llama a la API de ODBC de SQLExecDirect).</p></td>
</tr>
</tbody>
</table>

