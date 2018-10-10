---
title: Eventos de ActiveX Data Objects (ADO)
TOCTitle: ADO Events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5938ed58e3b0074f69a4380fd4a0ac0be857084b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486386"
---
# <a name="ado-events"></a><span data-ttu-id="c8bd9-102">Eventos de ADO</span><span class="sxs-lookup"><span data-stu-id="c8bd9-102">ADO Events</span></span>


<span data-ttu-id="c8bd9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8bd9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-105">Se utiliza (recibe una llamada) después de la operación <strong>BeginTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-105">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-107">Se utiliza (recibe una llamada) después de la operación <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-107">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-109">Se utiliza (recibe una llamada) después de iniciar una conexión.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-109">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-110"><a href="connectcomplete-and-disconnect-events-ado.md">Desconectar</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-110"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-111">Se utiliza (recibe una llamada) después de finalizar una conexión.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-111">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-113">Se usa (recibe una llamada) cuando se produce un intento de mover una fila más allá del final del objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-113">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-115">Se utiliza (recibe una llamada) después de que un comando ha terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-115">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-117">Se usa (recibe una llamada) después de que todos los registros implicados en una operación asincrónica prolongada se recuperaron e insertado en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-117">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-119">Se usa (recibe una llamada) periódicamente durante una operación asincrónica prolongada para informar de cuántas filas se recuperaron e insertado actualmente en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-119">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-121">Se utiliza (recibe una llamada) después de que el valor de uno o varios objetos <strong>Field</strong> haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-121">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-122"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-122"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-123">Se utiliza (recibe una llamada) siempre que se produce una advertencia durante una operación <strong>ConnectionEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-123">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-125">Se usa (recibe una llamada) después de un cambio de la posición actual en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-125">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-127">Se utiliza (recibe una llamada) después de cambiar uno o más registros.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-127">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-129">Se usa (recibe una llamada) después de un cambio en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-129">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">A RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-131">Se utiliza (recibe una llamada) después de la operación <strong>RollbackTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-131">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-133">Se utiliza (recibe una llamada) antes de que una operación pendiente cambie el valor de uno o varios objetos <strong>Field</strong> en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-133">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-135">Se usa (recibe una llamada) antes de cambiar uno o más registros (filas) en el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-135">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-137">Se usa (recibe una llamada) antes de que una operación pendiente cambie el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-137">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-138"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-138"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-139">Se utiliza (recibe una llamada) antes de iniciar una conexión.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-139">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8bd9-140"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-140"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-141">Se utiliza (recibe una llamada) antes de que un comando pendiente se ejecute en esta conexión y ofrece al usuario una oportunidad de examinar y modificar los parámetros de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-141">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8bd9-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="c8bd9-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="c8bd9-143">El evento <strong>WillMove recibe</strong> se denomina <em>antes de</em> una operación pendiente cambie la posición actual en el <strong>conjunto de registros</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-143">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

