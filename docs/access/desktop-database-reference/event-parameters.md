---
title: Parámetros de evento (referencia de escritorio de la base de datos de Access)
TOCTitle: Event Parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 023109586d13dc25846c8c145746aaf97fc22c15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888373"
---
# <a name="event-parameters"></a>Parámetros de evento


**Se aplica a**: Access 2013, Office 2013


Cada controlador de eventos tiene un parámetro de estado que controla el controlador de eventos. Para los eventos Complete, este parámetro también se utiliza para indicar si la operación que generó el evento se ha realizado correcta o incorrectamente. La mayoría de los eventos Complete también tienen un parámetro de error para proporcionar información sobre los errores que se hayan producido, así como uno o varios parámetros de objeto que hacen referencia al objeto ADO utilizado para llevar a cabo la operación. Por ejemplo, el evento [ExecuteComplete](executecomplete-event-ado.md) incluye parámetros de objeto para los objetos **Command**, **Recordset** y **Connection** asociados al evento. En el ejemplo siguiente de Microsoft Visual Basic, puede ver los objetos pCommand, pRecordset y pConnection que representan los objetos **Command**, **Recordset** y **Connection** usados por el método **Execute**.

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

Excepto en el caso del objeto **Error**, se pasan los mismos parámetros a los eventos Will. De este modo, se puede examinar cada uno de los objetos que se van a utilizar en la operación que está pendiente y determinar si la operación puede completarse.

Algunos controladores de eventos tienen un parámetro *Reason*, que proporciona información adicional sobre el motivo por el que se ha producido el evento. Por ejemplo, los eventos **WillMove** y **MoveComplete** pueden producirse debido a una llamada a cualquiera de los métodos de navegación (**MoveNext**, **MovePrevious**, etc.) o como resultado de una nueva consulta.

## <a name="status-parameter"></a>Parámetro de estado

Cuando se llama a la rutina del controlador de eventos, el parámetro *Status* se establece en uno de los valores siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>Se pasa tanto a los eventos Will como a los eventos Complete.

Este valor significa que la operación que ha causado el evento ha finalizado correctamente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Se pasa sólo a los eventos Complete. Este valor significa que la operación que provocó el evento no se ha realizado correctamente, o bien, que un evento Will canceló la operación. Compruebe el parámetro <em>Error</em> para obtener información más detallada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Se pasa sólo a los eventos Will.

Este valor significa que la operación no puede ser cancelada por el evento Will.

Es preciso que se lleve a cabo.</p></td>
</tr>
</tbody>
</table>


Si determina en el evento Will que la operación debe continuar, no modifique el parámetro *Status*. Sin embargo, mientras el valor del parámetro de estado de entrada no sea **adStatusCantDeny**, puede cancelar la operación que queda pendiente cambiando el valor de *Status* a **adStatusCancel**. Si lo hace, el evento Complete asociado a la operación tiene el parámetro *Status* establecido en **adStatusErrorsOccurred**. El objeto **Error** pasado al evento Complete contendrá el valor **adErrOperationCancelled**.

Si ya no desea procesar un evento, puede establecer el valor de *Status* en **adStatusUnwantedEvent** y su aplicación ya no recibirá notificación de dicho suceso. No obstante, recuerde que algunos eventos pueden provocarse por varias razones. En ese caso, deberá especificar **adStatusUnwantedEvent** por cada posible razón. Por ejemplo, para dejar de recibir notificaciones de eventos **RecordChange** pendientes, deberá establecer el valor del parámetro *Status* en **adStatusUnwantedEvent** para **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** y **adRsnFirstChange** en el momento de producirse.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>Se solicita que este controlador de eventos deje de recibir notificaciones.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Se solicita la cancelación de la operación que está a punto de realizarse.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Parámetro de error

El parámetro *Error* es una referencia a un objeto ADO [Error](error-object-ado.md) . Cuando el parámetro *Status* se establece en **adStatusErrorsOccurred**, el objeto **Error** contiene detalles acerca de por qué error en la operación. Si el evento Will asociado a un evento Complete ha cancelado la operación estableciendo el parámetro *Status* en **adStatusCancel**, el objeto de error siempre se establece en **adErrOperationCancelled**.

## <a name="object-parameter"></a>Parámetro de objeto

Cada evento recibe uno o varios objetos que representan los objetos implicados en la operación. Por ejemplo, el evento **ExecuteComplete** recibe un objeto **Command**, un objeto **Recordset** y un objeto **Connection**.

## <a name="reason-parameter"></a>Parámetro de motivo

El parámetro *Reason*, *adReason*, proporciona información adicional sobre por qué se ha producido el evento. Es posible que a los eventos con un parámetro *adReason* se llame varias veces, incluso para la misma operación, cada vez por un motivo diferente. Por ejemplo, se llama al controlador de eventos **WillChangeRecord** para las operaciones que están a punto de realizar o deshacer la inserción, la eliminación o la modificación de un registro. Si desea procesar un evento sólo cuando se produce por un motivo determinado, puede utilizar el parámetro *adReason* para filtrar las repeticiones que no son de su interés. Por ejemplo, si desea procesar los eventos de cambio de registro sólo cuando se producen porque se ha agregado un registro, podrá seguir este procedimiento:

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

En este caso, la notificación puede producirse por cada una de las demás razones. Sin embargo, se producirá sólo una vez por cada razón. Después de producirse la notificación una vez por cada razón, recibirá notificación sólo por la adición de un nuevo registro.

Por el contrario, debe establecer el *valor de adStatus* en **adStatusUnwantedEvent** sólo una vez para solicitar que un controlador de eventos sin parámetro **adReason** deje de recibir notificaciones de eventos.

