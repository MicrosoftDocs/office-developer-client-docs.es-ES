---
<span data-ttu-id="3135a-101"><<<<<<< Título HEAD: ejemplo de propiedad Count (VB) TOCTitle: ejemplo de propiedad Count (VB) === título: ejemplo de la propiedad Count (VB) TOCTitle: ejemplo de la propiedad Count (VB)</span><span class="sxs-lookup"><span data-stu-id="3135a-101"><<<<<<< HEAD title: Count Property Example (VB) TOCTitle: Count Property Example (VB) ======= title: Count property example (VB) TOCTitle: Count property example (VB)</span></span>
>>>>>>> <span data-ttu-id="3135a-102">Master ms:assetid: 9fea66f7-a4ed-fe2e-c199-672b910fef47 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249734(v=office.15) ms:contentKeyID: ms.date 48546695: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="3135a-102">master ms:assetid: 9fea66f7-a4ed-fe2e-c199-672b910fef47 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249734(v=office.15) ms:contentKeyID: 48546695 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3135a-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3135a-103"><<<<<<< HEAD</span></span>
# <a name="count-property-example-vb"></a><span data-ttu-id="3135a-104">Ejemplo de la propiedad Count (VB)</span><span class="sxs-lookup"><span data-stu-id="3135a-104">Count Property Example (VB)</span></span>
=======
# <a name="count-property-example-vb"></a><span data-ttu-id="3135a-105">Ejemplo de la propiedad Count (VB)</span><span class="sxs-lookup"><span data-stu-id="3135a-105">Count property example (VB)</span></span>
>>>>>>> <span data-ttu-id="3135a-106">master</span><span class="sxs-lookup"><span data-stu-id="3135a-106">master</span></span>


<span data-ttu-id="3135a-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3135a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3135a-108">En este ejemplo se muestra la propiedad [Count](count-property-ado.md) con dos colecciones en la base de datos de ***los empleados*** .</span><span class="sxs-lookup"><span data-stu-id="3135a-108">This example demonstrates the [Count](count-property-ado.md) property with two collections in the ***Employee*** database.</span></span> <span data-ttu-id="3135a-109">La propiedad obtiene el número de objetos de cada colección y establece el límite superior de los bucles que enumeran estas colecciones.</span><span class="sxs-lookup"><span data-stu-id="3135a-109">The property obtains the number of objects in each collection, and sets the upper limit for loops that enumerate these collections.</span></span> <span data-ttu-id="3135a-110">Otra forma de enumerar estas colecciones sin utilizar la propiedad **Count** sería utilizar instrucciones.</span><span class="sxs-lookup"><span data-stu-id="3135a-110">Another way to enumerate these collections without using the **Count** property would be to use statements.</span></span>

```vb 
 
'BeginCountVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLEmployees As String 
 Dim strCnxn As String 
 
 Dim intLoop As Integer 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employee table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "Employees" 
 'rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 rstEmployees.Open strSQLEmployees, Cnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines opening the recordset are identical as 
 'the default values for CursorType and LockType arguments match those specified 
 
 ' Print information about Fields collection 
 Debug.Print rstEmployees.Fields.Count & " Fields in Employee" 
 
 For intLoop = 0 To rstEmployees.Fields.Count - 1 
 Debug.Print " " & rstEmployees.Fields(intLoop).Name 
 Next intLoop 
 
 ' Print information about Properties collection 
 Debug.Print rstEmployees.Properties.Count & " Properties in Employee" 
 
 For intLoop = 0 To rstEmployees.Properties.Count - 1 
 Debug.Print " " & rstEmployees.Properties(intLoop).Name 
 Next intLoop 
 
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
'EndCountVB 
```

