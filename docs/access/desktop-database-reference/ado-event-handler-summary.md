---
title: Resumen de controladores de eventos de ADO
TOCTitle: ADO Event Handler Summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e47cf076c213707857285757d936d58bd153e7c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880603"
---
# <a name="ado-event-handler-summary"></a>Resumen de controladores de eventos de ADO


**Se aplica a**: Access 2013, Office 2013

Existen dos objetos de ADO que pueden provocar eventos: el objeto [Connection](connection-object-ado.md) y el objeto [Recordset](recordset-object-ado.md). La familia **ConnectionEvent** (eventos de conexión) se relaciona con operaciones sobre el objeto **Connection**, mientras que la familia **RecordsetEvent** (eventos de conjunto de registros) tiene que ver con operaciones sobre el objeto **Recordset**.

  - **Eventos de conexión**. Son eventos que se generan cuando una transacción sobre una conexión comienza, se confirma (commit) o se deshace (rollback), cuando se ejecuta un [comando](command-object-ado.md), cuando se produce una advertencia durante una operación de **evento de conexión** o cuando se inicia o finaliza una **conexión**.

  - **Eventos de conjunto de registros (recordset)**. Son eventos que se generan en operaciones de búsqueda asincrónicas, así como al desplazarse por las filas de un objeto **Recordset**, cambiar un campo de una fila de un **Recordset**, cambiar una fila de un **Recordset**, abrir un **Recordset** con un cursor de servidor, cerrar un **Recordset** o realizar cualquier otro cambio en el **Recordset**.

En las tablas siguientes, se resumen los eventos y sus descripciones.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A RollbackTransComplete <a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete,</p></td>
<td><p><strong>Administración de transacciones</strong>. Notificación de que la transacción actual sobre la conexión se ha iniciado (begin), confirmado (commit) o deshecho (rollback).</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, desconectar</a></p></td>
<td><p><strong>Administración de conexiones</strong>. Notificación de que la conexión actual se iniciará, se ha iniciado o ha finalizado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>Administración de la ejecución de comandos</strong>. Notificación de que la ejecución del comando actual sobre la conexión se iniciará o de que ha finalizado.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Informativo</strong>. Notificación de que existe información adicional acerca de la operación actual.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>RecordsetEvent</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p><strong>Estado de la recuperación</strong>. Notificación del progreso de una operación de recuperación de datos, o de que la operación se ha completado. Estos eventos sólo están disponibles si el objeto <strong>Recordset</strong>se abrió mediante un cursor de cliente.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></p></td>
<td><p><strong>Administración de cambios en campos</strong>. Notificación de que el valor del campo actual cambiará o de que ha cambiado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>Administración del desplazamiento</strong>. Notificación de que la posición actual de fila en un objeto <strong>Recordset</strong> cambiará, cambió o alcanzó el final del <strong>conjunto de registros</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></p></td>
<td><p><strong>Administración de cambios en filas</strong>. Notificación de que algo en la fila actual del objeto <strong>Recordset</strong> cambiará o cambió.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></p></td>
<td><p><strong>Administración de cambios en conjuntos de registros</strong>. Notificación de que algo en el objeto <strong>Recordset</strong> actual cambiará o ha cambiado.</p></td>
</tr>
</tbody>
</table>

