---
<<<<<<< Título HEAD: ejemplo de propiedad Version (VB) TOCTitle: ejemplo de propiedad Version (VB) === título: ejemplo de la propiedad Version (VB) TOCTitle: ejemplo de la propiedad Version (VB)
>>>>>>> Master ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15) ms:contentKeyID: ms.date 48548968: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="version-property-example-vb"></a>Ejemplo de la propiedad Version (VB)
=======
# <a name="version-property-example-vb"></a>Ejemplo de la propiedad Version (VB)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

En este ejemplo se usa la propiedad [Version](version-property-ado.md) de un objeto [Connection](connection-object-ado.md) para mostrar la versión de ADO actual. También se usan varias propiedades dinámicas para mostrar:

  - El nombre DBMS y la versión actuales.

  - La versión de OLE DB.

  - El nombre del proveedor y la versión.

  - La versión de ODBC.

  - El nombre del controlador ODBC y la versión.

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

