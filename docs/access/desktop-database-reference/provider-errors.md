---
title: Errores de proveedor (referencia de escritorio de la base de datos de Access)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d176b08e35888afbbde8c5d485887c00e413d74d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947178"
---
# <a name="provider-errors"></a>Errores de proveedor


**Se aplica a**: Access 2013, Office 2013 

Cuando se produce un error de proveedor, se devuelve un error en tiempo de ejecución de -2147467259. Si recibe este error, revise la colección **Errors** del objeto **Connection** activo, que contendrá uno o más errores que describen lo qué ocurrió.

## <a name="the-ado-errors-collection"></a>La colección Errors de ADO

Dado que una operación de ADO determinada puede causar varios errores de proveedor, ADO expone una colección de objetos de error a través del objeto **Connection**. Esta colección no contiene ningún objeto si una operación se completa correctamente, y contiene uno o más objetos **Error** si algo fue mal y el proveedor generó uno o más errores. Examine cada objeto de error individual para determinar la causa exacta del error.

Cuando haya terminado de tratar los errores que se hayan producido, puede borrar la colección llamando al método **Clear**. Es especialmente importante borrar explícitamente la colección **Errors** antes de llamar al método **Resync**, **UpdateBatch** o **CancelBatch** para un objeto **Recordset**, al método **Open** para un objeto **Connection**, o de establecer la propiedad **Filter** para un objeto **Recordset**. Si borra la colección explícitamente, podrá tener la seguridad de que no quedan objetos **Error** en la colección de una operación anterior.

Algunas operaciones pueden generar tanto advertencias como errores. Las advertencias también se representan mediante objetos **Error** en la colección **Errors**. Cuando un proveedor agrega una advertencia a la colección, no genera un error en tiempo de ejecución. Revise la propiedad **Contar** de la colección **Errors** para determinar si una advertencia fue generada por una operación determinada. Si el recuento es uno o una cifra mayor, significa que se ha agregado un objeto **Error** a la colección. Una vez que haya determinado que la colección **Errors** contiene errores o advertencias, puede recorrer la colección en iteración y recuperar información acerca de cada uno de los objetos **Error** que contiene. En el siguiente ejemplo breve de Visual Basic, se muestra esto:

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

La rutina de control de errores incluye un bucle **For Each** que examina cada objeto de la colección **Errors**. En este ejemplo, simplemente acumula un mensaje para presentación. En un programa de trabajo, escribiría código para realizar una tarea adecuada para cada error, como cerrar todos los archivos abiertos y apagar el programa de una forma ordenada.

## <a name="the-error-object"></a>El objeto Error

Examinando un objeto **Error**, se puede determinar qué error se produjo y, lo que es más importante, la aplicación o el objeto que provocó el error. El objeto **Error** tiene las propiedades siguientes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Descripción</strong></p></td>
<td><p>Un texto que describe el error que se produjo.</p></td>
</tr>
<tr class="even">
<td><p><strong>ContextoDeAyuda (HelpContext), HelpFile</strong></p></td>
<td><p>Hace referencia al tema de Ayuda y al archivo de Ayuda que contienen una descripción del error que se produjo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>El número de error específico del proveedor.</p></td>
</tr>
<tr class="even">
<td><p><strong>Número</strong></p></td>
<td><p>Un entero largo que representa el número (de la lista de <strong>ErrorValueEnum</strong>) del error que se produjo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Indica el nombre del objeto o de la aplicación que generó un error.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Un código de error de cinco caracteres que devuelve el proveedor durante el proceso de una instrucción SQL.</p></td>
</tr>
</tbody>
</table>


El objeto **Error** de ADO es bastante similar al objeto **Err** estándar de Visual Basic. Sus propiedades describen el error producido. Además del número del error, también se reciben dos informaciones relacionadas. La propiedad **NativeError** contiene un número de error específico del proveedor que utilice. En el ejemplo anterior, el proveedor es el proveedor de Microsoft OLE DB para SQL Server, de forma que **NativeError** contendrá errores específicos de SQL Server. La propiedad **SQLState** consiste en un código de cinco letras que describe un error en una instrucción SQL.

## <a name="event-related-errors"></a>Errores relacionados con eventos

El objeto **Error** también se utiliza cuando se producen errores relacionados con un evento. Para determinar si un error se produjo en el proceso que desencadenó un evento de ADO, revise el objeto **Error** pasado como un parámetro de evento.

Si la operación que provoca un evento concluye correctamente, el parámetro *adStatus* del controlador de eventos se establecerá en *adStatusOK*. Por otra parte, si la operación que desencadenó el evento no se ejecutó correctamente, el parámetro *adStatus* se establece en *adStatusErrorsOccurred*. En ese caso, el parámetro *pError* contendrá un objeto **Error** que describe el error.

