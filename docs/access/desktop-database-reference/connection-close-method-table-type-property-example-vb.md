---
<span data-ttu-id="de319-101"><<<<<<< Título HEAD: método Close de Connection, TOCTitle de ejemplo de propiedad de tipo tabla (VB): método Close de Connection, ejemplo de propiedad de tipo tabla (VB) === título: método Close de Connection, ejemplo de la propiedad tipo de Table (VB) TOCTitle: Método Close de Connection, ejemplo de la propiedad tipo de Table (VB)</span><span class="sxs-lookup"><span data-stu-id="de319-101"><<<<<<< HEAD title: Connection Close Method, Table Type Property Example (VB) TOCTitle: Connection Close Method, Table Type Property Example (VB) ======= title: Connection Close Method, Table Type property example (VB) TOCTitle: Connection Close Method, Table Type property example (VB)</span></span>
>>>>>>> <span data-ttu-id="de319-102">Master ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) ms:contentKeyID: ms.date 48547754: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="de319-102">master ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) ms:contentKeyID: 48547754 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="de319-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="de319-103"><<<<<<< HEAD</span></span>
# <a name="connection-close-method-table-type-property-example-vb"></a><span data-ttu-id="de319-104">Ejemplo de método Close de Connection, propiedad Tipo de Table (VB)</span><span class="sxs-lookup"><span data-stu-id="de319-104">Connection Close Method, Table Type Property Example (VB)</span></span>
=======
# <a name="connection-close-method-table-type-property-example-vb"></a><span data-ttu-id="de319-105">Método Close de Connection, ejemplo de la propiedad tipo de Table (VB)</span><span class="sxs-lookup"><span data-stu-id="de319-105">Connection Close Method, Table Type property example (VB)</span></span>
>>>>>>> <span data-ttu-id="de319-106">master</span><span class="sxs-lookup"><span data-stu-id="de319-106">master</span></span>

<span data-ttu-id="de319-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de319-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de319-p101">Si se establece la propiedad [ActiveConnection](activeconnection-property-adox.md) en **Nothing**, se debiera "cerrar" el catálogo. Las colecciones asociadas estarán vacías. Todo objeto que se hubiese creado a partir de objetos de esquema en el catálogo quedará huérfano. Las propiedades para esos objetos que estén en caché seguirán estando disponibles, pero se producirá un error al leer propiedades que requieran una llamada al proveedor.</span><span class="sxs-lookup"><span data-stu-id="de319-p101">Setting the [ActiveConnection](activeconnection-property-adox.md) property to **Nothing** should "close" the catalog. Associated collections will be empty. Any objects that were created from schema objects in the catalog will be orphaned. Any properties on those objects that have been cached will still be available, but attempting to read properties that require a call to the provider will fail.</span></span>

```vb 
 
    ' BeginCloseConnectionVB 
    Sub Main() 
    On Error GoTo CloseConnectionByNothingError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    Dim tbl As ADOX.Table 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Set tbl = cat.Tables(0) 
    Debug.Print tbl.Type ' Cache tbl.Type info 
    Set cat.ActiveConnection = Nothing 
    Debug.Print tbl.Type ' tbl is orphaned 
    ' Previous line will succeed if this was cached 
    Debug.Print tbl.Columns(0).DefinedSize 
    ' Previous line will fail if this info has not been cached 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    CloseConnectionByNothingError: 
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndCloseConnectionVB 
```

<br/>

<span data-ttu-id="de319-112">Cerrar un objeto [Connection](connection-object-ado.md) que se haya utilizado para "abrir" el catálogo debiera tener el mismo efecto que establecer la propiedad **ActiveConnection** en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="de319-112">Closing a [Connection](connection-object-ado.md) object that was used to "open" the catalog should have the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

```vb
    Sub CloseConnection() 
     On Error GoTo CloseConnectionError 
     
     Dim cnn As New ADODB.Connection 
     Dim cat As New ADOX.Catalog 
     Dim tbl As ADOX.Table 
     
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Set cat.ActiveConnection = cnn 
     Set tbl = cat.Tables(0) 
     Debug.Print tbl.Type ' Cache tbl.Type info 
     cnn.Close 
     Debug.Print tbl.Type ' tbl is orphaned 
     ' Previous line will succeed if this was cached 
     Debug.Print tbl.Columns(0).DefinedSize 
     ' Previous line will fail if this info has not been cached 
     
     'Clean up 
     Set cat = Nothing 
     Set cnn = Nothing 
     Exit Sub 
     
    CloseConnectionError: 
     
     Set cat = Nothing 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndCloseConnection2VB
```
