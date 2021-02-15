---
title: Parámetros de evento (referencia de base de datos de escritorio de Access)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd4a99ec24a05084a2ae137ded3219c2997f8cf3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293318"
---
# <a name="event-parameters"></a><span data-ttu-id="bb07c-102">Parámetros de evento</span><span class="sxs-lookup"><span data-stu-id="bb07c-102">Event parameters</span></span>

<span data-ttu-id="bb07c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb07c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb07c-p101">Cada controlador de eventos tiene un parámetro de estado que controla el controlador de eventos. Para los eventos Complete, este parámetro también se utiliza para indicar si la operación que generó el evento se ha realizado correcta o incorrectamente. La mayoría de los eventos Complete también tienen un parámetro de error para proporcionar información sobre los errores que se hayan producido, así como uno o varios parámetros de objeto que hacen referencia al objeto ADO utilizado para llevar a cabo la operación. Por ejemplo, el evento [ExecuteComplete](executecomplete-event-ado.md) incluye parámetros de objeto para los objetos **Command**, **Recordset** y **Connection** asociados al evento. En el ejemplo siguiente de Microsoft Visual Basic, puede ver los objetos pCommand, pRecordset y pConnection que representan los objetos **Command**, **Recordset** y **Connection** usados por el método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="bb07c-p102">Excepto en el caso del objeto **Error**, se pasan los mismos parámetros a los eventos Will. De este modo, se puede examinar cada uno de los objetos que se van a utilizar en la operación que está pendiente y determinar si la operación puede completarse.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="bb07c-p103">Algunos controladores de eventos tienen un parámetro *Reason*, que proporciona información adicional sobre el motivo por el que se ha producido el evento. Por ejemplo, los eventos **WillMove** y **MoveComplete** pueden producirse debido a una llamada a cualquiera de los métodos de navegación (**MoveNext**, **MovePrevious**, etc.) o como resultado de una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p103">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred. For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="bb07c-113">Parámetro de estado</span><span class="sxs-lookup"><span data-stu-id="bb07c-113">Status Parameter</span></span>

<span data-ttu-id="bb07c-114">Cuando se llama a la rutina del controlador de eventos, el parámetro *Status* se establece en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bb07c-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb07c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bb07c-115">Value</span></span></p></th>
<th><p><span data-ttu-id="bb07c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb07c-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb07c-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="bb07c-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="bb07c-118">Se pasa tanto a los eventos Will como a los eventos Complete.</span><span class="sxs-lookup"><span data-stu-id="bb07c-118">Passed to both Will and Complete events.</span></span> <span data-ttu-id="bb07c-119">Este valor significa que la operación que ha causado el evento ha finalizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb07c-119">This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb07c-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="bb07c-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="bb07c-p105">Se pasa sólo a los eventos Complete. Este valor significa que la operación que provocó el evento no se ha realizado correctamente, o bien, que un evento Will canceló la operación. Compruebe el parámetro <em>Error</em> para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p105">Passed to Complete events only. This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation. Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb07c-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="bb07c-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="bb07c-125">Se pasa sólo a los eventos Will.</span><span class="sxs-lookup"><span data-stu-id="bb07c-125">Passed to Will events only.</span></span> <span data-ttu-id="bb07c-126">Este valor significa que la operación no puede ser cancelada por el evento Will.</span><span class="sxs-lookup"><span data-stu-id="bb07c-126">This value means that the operation cannot be canceled by the Will event.</span></span> <span data-ttu-id="bb07c-127">Es preciso que se lleve a cabo.</span><span class="sxs-lookup"><span data-stu-id="bb07c-127">It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb07c-p107">Si determina en el evento Will que la operación debe continuar, no modifique el parámetro *Status*. Sin embargo, mientras el valor del parámetro de estado de entrada no sea **adStatusCantDeny**, puede cancelar la operación que queda pendiente cambiando el valor de *Status* a **adStatusCancel**. Si lo hace, el evento Complete asociado a la operación tiene el parámetro *Status* establecido en **adStatusErrorsOccurred**. El objeto **Error** pasado al evento Complete contendrá el valor **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p107">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged. As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**. When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**. The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="bb07c-p108">Si ya no desea procesar un evento, puede establecer el valor de *Status* en **adStatusUnwantedEvent** y su aplicación ya no recibirá notificación de dicho suceso. No obstante, recuerde que algunos eventos pueden provocarse por varias razones. En ese caso, deberá especificar **adStatusUnwantedEvent** por cada posible razón. Por ejemplo, para dejar de recibir notificaciones de eventos **RecordChange** pendientes, deberá establecer el valor del parámetro *Status* en **adStatusUnwantedEvent** para **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** y **adRsnFirstChange** en el momento de producirse.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p108">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event. Remember, however, that some events can be raised for more than one reason. In that case, you must specify **adStatusUnwantedEvent** for each possible reason. For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb07c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bb07c-136">Value</span></span></p></th>
<th><p><span data-ttu-id="bb07c-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb07c-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb07c-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="bb07c-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="bb07c-139">Se solicita que este controlador de eventos deje de recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="bb07c-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb07c-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="bb07c-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="bb07c-141">Se solicita la cancelación de la operación que está a punto de realizarse.</span><span class="sxs-lookup"><span data-stu-id="bb07c-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="bb07c-142">Parámetro de error</span><span class="sxs-lookup"><span data-stu-id="bb07c-142">Error Parameter</span></span>

<span data-ttu-id="bb07c-p109">El parámetro *Error* es una referencia a un objeto [Error](error-object-ado.md) de ADO. Cuando el valor del parámetro *Status* está establecido en **adStatusErrorsOccurred**, el objeto **Error** contiene información detallada sobre por qué la operación no se ha realizado correctamente. Si el evento Will asociado a un evento Complete ha cancelado la operación estableciendo el valor del parámetro *Status* en **adStatusCancel**, el objeto de error siempre se establece en **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p109">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object. When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed. If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="bb07c-146">Parámetro de objeto</span><span class="sxs-lookup"><span data-stu-id="bb07c-146">Object Parameter</span></span>

<span data-ttu-id="bb07c-p110">Cada evento recibe uno o varios objetos que representan los objetos implicados en la operación. Por ejemplo, el evento **ExecuteComplete** recibe un objeto **Command**, un objeto **Recordset** y un objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="bb07c-149">Parámetro de motivo</span><span class="sxs-lookup"><span data-stu-id="bb07c-149">Reason Parameter</span></span>

<span data-ttu-id="bb07c-p111">El parámetro *Reason*, *adReason*, proporciona información adicional sobre por qué se ha producido el evento. Es posible que a los eventos con un parámetro *adReason* se llame varias veces, incluso para la misma operación, cada vez por un motivo diferente. Por ejemplo, se llama al controlador de eventos **WillChangeRecord** para las operaciones que están a punto de realizar o deshacer la inserción, la eliminación o la modificación de un registro. Si desea procesar un evento sólo cuando se produce por un motivo determinado, puede utilizar el parámetro *adReason* para filtrar las repeticiones que no son de su interés. Por ejemplo, si desea procesar los eventos de cambio de registro sólo cuando se producen porque se ha agregado un registro, podrá seguir este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="bb07c-p111">The *Reason* parameter, *adReason*, provides additional information about why the event occurred. Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason. For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record. If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in. For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

```vb 
 
' BeginEventExampleVB01 
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset) 
 If adReason = adRsnAddNew Then 
 ' Process event 
 '... 
 Else 
 ' Cancel event notification for all 
 ' other possible adReason values. 
 adStatus = adStatusUnwantedEvent 
 End If 
End Sub 
' EndEventExampleVB01 
```

<span data-ttu-id="bb07c-p112">En este caso, la notificación puede producirse por cada una de las demás razones. Sin embargo, se producirá sólo una vez por cada razón. Después de producirse la notificación una vez por cada razón, recibirá notificación sólo por la adición de un nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="bb07c-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="bb07c-158">En cambio, es necesario establecer el valor de *adStatus* en **adStatusUnwantedEvent** sólo una vez para solicitar que un controlador de eventos sin parámetro **adReason** deje de recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="bb07c-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

