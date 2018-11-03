---
title: RecordStatusEnum (enumeración) (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 662176616b267e2fe60b225a3d3def7418e7bcaf
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944357"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum (enumeración) (DAO)


**Se aplica a**: Access 2013, Office 2013

Se utiliza con la propiedad **RecordStatus** para indicar el estado de actualización del registro actual si forma parte de una actualización por lotes.

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
<td><p>dbRecordDBDeleted</p></td>
<td><p>4</p></td>
<td><p>El registro se ha eliminado localmente y en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3</p></td>
<td><p>El registro se ha eliminado, pero permanece todavía en la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordModified</p></td>
<td><p>1</p></td>
<td><p>El registro se ha modificado y no se ha actualizado en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2</p></td>
<td><p>El registro se ha insertado con el método <strong>AddNew</strong>, pero no se ha insertado todavía en la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(Valor predeterminado) El registro no se ha modificado o se ha actualizado correctamente.</p></td>
</tr>
</tbody>
</table>

