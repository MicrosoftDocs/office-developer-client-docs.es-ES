---
title: Ejemplo de las propiedades Attributes y Name (VB)
TOCTitle: Attributes and Name Properties Example (VB)
ms:assetid: b049c03c-9add-48b7-6a0a-51d2507c8e33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249840(v=office.15)
ms:contentKeyID: 48547120
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95e0aaafdce4d7647666b66787a90ae24db53533
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483381"
---
# <a name="attributes-and-name-properties-example-vb"></a><span data-ttu-id="b68c3-102">Ejemplo de las propiedades Attributes y Name (VB)</span><span class="sxs-lookup"><span data-stu-id="b68c3-102">Attributes and Name Properties Example (VB)</span></span>


<span data-ttu-id="b68c3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b68c3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b68c3-p101">En este ejemplo se muestra el valor de la propiedad [Attributes](attributes-property-ado.md) de los objetos [Connection](connection-object-ado.md), [Field](field-object-ado.md) y [Property](property-object-ado.md). Se utiliza la propiedad [Name](name-property-ado.md) para mostrar el nombre de cada objeto **Field** y **Property**.</span><span class="sxs-lookup"><span data-stu-id="b68c3-p101">This example displays the value of the [Attributes](attributes-property-ado.md) property for [Connection](connection-object-ado.md), [Field](field-object-ado.md), and [Property](property-object-ado.md) objects. It uses the [Name](name-property-ado.md) property to display the name of each **Field** and **Property** object.</span></span>

```vb 
 
'BeginAttributesVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim rstEmployees As ADODB.Recordset 
 Dim strSQLEmployee As String 
 'record variables 
 Dim adoField As ADODB.Field 
 Dim adoProp As ADODB.Property 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' Open recordset 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployee = "employee" 
 rstEmployees.Open strSQLEmployee, Cnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines openign the recordset are identical as 
 'the default values for CursorType and LockType arguments match those shown 
 
 ' Display the attributes of the connection 
 Debug.Print "Connection attributes = " & Cnxn.Attributes 
 
 ' Display the property attributes of the Employee Table 
 Debug.Print "Property attributes:" 
 For Each adoProp In rstEmployees.Properties 
 Debug.Print " " & adoProp.Name & " = " & adoProp.Attributes 
 Next adoProp 
 
 ' Display the field attributes of the Employee Table 
 Debug.Print "Field attributes:" 
 For Each adoField In rstEmployees.Fields 
 Debug.Print " " & adoField.Name & " = " & adoField.Attributes 
 Next adoField 
 
 ' Display fields of the Employee Table which are NULLABLE 
 Debug.Print "NULLABLE Fields:" 
 For Each adoField In rstEmployees.Fields 
 If CBool(adoField.Attributes And adFldIsNullable) Then 
 Debug.Print " " & adoField.Name 
 End If 
 Next adoField 
 
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
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndAttributesVB 
```
