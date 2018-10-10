---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9538e1fb4a712b109e021512a3d28d299deaeb3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484809"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica opciones para abrir un [Record](record-object-ado.md). Estos valores se pueden combinar mediante OR.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adDelayFetchFields</strong></p></td>
<td><p>0 x 8000</p></td>
<td><p>Indica al proveedor que los campos asociados al objeto <strong>Record</strong> no es necesario que se recuperen inicialmente, sino que se pueden recuperar en el primer intento de obtener acceso al campo. El comportamiento predeterminado, indicado por la ausencia de esta marca, consiste en recuperar todos los campos de un objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indica al proveedor que la secuencia (Stream) predeterminada asociada con el objeto <strong>Record</strong> no es necesario que se recupere inicialmente. El comportamiento predeterminado, indicado por la ausencia de esta marca, consiste en recuperar la secuencia predeterminada asociada al objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indica que el objeto <strong>Record</strong> se abre en modo asincrónico.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Indica que la cadena de origen (Source) contiene texto de un comando que se debe ejecutar. Este valor es equivalente a la opción <strong>adCmdText</strong> en <strong>Recordset.Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Indica que no se especifica ninguna opción.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0 x 800000</p></td>
<td><p>Indica que si el origen apunta a un nodo que contiene un script ejecutable (tal como una página .ASP), entonces el <strong>Record</strong> abierto contendrá los resultados del script ejecutado. Este valor sólo es válido con registros que no son de tipo colección.</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

Estas constantes no tienen equivalentes ADO/WFC.

