---
<span data-ttu-id="eb429-101"><<<<<<< Título HEAD: colección Parameters, TOCTitle de ejemplo de propiedad comando (VB): colección Parameters, ejemplo de propiedad comando (VB) === título: colección de parámetros, ejemplo de la propiedad comando (VB) TOCTitle: parámetros Colección de ejemplo de la propiedad comando (VB)</span><span class="sxs-lookup"><span data-stu-id="eb429-101"><<<<<<< HEAD title: Parameters Collection, Command Property Example (VB) TOCTitle: Parameters Collection, Command Property Example (VB) ======= title: Parameters Collection, Command property example (VB) TOCTitle: Parameters Collection, Command property example (VB)</span></span>
>>>>>>> <span data-ttu-id="eb429-102">Master ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15) ms:contentKeyID: ms.date 48544290: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="eb429-102">master ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15) ms:contentKeyID: 48544290 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="eb429-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="eb429-103"><<<<<<< HEAD</span></span>
# <a name="parameters-collection-command-property-example-vb"></a><span data-ttu-id="eb429-104">Ejemplo de colección Parameters, propiedad Comando (VB)</span><span class="sxs-lookup"><span data-stu-id="eb429-104">Parameters Collection, Command Property Example (VB)</span></span>
=======
# <a name="parameters-collection-command-property-example-vb"></a><span data-ttu-id="eb429-105">Colección de parámetros, ejemplo de la propiedad comando (VB)</span><span class="sxs-lookup"><span data-stu-id="eb429-105">Parameters Collection, Command property example (VB)</span></span>
>>>>>>> <span data-ttu-id="eb429-106">master</span><span class="sxs-lookup"><span data-stu-id="eb429-106">master</span></span>


<span data-ttu-id="eb429-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb429-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb429-108">El código siguiente muestra cómo utilizar la propiedad [Comando](command-property-adox.md) con el objeto [Command](command-object-ado.md) para recuperar información de parámetros para el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="eb429-108">The following code demonstrates how to use the [Command](command-property-adox.md) property with the [Command](command-object-ado.md) object to retrieve parameter information for the procedure.</span></span>

```vb 
 
' BeginParametersVB 
Sub Main() 
 On Error GoTo ProcedureParametersError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command object 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Retrieve Parameter information 
 cmd.Parameters.Refresh 
 For Each prm In cmd.Parameters 
 Debug.Print prm.Name & ":" & prm.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureParametersError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndParametersVB 
```

