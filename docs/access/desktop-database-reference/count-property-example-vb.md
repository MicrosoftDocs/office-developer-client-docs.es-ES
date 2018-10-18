---
<<<<<<< Título HEAD: ejemplo de propiedad Count (VB) TOCTitle: ejemplo de propiedad Count (VB) === título: ejemplo de la propiedad Count (VB) TOCTitle: ejemplo de la propiedad Count (VB)
>>>>>>> Master ms:assetid: 9fea66f7-a4ed-fe2e-c199-672b910fef47 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249734(v=office.15) ms:contentKeyID: ms.date 48546695: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="count-property-example-vb"></a>Ejemplo de la propiedad Count (VB)
=======
# <a name="count-property-example-vb"></a>Ejemplo de la propiedad Count (VB)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

En este ejemplo se muestra la propiedad [Count](count-property-ado.md) con dos colecciones en la base de datos de ***los empleados*** . La propiedad obtiene el número de objetos de cada colección y establece el límite superior de los bucles que enumeran estas colecciones. Otra forma de enumerar estas colecciones sin utilizar la propiedad **Count** sería utilizar instrucciones.

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

