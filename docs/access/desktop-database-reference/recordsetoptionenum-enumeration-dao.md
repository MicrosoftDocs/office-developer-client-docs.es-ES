---
title: RecordsetOptionEnum (enumeración) (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717282"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>RecordsetOptionEnum (enumeración) (DAO)


**Se aplica a**: Access 2013, Office 2013

Se usa con el método **OpenRecordset** para especificar las características de un nuevo objeto de **Recordset**.

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
<td><p>dbAppendOnly</p></td>
<td><p>8</p></td>
<td><p>Permite al usuario agregar nuevos registros al conjunto de registros de tipo dynaset, pero le impide leer los registros existentes.</p></td>
</tr>
<tr class="even">
<td><p>dbConsistent</p></td>
<td><p>32</p></td>
<td><p>Aplica actualizaciones sólo a los campos que no afectarán a otros registros en el conjunto de registros de tipo dynaset (tipo dynaset y snapshot únicamente).</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>Impide a otros usuario leer registros del conjunto de registros (tipo tabla únicamente).</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>Impide a otros usuario cambiar registros del conjunto de registros.</p></td>
</tr>
<tr class="odd">
<td><p>dbExecDirect</p></td>
<td><p>2048</p></td>
<td><p>Ejecuta la consulta sin llamar primero a la función de ODBC de SQLPrepare.</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p>128</p></td>
<td><p>Deshace las actualizaciones si se produce un error.</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>Crea un conjunto de registros de tipo snapshot que sólo admite desplazamientos hacia delante (tipo snapshot únicamente).</p></td>
</tr>
<tr class="even">
<td><p>dbInconsistent</p></td>
<td><p>16</p></td>
<td><p>Aplica actualizaciones a todos los campos del conjunto de registros de tipo dynaset, aunque otros registros se vean afectados (tipo dynaset y snapshot únicamente).</p></td>
</tr>
<tr class="odd">
<td><p>dbReadOnly</p></td>
<td><p>4</p></td>
<td><p>Abre el conjunto de registros en modo de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>Ejecuta la consulta de forma asincrónica.</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>Genera un error en tiempo de ejecución si otro usuario cambia datos que se estén editando (tipo dynaset únicamente).</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>Envía una instrucción SQL a una base de datos ODBC (tipo snapshot únicamente).</p></td>
</tr>
</tbody>
</table>

