---
title: Ejemplo de la propiedad Type (Field) (VB)
TOCTitle: Type Property Example (Field) (VB)
ms:assetid: ff9e26a8-898d-ec89-5093-69c66dbb05ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250314(v=office.15)
ms:contentKeyID: 48548966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0206bf366cfa5ef21e1816a2dba2eaad8dbe67ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485807"
---
# <a name="type-property-example-field-vb"></a><span data-ttu-id="74f4e-102">Ejemplo de la propiedad Type (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="74f4e-102">Type Property Example (Field) (VB)</span></span>


<span data-ttu-id="74f4e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="74f4e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="74f4e-p101">En este ejemplo se muestra la propiedad [Type](type-property-ado.md) al mostrar el nombre de la constante que corresponde al valor de la propiedad [Type](type-property-ado.md) de todos los objetos [Field](field-object-ado.md) de la tabla ***Employees***. Para que este procedimiento se ejecute se necesita la función FieldType.</span><span class="sxs-lookup"><span data-stu-id="74f4e-p101">This example demonstrates the [Type](type-property-ado.md) property by displaying the name of the constant that corresponds to the value of the [Type](type-property-ado.md) property of all the [Field](field-object-ado.md) objects in the ***Employees*** table. The FieldType function is required for this procedure to run.</span></span>

```vb 
 
'BeginTypeFieldVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstEmployees As ADODB.Recordset 
 Dim fld As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLEmployee As String 
 Dim FieldType As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employees table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployee = "employee" 
 rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 'rstEmployees.Open strSQLEmployee, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 ' the above two lines of code are identical 
 
 Debug.Print "Fields in Employees Table:" & vbCr 
 
 ' Enumerate Fields collection of Employees table 
 For Each fld In rstEmployees.Fields 
 ' translate field-type code to text 
 Select Case fld.Type 
 Case adChar 
 FieldType = "adChar" 
 Case adVarChar 
 FieldType = "adVarChar" 
 Case adSmallInt 
 FieldType = "adSmallInt" 
 Case adUnsignedTinyInt 
 FieldType = "adUnsignedTinyInt" 
 Case adDBTimeStamp 
 FieldType = "adDBTimeStamp" 
 End Select 
 ' show results 
 Debug.Print " Name: " & fld.Name & vbCr & _ 
 " Type: " & FieldType & vbCr 
 Next fld 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 Set fld = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndTypeFieldVB 
```
