---
title: Ejemplo del método NextRecordset (VB)
TOCTitle: NextRecordset Method Example (VB)
ms:assetid: f8d99670-3c28-1704-0ec1-34b06e7cd1b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250265(v=office.15)
ms:contentKeyID: 48548795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: adde158f073c991e4c6aadea8e2a39dbc89e0d6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486428"
---
# <a name="nextrecordset-method-example-vb"></a><span data-ttu-id="b238e-102">Ejemplo del método NextRecordset (VB)</span><span class="sxs-lookup"><span data-stu-id="b238e-102">NextRecordset Method Example (VB)</span></span>


<span data-ttu-id="b238e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b238e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b238e-104">En este ejemplo se utiliza el método [NextRecordset](nextrecordset-method-ado.md) para ver los datos de un conjunto de registros que utiliza una instrucción compuesta formada por tres instrucciones **SELECT**.</span><span class="sxs-lookup"><span data-stu-id="b238e-104">This example uses the [NextRecordset](nextrecordset-method-ado.md) method to view the data in a recordset that uses a compound command statement made up of three separate **SELECT** statements.</span></span>

```vb 
 
'BeginNextRecordsetVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim rstCompound As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim SQLCompound As String 
 
 Dim intCount As Integer 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open compound recordset 
 Set rstCompound = New ADODB.Recordset 
 SQLCompound = "SELECT * FROM Authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs" 
 rstCompound.Open SQLCompound, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' Display results from each SELECT statement 
 intCount = 1 
 Do Until rstCompound Is Nothing 
 Debug.Print "Contents of recordset #" & intCount 
 
 Do Until rstCompound.EOF 
 Debug.Print , rstCompound.Fields(0), rstCompound.Fields(1) 
 rstCompound.MoveNext 
 Loop 
 
 Set rstCompound = rstCompound.NextRecordset 
 intCount = intCount + 1 
 Loop 
 
 ' clean up 
 Cnxn.Close 
 Set rstCompound = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstCompound Is Nothing Then 
 If rstCompound.State = adStateOpen Then rstCompound.Close 
 End If 
 Set rstCompound = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndNextRecordsetVB 
```
