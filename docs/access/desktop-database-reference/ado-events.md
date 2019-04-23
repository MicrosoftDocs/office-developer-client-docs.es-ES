---
title: Eventos de ActiveX Data Objects (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cc2ef73798dca18e00c42768fde78da2abdb56a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283341"
---
# <a name="ado-events"></a><span data-ttu-id="eed9b-102">Eventos de ADO</span><span class="sxs-lookup"><span data-stu-id="eed9b-102">ADO events</span></span>

<span data-ttu-id="eed9b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eed9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="eed9b-104">Evento</span><span class="sxs-lookup"><span data-stu-id="eed9b-104">Event</span></span></th>
<th><span data-ttu-id="eed9b-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="eed9b-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-107">Se utiliza (recibe una llamada) después de la operación <strong>BeginTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-109">Se utiliza (recibe una llamada) después de la operación <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-111">Se utiliza (recibe una llamada) después de iniciar una conexión.</span><span class="sxs-lookup"><span data-stu-id="eed9b-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-112"><a href="connectcomplete-and-disconnect-events-ado.md">Desconectar</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-113">Se utiliza (recibe una llamada) después de finalizar una conexión.</span><span class="sxs-lookup"><span data-stu-id="eed9b-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-115">Se usa (recibe una llamada) cuando se produce un intento de mover una fila más allá del final del objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-117">Se utiliza (recibe una llamada) después de que un comando ha terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="eed9b-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-119">Se usa (recibe una llamada) después de que todos los registros implicados en una operación asincrónica prolongada se recuperaron e insertado en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-121">Se usa (recibe una llamada) periódicamente durante una operación asincrónica prolongada para informar de cuántas filas se recuperaron e insertado actualmente en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-123">Se utiliza (recibe una llamada) después de que el valor de uno o varios objetos <strong>Field</strong> haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="eed9b-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-124"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-125">Se utiliza (recibe una llamada) siempre que se produce una advertencia durante una operación <strong>ConnectionEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-127">Se usa (recibe una llamada) después de un cambio de la posición actual en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-129">Se utiliza (recibe una llamada) después de cambiar uno o más registros.</span><span class="sxs-lookup"><span data-stu-id="eed9b-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-131">Se usa (recibe una llamada) después de un cambio en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-133">Se utiliza (recibe una llamada) después de la operación <strong>RollbackTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-135">Se utiliza (recibe una llamada) antes de que una operación pendiente cambie el valor de uno o varios objetos <strong>Field</strong> en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-137">Se usa (recibe una llamada) antes de cambiar uno o más registros (filas) en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-139">Se usa (recibe una llamada) antes de que una operación pendiente cambie el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-140"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-141">Se utiliza (recibe una llamada) antes de iniciar una conexión.</span><span class="sxs-lookup"><span data-stu-id="eed9b-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed9b-142"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-143">Se utiliza (recibe una llamada) antes de que un comando pendiente se ejecute en esta conexión y ofrece al usuario una oportunidad de examinar y modificar los parámetros de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="eed9b-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed9b-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="eed9b-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="eed9b-145">El evento <strong>WillMove</strong> recibe una llamada <em>antes</em> de que una operación pendiente cambie la posición actual en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="eed9b-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
