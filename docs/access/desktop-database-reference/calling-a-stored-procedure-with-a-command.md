---
title: Llamar a un procedimiento almacenado con un comando
TOCTitle: Calling a Stored Procedure with a Command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 573b847f53d3fc7ca07691e9a92d152598531bce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485011"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>Llamar a un procedimiento almacenado con un comando


**Se aplica a**: Access 2013 | Office 2013

También puede utilizar un comando cuando llame a un procedimiento almacenado. El código siguiente llama a un procedimiento almacenado en la base de datos de ejemplo Neptuno, denominado CustOrdersOrders, que se define como se indica a continuación:

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

Este procedimiento almacenado es similar al comando utilizado en [Parámetros del objeto Command](command-object-parameters.md), en cuanto a que toma un parámetro identificador de cliente y devuelve información sobre los pedidos de ese cliente. El código siguiente utiliza este procedimiento almacenado como origen para un **conjunto de registros** de ADO.

El uso del procedimiento almacenado le permite tener acceso a otra funcionalidad de ADO: el método **Refresh** de la colección **Parameters**. Utilizando este método, ADO puede rellenar automáticamente toda la información acerca de los parámetros que requiere el comando en tiempo de ejecución. El uso de esta técnica afecta negativamente al rendimiento, puesto que ADO debe consultar información acerca de los parámetros en el origen de datos.

Existen otras diferencias importantes entre el código de este ejemplo y el código en [Parámetros del objeto Command](command-object-parameters.md), donde los parámetros se introdujeron manualmente. En primer lugar, este código no establece la propiedad **Prepared** en **True** porque es un procedimiento almacenado de SQL Server y está precompilado por definición. En segundo lugar, la propiedad **CommandType** del objeto **Command** se cambió a **adCmdStoredProc** en el segundo ejemplo para informar a ADO de que el comando era un procedimiento almacenado.

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

