---
<span data-ttu-id="c4819-101"><<<<<<< Título HEAD: filtro y ejemplo de propiedades RecordCount (VB) TOCTitle: filtro y ejemplo de propiedades RecordCount (VB) === título: ejemplo de las propiedades Filter y RecordCount (VB) TOCTitle: propiedades Filter y RecordCount ejemplo (VB)</span><span class="sxs-lookup"><span data-stu-id="c4819-101"><<<<<<< HEAD title: Filter and RecordCount Properties Example (VB) TOCTitle: Filter and RecordCount Properties Example (VB) ======= title: Filter and RecordCount properties example (VB) TOCTitle: Filter and RecordCount properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="c4819-102">Master ms:assetid: 3da4623e-03e7-27ac-7351-3b22415be0b9 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249167(v=office.15) ms:contentKeyID: ms.date 48544354: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="c4819-102">master ms:assetid: 3da4623e-03e7-27ac-7351-3b22415be0b9 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249167(v=office.15) ms:contentKeyID: 48544354 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c4819-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="c4819-103"><<<<<<< HEAD</span></span>
# <a name="filter-and-recordcount-properties-example-vb"></a><span data-ttu-id="c4819-104">Ejemplo de las propiedades Filter y RecordCount (VB)</span><span class="sxs-lookup"><span data-stu-id="c4819-104">Filter and RecordCount Properties Example (VB)</span></span>
=======
# <a name="filter-and-recordcount-properties-example-vb"></a><span data-ttu-id="c4819-105">Ejemplo de las propiedades Filter y RecordCount (VB)</span><span class="sxs-lookup"><span data-stu-id="c4819-105">Filter and RecordCount properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="c4819-106">master</span><span class="sxs-lookup"><span data-stu-id="c4819-106">master</span></span>


<span data-ttu-id="c4819-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4819-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4819-108">Este ejemplo se abre un **objeto Recordset** en la tabla Publishers en la base de datos ***Pubs*** .</span><span class="sxs-lookup"><span data-stu-id="c4819-108">This example open a **Recordset** on the Publishers table in the ***Pubs*** database.</span></span> <span data-ttu-id="c4819-109">A continuación, se usa la propiedad [Filter](filter-property-ado.md) para limitar el número de registros visibles a aquellos editores de una región o país concreto.</span><span class="sxs-lookup"><span data-stu-id="c4819-109">It then uses the [Filter](filter-property-ado.md) property to limit the number of visible records to those publishers in a particular country/region.</span></span> <span data-ttu-id="c4819-110">La propiedad **RecordCount** se usa para mostrar la diferencia entre los conjuntos de registros filtrados y sin filtrar.</span><span class="sxs-lookup"><span data-stu-id="c4819-110">The **RecordCount** property is used to show the difference between the filtered and unfiltered recordsets.</span></span>

```vb 
 
'BeginFilterVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim SQLPublishers As String 
 
 ' criteria variables 
 Dim intPublisherCount As Integer 
 Dim strCountry As String 
 Dim strMessage As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with data from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 SQLPublishers = "publishers" 
 rstPublishers.Open SQLPublishers, strCnxn, adOpenStatic, , adCmdTable 
 
 intPublisherCount = rstPublishers.RecordCount 
 
 ' get user input 
 strCountry = Trim(InputBox("Enter a country to filter on (e.g. USA):")) 
 
 If strCountry <> "" Then 
 ' open a filtered Recordset object 
 rstPublishers.Filter = "Country ='" & strCountry & "'" 
 
 If rstPublishers.RecordCount = 0 Then 
 MsgBox "No publishers from that country." 
 Else 
 ' print number of records for the original recordset 
 ' and the filtered recordset 
 strMessage = "Orders in original recordset: " & _ 
 vbCr & intPublisherCount & vbCr & _ 
 "Orders in filtered recordset (Country = '" & _ 
 strCountry & "'): " & vbCr & _ 
 rstPublishers.RecordCount 
 MsgBox strMessage 
 End If 
 End If 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndFilterVB 
```


> [!NOTE]
> <P><span data-ttu-id="c4819-p102">[!NOTA] Cuando se saben los datos que se desean seleccionar, normalmente es más eficaz abrir un objeto <STRONG>Recordset</STRONG> con una instrucción SQL. En este ejemplo se muestra cómo se puede crear sólo un objeto <STRONG>Recordset</STRONG> y obtener registros de un país o región determinado.</span><span class="sxs-lookup"><span data-stu-id="c4819-p102">When you know the data you want to select, it's usually more efficient to open a <STRONG>Recordset</STRONG> with an SQL statement. This example shows how you can create just one <STRONG>Recordset</STRONG> and obtain records from a particular country/region.</span></span></P>



```vb 
 
'BeginFilter2VB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLPublishers As String 
 Dim strCnxn As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with criteria from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 strSQLPublishers = "SELECT * FROM publishers WHERE Country = 'USA'" 
 rstPublishers.Open strSQLPublishers, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' print recordset 
 rstPublishers.MoveFirst 
 Do While Not rstPublishers.EOF 
 Debug.Print rstPublishers!pub_name & ", " & rstPublishers!country 
 rstPublishers.MoveNext 
 Loop 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndFilter2VB 
```

