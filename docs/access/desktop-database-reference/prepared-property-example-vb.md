---
title: Ejemplo de la propiedad Prepared (VB)
TOCTitle: Prepared Property Example (VB)
ms:assetid: d7332052-bf2e-f7d4-eb06-59ff8d68f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250081(v=office.15)
ms:contentKeyID: 48548000
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e4048a21b8d4815dda3bc7a4f9377b24e8fac02
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484595"
---
# <a name="prepared-property-example-vb"></a><span data-ttu-id="e02b7-102">Ejemplo de la propiedad Prepared (VB)</span><span class="sxs-lookup"><span data-stu-id="e02b7-102">Prepared Property Example (VB)</span></span>


<span data-ttu-id="e02b7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e02b7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e02b7-104">En este ejemplo se muestra la propiedad [Prepared](prepared-property-ado.md) al abrir dos objetos [Command](command-object-ado.md), uno preparado y otro sin preparar.</span><span class="sxs-lookup"><span data-stu-id="e02b7-104">This example demonstrates the [Prepared](prepared-property-ado.md) property by opening two [Command](command-object-ado.md) objects — one prepared and one not prepared.</span></span>

```vb 
 
'BeginPreparedVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim cmd1 As ADODB.Command 
 Dim cmd2 As ADODB.Command 
 
 Dim strCnxn As String 
 Dim strCmd As String 
 Dim sngStart As Single 
 Dim sngEnd As Single 
 Dim sngNotPrepared As Single 
 Dim sngPrepared As Single 
 Dim intLoop As Integer 
 
 ' Open a connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' Create two command objects for the same 
 ' command - one prepared and one not prepared 
 strCmd = "SELECT title, type FROM Titles ORDER BY type" 
 
 Set cmd1 = New ADODB.Command 
 Set cmd1.ActiveConnection = Cnxn 
 cmd1.CommandText = strCmd 
 
 Set cmd2 = New ADODB.Command 
 Set cmd2.ActiveConnection = Cnxn 
 cmd2.CommandText = strCmd 
 cmd2.Prepared = True 
 
 ' Set a timer, then execute the unprepared 
 ' command 20 times 
 sngStart = Timer 
 For intLoop = 1 To 20 
 cmd1.Execute 
 Next intLoop 
 sngEnd = Timer 
 sngNotPrepared = sngEnd - sngStart 
 
 ' Reset the timer, then execute the prepared 
 ' command 20 times 
 sngStart = Timer 
 For intLoop = 1 To 20 
 cmd2.Execute 
 Next intLoop 
 sngEnd = Timer 
 sngPrepared = sngEnd - sngStart 
 
 ' Display performance results 
 MsgBox "Performance Results:" & vbCr & _ 
 " Not Prepared: " & Format(sngNotPrepared, _ 
 "##0.000") & " seconds" & vbCr & _ 
 " Prepared: " & Format(sngPrepared, _ 
 "##0.000") & " seconds" 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Set cmd1 = Nothing 
 Set cmd2 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 Set cmd1 = Nothing 
 Set cmd2 = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndPreparedVB 
```
