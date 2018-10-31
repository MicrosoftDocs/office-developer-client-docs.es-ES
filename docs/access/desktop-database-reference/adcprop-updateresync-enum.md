---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 056e68456b3f5bcf30768b0a5a616467c8271a5a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861410"
---
# <a name="adcpropupdateresyncenum"></a>ADCPROP\_UPDATERESYNC\_ENUM

**Se aplica a**: Access 2013 | Office 2013

Especifica si al método [UpdateBatch](updatebatch-method-ado.md) le sigue una operación implícita del método [Resync](resync-method-ado.md) y, si es así, el ámbito de esa operación.

<br/>

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
<td><p><strong>adResyncAll</strong></p></td>
<td><p>15</p></td>
<td><p>Llama a <strong> Resync</strong> con el valor combinado del resto de los miembros ADCPROP_UPDATERESYNC_ENUM.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>Valor predeterminado. Intenta recuperar el nuevo valor de identidad de las columnas que se incrementan automáticamente o que genera el origen de datos, como los campos de autonumeración de Microsoft Jet o las columnas de identidad de Microsoft SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>Llama a <strong>Resync</strong> para todas las filas en las que la operación de actualización o eliminación generó un error debido a un conflicto de concurrencia.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8</p></td>
<td><p>Llama a <strong>Resync</strong> para todas las filas correctamente insertadas. Sin embargo, los valores de columna AutoIncrement no volvió a sincronizar. En su lugar, el contenido de las filas recién insertadas se volvió a sincronizar según el valor de clave principal existente. Si la clave principal es un valor con incremento automático, <strong>Resync</strong> no recuperará el contenido de la fila prevista. Para incrementar automáticamente los valores de la claves principales, llame a <strong>UpdateBatch</strong> con el valor combinado <strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>No llama a <strong>Resync</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>Llama a <strong>Resync</strong> para todas las filas correctamente actualizadas.</p></td>
</tr>
</tbody>
</table>

