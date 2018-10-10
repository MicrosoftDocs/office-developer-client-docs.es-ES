---
title: Ejemplo de las propiedades Provider y DefaultDatabase (VB)
TOCTitle: Provider and DefaultDatabase Properties Example (VB)
ms:assetid: 337b90e6-851d-2101-0671-50c4173aec13
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249104(v=office.15)
ms:contentKeyID: 48544107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 445315a3d5271d5566667916180a05de74d44980
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483992"
---
# <a name="provider-and-defaultdatabase-properties-example-vb"></a>Ejemplo de las propiedades Provider y DefaultDatabase (VB)


**Se aplica a**: Access 2013 | Office 2013

En este ejemplo se muestra la propiedad [Provider](provider-property-ado.md) al abrir tres objetos [Connection](connection-object-ado.md) mediante diferentes proveedores. También se utiliza la propiedad [DefaultDatabase](defaultdatabase-property-ado.md) para establecer la base de datos predeterminada del Proveedor Microsoft ODBC.

```vb 
 
'BeginProviderVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection strings 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim Cnxn3 As ADODB.Connection 
 Dim strCnxn As String 
 
 ' Open a connection using the Microsoft ODBC provider 
 Set Cnxn1 = New ADODB.Connection 
 Cnxn1.ConnectionString = "driver={SQL Server};server='MySqlServer';" & _ 
 "user id='MyUserID';password='MyPassword';" 
 Cnxn1.Open strCnxn 
 Cnxn1.DefaultDatabase = "Pubs" 
 
 ' Display the provider 
 MsgBox "Cnxn1 provider: " & Cnxn1.Provider 
 
 ' Open a connection using the Microsoft Jet provider 
 Set Cnxn2 = New ADODB.Connection 
 Cnxn2.Provider = "Microsoft.Jet.OLEDB.4.0" 
 Cnxn2.Open "C:\Program Files\Microsoft Office\Office\Samples\northwind.mdb", _ 
 "MyUserID", "MyPassword" 
 
 ' Display the provider. 
 MsgBox "Cnxn2 provider: " & Cnxn2.Provider 
 
 ' Open a connection using the Microsoft SQL Server provider 
 Set Cnxn3 = New ADODB.Connection 
 Cnxn3.Provider = "sqloledb" 
 Cnxn3.Open "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 ' Display the provider 
 MsgBox "Cnxn3 provider: " & Cnxn3.Provider 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Cnxn3.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Set Cnxn3 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Not Cnxn3 Is Nothing Then 
 If Cnxn3.State = adStateOpen Then Cnxn3.Close 
 End If 
 Set Cnxn3 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndProviderVB 
```

