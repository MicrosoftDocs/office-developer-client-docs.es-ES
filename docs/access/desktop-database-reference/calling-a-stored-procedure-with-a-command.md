---
title: Llamar a un procedimiento almacenado con un comando
TOCTitle: Calling a stored procedure with a command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6578dbfc50ae8ffeaa31f49b694b37ba5fd534e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296713"
---
# <a name="calling-a-stored-procedure-with-a-command"></a><span data-ttu-id="01b53-102">Llamar a un procedimiento almacenado con un comando</span><span class="sxs-lookup"><span data-stu-id="01b53-102">Calling a stored procedure with a command</span></span>


<span data-ttu-id="01b53-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01b53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01b53-p101">También puede utilizar un comando cuando llame a un procedimiento almacenado. El código siguiente llama a un procedimiento almacenado en la base de datos de ejemplo Neptuno, denominado CustOrdersOrders, que se define como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="01b53-p101">You can also use a command when calling a stored procedure. The following code calls a stored procedure in the Northwind sample database, called CustOrdersOrders, which is defined as follows:</span></span>

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

<span data-ttu-id="01b53-p102">Este procedimiento almacenado es similar al comando utilizado en [Parámetros del objeto Command](command-object-parameters.md), en cuanto a que toma un parámetro identificador de cliente y devuelve información sobre los pedidos de ese cliente. El código siguiente utiliza este procedimiento almacenado como origen para un **conjunto de registros** de ADO.</span><span class="sxs-lookup"><span data-stu-id="01b53-p102">This stored procedure is similar to the command used in [Command Object Parameters](command-object-parameters.md), in that it takes a customer ID parameter and returns information about that customer's orders. The code below uses this stored procedure as the source for an ADO **Recordset**.</span></span>

<span data-ttu-id="01b53-p103">El uso del procedimiento almacenado le permite tener acceso a otra funcionalidad de ADO: el método **Refresh** de la colección **Parameters**. Utilizando este método, ADO puede rellenar automáticamente toda la información acerca de los parámetros que requiere el comando en tiempo de ejecución. El uso de esta técnica afecta negativamente al rendimiento, puesto que ADO debe consultar información acerca de los parámetros en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="01b53-p103">Using the stored procedure allows you to access another capability of ADO: the **Parameters** collection **Refresh** method. By using this method, ADO can automatically fill in all information about the parameters required by the command at run time. There is a performance penalty in using this technique, because ADO must query the data source for the information about the parameters.</span></span>

<span data-ttu-id="01b53-p104">Existen otras diferencias importantes entre el código de este ejemplo y el código en [Parámetros del objeto Command](command-object-parameters.md), donde los parámetros se introdujeron manualmente. En primer lugar, este código no establece la propiedad **Prepared** en **True** porque es un procedimiento almacenado de SQL Server y está precompilado por definición. En segundo lugar, la propiedad **CommandType** del objeto **Command** se cambió a **adCmdStoredProc** en el segundo ejemplo para informar a ADO de que el comando era un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="01b53-p104">Other important differences exist between the code below and the code in [Command Object Parameters](command-object-parameters.md), where the parameters were entered manually. First, this code does not set the **Prepared** property to **True** because it is a SQL Server stored procedure and is precompiled by definition. Second, the **CommandType** property of the **Command** object changed to **adCmdStoredProc** in the second example to inform ADO that the command was a stored procedure.</span></span>

```vb 
 
'BeginAutoParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set CommandText equal to the stored procedure name. 
 objCmd.CommandText = "CustOrdersOrders" 
 objCmd.CommandType = adCmdStoredProc 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Automatically fill in parameter info from stored procedure. 
 objCmd.Parameters.Refresh 
 
 ' Set the param value. 
 objCmd(1) = "ALFKI" 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd(1) = "CACTU" 
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
'EndAutoParamCmd 
```

