---
title: Ejemplo del método OpenSchema (VB)
TOCTitle: OpenSchema method example (VB)
ms:assetid: 02fe101a-c2df-6454-2cca-f5833e60fc03
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248797(v=office.15)
ms:contentKeyID: 48542973
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fccddd2f9566e0cb864a7a1cb4ccddb340fd0c5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873463"
---
# <a name="openschema-method-example-vb"></a><span data-ttu-id="5beec-102">Ejemplo del método OpenSchema (VB)</span><span class="sxs-lookup"><span data-stu-id="5beec-102">OpenSchema method example (VB)</span></span>


<span data-ttu-id="5beec-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5beec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5beec-104">En este ejemplo se utiliza el método [OpenSchema](openschema-method-ado.md) para mostrar el nombre y el tipo de cada tabla de la base de datos ***Pubs***.</span><span class="sxs-lookup"><span data-stu-id="5beec-104">This example uses the [OpenSchema](openschema-method-ado.md) method to display the name and type of each table in the ***Pubs*** database.</span></span>

```vb 
 
'BeginOpenSchemaVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub OpenSchemaX() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstSchema As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 Set rstSchema = Cnxn.OpenSchema(adSchemaTables) 
 
 Do Until rstSchema.EOF 
 Debug.Print "Table name: " & _ 
 rstSchema!TABLE_NAME & vbCr & _ 
 "Table type: " & rstSchema!TABLE_TYPE & vbCr 
 rstSchema.MoveNext 
 Loop 
 
 ' clean up 
 rstSchema.Close 
 Cnxn.Close 
 Set rstSchema = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstSchema Is Nothing Then 
 If rstSchema.State = adStateOpen Then rstSchema.Close 
 End If 
 Set rstSchema = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOpenSchemaVB 
```

<span data-ttu-id="5beec-105">En este ejemplo se especifica una tabla\_restricción de tipo de consulta en el argumento ***Criteria*** del método **OpenSchema** .</span><span class="sxs-lookup"><span data-stu-id="5beec-105">This example specifies a TABLE\_TYPE query constraint in the **OpenSchema** method ***Criteria*** argument.</span></span> <span data-ttu-id="5beec-106">Como resultado, se devuelven sólo la información de esquema de las vistas especificadas en la base de datos ***Pubs*** .</span><span class="sxs-lookup"><span data-stu-id="5beec-106">As a result, only schema information for the Views specified in the ***Pubs*** database are returned.</span></span> <span data-ttu-id="5beec-107">A continuación, se muestra en el ejemplo el nombre y el tipo de cada tabla.</span><span class="sxs-lookup"><span data-stu-id="5beec-107">The example then displays the name(s) and type(s) of each table(s).</span></span>

```vb 
 
'BeginOpenSchema2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn2 As ADODB.Connection 
 Dim rstSchema As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set Cnxn2 = New ADODB.Connection 
 strCnxn = "Provider=sqloledb;" & _ 
 "Data Source=MySqlServer;Initial Catalog=Pubs;Integrated Security=SSPI; " 
 Cnxn2.Open strCnxn 
 
 Set rstSchema = Cnxn2.OpenSchema(adSchemaTables, Array(Empty, Empty, Empty, "VIEW")) 
 
 Do Until rstSchema.EOF 
 Debug.Print "Table name: " & _ 
 rstSchema!TABLE_NAME & vbCr & _ 
 "Table type: " & rstSchema!TABLE_TYPE & vbCr 
 rstSchema.MoveNext 
 Loop 
 
 ' clean up 
 rstSchema.Close 
 Cnxn2.Close 
 Set rstSchema = Nothing 
 Set Cnxn2 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstSchema Is Nothing Then 
 If rstSchema.State = adStateOpen Then rstSchema.Close 
 End If 
 Set rstSchema = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOpenSchema2VB 
```

