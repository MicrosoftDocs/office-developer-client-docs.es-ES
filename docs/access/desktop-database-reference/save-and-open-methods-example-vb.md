---
title: Ejemplo de los métodos Save y Open (VB)
TOCTitle: Save and Open methods example (VB)
ms:assetid: aecb56b4-3ccd-d8f1-84a9-fd5a40aeca5f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249828(v=office.15)
ms:contentKeyID: 48547081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e4eff3eae32cf4d910a44eca5a733ac044a7829
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716939"
---
# <a name="save-and-open-methods-example-vb"></a><span data-ttu-id="9ea0d-102">Ejemplo de los métodos Save y Open (VB)</span><span class="sxs-lookup"><span data-stu-id="9ea0d-102">Save and Open methods example (VB)</span></span>


<span data-ttu-id="9ea0d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ea0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ea0d-104">En estos tres ejemplos se muestra cómo se pueden utilizar conjuntamente los métodos [Save](save-method-ado.md) y [Open](open-method-ado-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="9ea0d-104">These three examples demonstrate how the [Save](save-method-ado.md) and [Open](open-method-ado-recordset.md) methods can be used together.</span></span>

<span data-ttu-id="9ea0d-p101">Supongamos que se va de viaje de negocios y que desea llevarse una tabla de una base de datos. Antes de marcharse, obtiene acceso a los datos como un [conjunto de registros](recordset-object-ado.md) y lo guarda en un formato transportable. Cuando llega a su destino, obtiene acceso al **conjunto de registros** como un **conjunto de registros** local desconectado. Realiza cambios en el **conjunto de registros** y, a continuación, lo vuelve a guardar. Finalmente, al volver a casa, se conecta de nuevo a la base de datos y la actualiza con los cambios realizados mientras estaba de viaje.</span><span class="sxs-lookup"><span data-stu-id="9ea0d-p101">Assume you are going on a business trip and want to take along a table from a database. Before you go, you access the data as a [Recordset](recordset-object-ado.md) and save it in a transportable form. When you arrive at your destination, you access the **Recordset** as a local, disconnected **Recordset**. You make changes to the **Recordset**, then save it again. Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</span></span>

<span data-ttu-id="9ea0d-110">Primero, obtenga acceso y guarde la tabla ***Authors***.</span><span class="sxs-lookup"><span data-stu-id="9ea0d-110">First, access and save the ***Authors*** table.</span></span>

```vb 
 
'BeginSaveVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstAuthors As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 Set rstAuthors = New ADODB.Recordset 
 strSQLAuthors = "SELECT au_id, au_lname, au_fname, city, phone FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenDynamic, adLockOptimistic, adCmdText 
 
 'For sake of illustration, save the Recordset to a diskette in XML format 
 rstAuthors.Save "c:\Pubs.xml", adPersistXML 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 'clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSaveVB 
```

<br/>

<span data-ttu-id="9ea0d-111">En este punto, ha llegado a su destino.</span><span class="sxs-lookup"><span data-stu-id="9ea0d-111">At this point, you have arrived at your destination.</span></span> <span data-ttu-id="9ea0d-112">Va a tener acceso a la tabla ***Authors*** como un **conjunto de registros**de local y desconectado.</span><span class="sxs-lookup"><span data-stu-id="9ea0d-112">You will access the ***Authors*** table as a local, disconnected **Recordset**.</span></span> <span data-ttu-id="9ea0d-113">No olvide que debe tener el proveedor **MSPersist** en el equipo que va a usar con el fin de obtener acceso al archivo guardado, r:\\Pubs.xml.</span><span class="sxs-lookup"><span data-stu-id="9ea0d-113">Don't forget you must have the **MSPersist** provider on the machine that you are using in order to access the saved file, a:\\Pubs.xml.</span></span>

```vb 
 
'BeginSave2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rst As ADODB.Recordset 
 Set rst = New ADODB.Recordset 
 
 'For sake of illustration, we specify all parameters 
 rst.Open "c:\Pubs.xml", "Provider=MSPersist;", adOpenForwardOnly, adLockBatchOptimistic, adCmdFile 
 
 'Now you have a local, disconnected Recordset - Edit as you desired 
 '(In this example the change makes no difference) 
 rst.Find "au_lname = 'Carson'" 
 If rst.EOF Then 
 Debug.Print "Name not found." 
 Exit Sub 
 End If 
 
 rst!city = "Chicago" 
 rst.Update 
 
 'Save changes in ADTG format this time, purely for sake of illustration. 
 'Note that the previous version is still on the diskette, as a:\Pubs.xml. 
 rst.Save "c:\Pubs.adtg", adPersistADTG 
 
 ' clean up 
 rst.Close 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 'clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSave2VB 
```

<br/>

<span data-ttu-id="9ea0d-p103">Por último, vuelve a casa. Ahora, actualice la base de datos con los cambios realizados.</span><span class="sxs-lookup"><span data-stu-id="9ea0d-p103">Finally, you return home. Now update the database with your changes.</span></span>

```vb 
 
'BeginSave3VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As New ADODB.Connection 
 Dim rst As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set rst = New ADODB.Recordset 
 ' The lock mode is batch optimistic because we are going to 
 ' use the UpdateBatch method. 
 rst.Open "c:\Pubs.adtg", "Provider=MSPersist;", adOpenForwardOnly, adLockBatchOptimistic, adCmdFile 
 
 ' Connect to the database, associate the Recordset with the connection 
 ' then update the database table with the changed Recordset 
 strCnxn = "Provider=SQLOLEDB;Data Source=MySqlServer;Integrated Security=SSPI;Initial Catalog=pubs;" 
 Cnxn.Open strCnxn 
 
 rst.ActiveConnection = Cnxn 
 rst.UpdateBatch 
 
 ' clean up 
 rst.Close 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 'clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSave3VB 
```

