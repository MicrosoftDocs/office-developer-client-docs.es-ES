---
<<<<<<< Título HEAD: TOCTitle ejemplo de propiedad ActiveConnection de catálogo (VB): ejemplo de propiedad ActiveConnection de catálogo (VB) === título: ejemplo de la propiedad ActiveConnection de Catalog (VB) TOCTitle: catálogo ActiveConnection ejemplo de la propiedad (VB)
>>>>>>> Master ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15) ms:contentKeyID: ms.date 48543348: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="catalog-activeconnection-property-example-vb"></a>Ejemplo de propiedad ActiveConnection de Catalog (VB)
=======
# <a name="catalog-activeconnection-property-example-vb"></a>Ejemplo de propiedad ActiveConnection de Catalog (VB)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Si se establece la propiedad [ActiveConnection](activeconnection-property-adox.md) en una conexión abierta válida, se "abre" el catálogo. Desde un catálogo abierto se puede tener acceso a los objetos de esquema que contiene el catálogo.

```vb 
 
    ' BeginOpenConnectionVB 
    Sub OpenConnection() 
    On Error GoTo OpenConnectionError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Debug.Print cat.Tables(0).Type 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    OpenConnectionError: 
    
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndOpenConnectionVB 
```

Si se establece la propiedad **ActiveConnection** en una cadena de conexión válida, también se "abre" el catálogo.

```vb
    ' BeginOpenConnection2VB 
    Sub Main() 
     On Error GoTo OpenConnectionWithStringError 
     Dim cat As New ADOX.Catalog 
     
     cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Debug.Print cat.Tables(0).Type 
     
     'Clean up 
     Set cat.ActiveConnection = Nothing 
     Exit Sub 
     
    OpenConnectionWithStringError: 
     Set cat = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndOpenConnection2VB
```
