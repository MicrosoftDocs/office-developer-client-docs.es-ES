---
title: Parámetros del objeto Command
TOCTitle: Command Object Parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16e292c5700c653300e5493cbd613326621266c1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483796"
---
# <a name="command-object-parameters"></a><span data-ttu-id="a5953-102">Parámetros del objeto Command</span><span class="sxs-lookup"><span data-stu-id="a5953-102">Command Object Parameters</span></span>


<span data-ttu-id="a5953-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5953-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5953-p101">En el ejemplo siguiente, se muestra un uso más interesante para el objeto **Command**. En el ejemplo, el texto del comando SQL se ha modificado para hacerlo parametrizado. De este modo, se puede volver a utilizar el comando, pasando un valor diferente para el parámetro cada vez. Dado que la propiedad **Prepared** del objeto **Command** se ha establecido en **True**, ADO requerirá que el proveedor compile el comando especificado en **CommandText** antes de ejecutarlo por primera vez. También guardará el comando compilado en memoria. Esto ralentiza ligeramente la ejecución del comando la primera vez que se ejecuta, debido a la sobrecarga necesaria para prepararlo, pero tiene como consecuencia una mejora del rendimiento cada vez que se vuelve a llamar al comando posteriormente. Por tanto, los comandos sólo se deberían preparar si se van a utilizar más de una vez.</span><span class="sxs-lookup"><span data-stu-id="a5953-p101">A more interesting use for the **Command** object is shown in the next example, in which the text of the SQL command has been modified to make it parameterized. This makes it possible to reuse the command, passing in a different value for the parameter each time. Because the **Prepared** property on the **Command** object is set equal to **True**, ADO will require the provider to compile the command specified in **CommandText** before executing it for the first time. It also will retain the compiled command in memory. This slows the execution of the command slightly the first time it is executed because of the overhead required to prepare it, but results in a performance gain each time the command is called thereafter. Thus, commands should be prepared only if they will be used more than once.</span></span>

```vb 
 
'BeginManualParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set the CommandText as a parameterized SQL query. 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = ? " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Prepare command since we will be executing it more than once. 
 objCmd.Prepared = True 
 
 ' Create new parameter for CustomerID. Initial value is ALFKI. 
 Set objParm1 = objCmd.CreateParameter("CustId", adChar, _ 
 adParamInput, 5, "ALFKI") 
 objCmd.Parameters.Append objParm1 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd("CustId") = "CACTU" 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndManualParamCmd 
```

<span data-ttu-id="a5953-p102">No todos los proveedores admiten comandos preparados. Si el proveedor no admite la preparación de comandos, podría devolver un error en cuanto esta propiedad se estableciese en **True**. Si no devuelve un error, omite la solicitud de preparar el comando y establece la propiedad **Prepared** en **False**.</span><span class="sxs-lookup"><span data-stu-id="a5953-p102">Not all providers support prepared commands. If the provider does not support command preparation, it might return an error as soon as this property is set to **True**. If it does not return an error, it ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>
