---
title: Crear y ejecutar un comando sencillo
TOCTitle: Creating and Executing a Simple Command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0446654a6ad39246289690c95f160bd77dcde19d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886266"
---
# <a name="creating-and-executing-a-simple-command"></a><span data-ttu-id="af881-102">Crear y ejecutar un comando sencillo</span><span class="sxs-lookup"><span data-stu-id="af881-102">Creating and Executing a Simple Command</span></span>


<span data-ttu-id="af881-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af881-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af881-p101">Aunque no es un uso habitual del objeto **Command**, el código siguiente muestra el método básico para usar este objeto\*\*\*\* con el fin de ejecutar un comando en un origen de datos. En este caso, se trata de un comando que devuelve filas, por tanto, devuelve los resultados de la ejecución del comando en un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="af881-p101">Though not a typical usage of the **Command** object, the following code shows the basic method of using the **Command** object to execute a command against a data source. In this case, it is a row-returning command, so it returns the results of the command execution into a **Recordset** object.</span></span>

```vb 
 
 'BeginBasicCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = 'ALFKI' " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print "ALFKI" 
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
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndBasicCmd 
```

<span data-ttu-id="af881-106">El comando que se va a ejecutar se especifica con la propiedad **CommandText**.</span><span class="sxs-lookup"><span data-stu-id="af881-106">The command to be executed is specified with the **CommandText** property.</span></span>


> [!NOTE]
> <span data-ttu-id="af881-107">Varios ejemplos de esta sección llamar a una función de utilidad, **GetNewConnection**, para establecer una conexión con el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="af881-107">Several examples in this section call a utility function, **GetNewConnection**, to establish a connection with the data provider.</span></span> <span data-ttu-id="af881-108">Para evitar la redundancia, aparece sólo una vez:</span><span class="sxs-lookup"><span data-stu-id="af881-108">To avoid redundancy, it is listed only once:</span></span>

```vb 
 
'BeginNewConnection 
Private Function GetNewConnection() As ADODB.Connection 
 Dim oCn As New ADODB.Connection 
 Dim sCnStr As String 
 
 sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Integrated Security='SSPI';Database='Northwind';" 
 oCn.Open sCnStr 
 
 If oCn.State = adStateOpen Then 
 Set GetNewConnection = oCn 
 End If 
 
End Function 
'EndNewConnection 
```

