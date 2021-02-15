---
title: Resumen del controlador de eventos de ADO
TOCTitle: ADO event handler summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c37c1257ad3f3cb046f7faf82ffcb93f067b1ff5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283376"
---
# <a name="ado-event-handler-summary"></a><span data-ttu-id="bbcef-102">Resumen de controladores de eventos de ADO</span><span class="sxs-lookup"><span data-stu-id="bbcef-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="bbcef-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbcef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbcef-p101">Existen dos objetos de ADO que pueden provocar eventos: el objeto [Connection](connection-object-ado.md) y el objeto [Recordset](recordset-object-ado.md). La familia **ConnectionEvent** (eventos de conexión) se relaciona con operaciones sobre el objeto **Connection**, mientras que la familia **RecordsetEvent** (eventos de conjunto de registros) tiene que ver con operaciones sobre el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bbcef-p101">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object. The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

- <span data-ttu-id="bbcef-106">**Eventos de conexión**. Son eventos que se generan cuando una transacción sobre una conexión comienza, se confirma (commit) o se deshace (rollback), cuando se ejecuta un [comando](command-object-ado.md), cuando se produce una advertencia durante una operación de **evento de conexión** o cuando se inicia o finaliza una **conexión**.</span><span class="sxs-lookup"><span data-stu-id="bbcef-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

- <span data-ttu-id="bbcef-107">**Eventos de conjunto de registros (recordset)**. Son eventos que se generan en operaciones de búsqueda asincrónicas, así como al desplazarse por las filas de un objeto **Recordset**, cambiar un campo de una fila de un **Recordset**, cambiar una fila de un **Recordset**, abrir un **Recordset** con un cursor de servidor, cerrar un **Recordset** o realizar cualquier otro cambio en el **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bbcef-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="bbcef-108">En las tablas siguientes, se resumen los eventos y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="bbcef-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbcef-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="bbcef-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="bbcef-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbcef-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbcef-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="bbcef-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="bbcef-112"><strong>Administración de transacciones</strong>. Notificación de que la transacción actual sobre la conexión se ha iniciado (begin), confirmado (commit) o deshecho (rollback).</span><span class="sxs-lookup"><span data-stu-id="bbcef-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbcef-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-114"><strong>Administración de conexiones</strong>. Notificación de que la conexión actual se iniciará, se ha iniciado o ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="bbcef-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbcef-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-116"><strong>Administración de la ejecución de comandos</strong>. Notificación de que la ejecución del comando actual sobre la conexión se iniciará o de que ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="bbcef-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbcef-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-118"><strong>Informativo</strong>. Notificación de que existe información adicional acerca de la operación actual.</span><span class="sxs-lookup"><span data-stu-id="bbcef-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="bbcef-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="bbcef-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="bbcef-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbcef-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbcef-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-p102"><strong>Estado de la recuperación</strong>. Notificación del progreso de una operación de recuperación de datos, o de que la operación se ha completado. Estos eventos sólo están disponibles si el objeto <strong>Recordset</strong>se abrió mediante un cursor de cliente.</span><span class="sxs-lookup"><span data-stu-id="bbcef-p102"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed. These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbcef-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-125"><strong>Administración de cambios en campos</strong>. Notificación de que el valor del campo actual cambiará o de que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="bbcef-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbcef-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-127"><strong>Administración del desplazamiento</strong>. Notificación de que la posición actual de fila en un objeto <strong>Recordset</strong> cambiará, cambió o alcanzó el final del <strong>conjunto de registros</strong>.</span><span class="sxs-lookup"><span data-stu-id="bbcef-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbcef-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-129"><strong>Administración de cambios en filas</strong>. Notificación de que algo en la fila actual del objeto <strong>Recordset</strong> cambiará o cambió.</span><span class="sxs-lookup"><span data-stu-id="bbcef-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbcef-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="bbcef-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="bbcef-131"><strong>Administración de cambios en conjuntos de registros</strong>. Notificación de que algo en el objeto <strong>Recordset</strong> actual cambiará o ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="bbcef-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

