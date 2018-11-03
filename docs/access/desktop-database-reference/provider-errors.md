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
# <a name="provider-errors"></a><span data-ttu-id="0e87a-102">Errores de proveedor</span><span class="sxs-lookup"><span data-stu-id="0e87a-102">Provider errors</span></span>


<span data-ttu-id="0e87a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e87a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="0e87a-p101">Cuando se produce un error de proveedor, se devuelve un error en tiempo de ejecución de -2147467259. Si recibe este error, revise la colección **Errors** del objeto **Connection** activo, que contendrá uno o más errores que describen lo qué ocurrió.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p101">When a provider error occurs, a run-time error of -2147467259 is returned. When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="0e87a-106">La colección Errors de ADO</span><span class="sxs-lookup"><span data-stu-id="0e87a-106">The ADO Errors Collection</span></span>

<span data-ttu-id="0e87a-p102">Dado que una operación de ADO determinada puede causar varios errores de proveedor, ADO expone una colección de objetos de error a través del objeto **Connection**. Esta colección no contiene ningún objeto si una operación se completa correctamente, y contiene uno o más objetos **Error** si algo fue mal y el proveedor generó uno o más errores. Examine cada objeto de error individual para determinar la causa exacta del error.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p102">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object. This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors. Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="0e87a-p103">Cuando haya terminado de tratar los errores que se hayan producido, puede borrar la colección llamando al método **Clear**. Es especialmente importante borrar explícitamente la colección **Errors** antes de llamar al método **Resync**, **UpdateBatch** o **CancelBatch** para un objeto **Recordset**, al método **Open** para un objeto **Connection**, o de establecer la propiedad **Filter** para un objeto **Recordset**. Si borra la colección explícitamente, podrá tener la seguridad de que no quedan objetos **Error** en la colección de una operación anterior.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p103">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method. It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object. By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="0e87a-p104">Algunas operaciones pueden generar tanto advertencias como errores. Las advertencias también se representan mediante objetos **Error** en la colección **Errors**. Cuando un proveedor agrega una advertencia a la colección, no genera un error en tiempo de ejecución. Revise la propiedad **Contar** de la colección **Errors** para determinar si una advertencia fue generada por una operación determinada. Si el recuento es uno o una cifra mayor, significa que se ha agregado un objeto **Error** a la colección. Una vez que haya determinado que la colección **Errors** contiene errores o advertencias, puede recorrer la colección en iteración y recuperar información acerca de cada uno de los objetos **Error** que contiene. En el siguiente ejemplo breve de Visual Basic, se muestra esto:</span><span class="sxs-lookup"><span data-stu-id="0e87a-p104">Some operations can generate warnings as well as errors. Warnings are also represented by **Error** objects in the **Errors** collection. When a provider adds a warning to the collection, it does not generate a run-time error. Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation. If the count is one or greater, an **Error** object has been added to the collection. Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains. The following short Visual Basic example demonstrates this:</span></span>

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

<span data-ttu-id="0e87a-p105">La rutina de control de errores incluye un bucle **For Each** que examina cada objeto de la colección **Errors**. En este ejemplo, simplemente acumula un mensaje para presentación. En un programa de trabajo, escribiría código para realizar una tarea adecuada para cada error, como cerrar todos los archivos abiertos y apagar el programa de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p105">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection. In this example, it simply accumulates a message for display. In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="0e87a-123">El objeto Error</span><span class="sxs-lookup"><span data-stu-id="0e87a-123">The Error Object</span></span>

<span data-ttu-id="0e87a-p106">Examinando un objeto **Error**, se puede determinar qué error se produjo y, lo que es más importante, la aplicación o el objeto que provocó el error. El objeto **Error** tiene las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="0e87a-p106">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error. The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e87a-126">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="0e87a-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="0e87a-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e87a-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e87a-128"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="0e87a-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="0e87a-129">Un texto que describe el error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="0e87a-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e87a-130"><strong>ContextoDeAyuda (HelpContext), HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="0e87a-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="0e87a-131">Hace referencia al tema de Ayuda y al archivo de Ayuda que contienen una descripción del error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="0e87a-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e87a-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="0e87a-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="0e87a-133">El número de error específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="0e87a-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e87a-134"><strong>Número</strong></span><span class="sxs-lookup"><span data-stu-id="0e87a-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="0e87a-135">Un entero largo que representa el número (de la lista de <strong>ErrorValueEnum</strong>) del error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="0e87a-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e87a-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="0e87a-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="0e87a-137">Indica el nombre del objeto o de la aplicación que generó un error.</span><span class="sxs-lookup"><span data-stu-id="0e87a-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e87a-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="0e87a-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="0e87a-139">Un código de error de cinco caracteres que devuelve el proveedor durante el proceso de una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="0e87a-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e87a-p107">El objeto **Error** de ADO es bastante similar al objeto **Err** estándar de Visual Basic. Sus propiedades describen el error producido. Además del número del error, también se reciben dos informaciones relacionadas. La propiedad **NativeError** contiene un número de error específico del proveedor que utilice. En el ejemplo anterior, el proveedor es el proveedor de Microsoft OLE DB para SQL Server, de forma que **NativeError** contendrá errores específicos de SQL Server. La propiedad **SQLState** consiste en un código de cinco letras que describe un error en una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p107">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object. Its properties describe the error that occurred. In addition to the number of the error, you also receive two related pieces of information. The **NativeError** property contains an error number specific to the provider you are using. In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server. The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="0e87a-146">Errores relacionados con eventos</span><span class="sxs-lookup"><span data-stu-id="0e87a-146">Event-Related Errors</span></span>

<span data-ttu-id="0e87a-p108">El objeto **Error** también se utiliza cuando se producen errores relacionados con un evento. Para determinar si un error se produjo en el proceso que desencadenó un evento de ADO, revise el objeto **Error** pasado como un parámetro de evento.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p108">The **Error** object is also used when event-related errors occur. You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="0e87a-p109">Si la operación que provoca un evento concluye correctamente, el parámetro *adStatus* del controlador de eventos se establecerá en *adStatusOK*. Por otra parte, si la operación que desencadenó el evento no se ejecutó correctamente, el parámetro *adStatus* se establece en *adStatusErrorsOccurred*. En ese caso, el parámetro *pError* contendrá un objeto **Error** que describe el error.</span><span class="sxs-lookup"><span data-stu-id="0e87a-p109">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*. On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*. In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

