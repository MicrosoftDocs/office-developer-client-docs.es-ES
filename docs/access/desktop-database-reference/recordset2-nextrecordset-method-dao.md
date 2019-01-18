---
title: Recordset2.NextRecordset (método) (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 33288131-d4f3-0159-1736-f401346087f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192318(v=office.15)
ms:contentKeyID: 48544096
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053575
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54d0e49dfbe9dc3fb87eb10af9eefe3aa2f83709
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715931"
---
# <a name="recordset2nextrecordset-method-dao"></a><span data-ttu-id="7c7fe-102">Recordset2.NextRecordset (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c7fe-102">Recordset2.NextRecordset method (DAO)</span></span>


<span data-ttu-id="7c7fe-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c7fe-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7fe-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c7fe-104">Syntax</span></span>

<span data-ttu-id="7c7fe-105">*expresión* . NextRecordset</span><span class="sxs-lookup"><span data-stu-id="7c7fe-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="7c7fe-106">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7c7fe-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c7fe-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c7fe-107">Return value</span></span>

<span data-ttu-id="7c7fe-108">Booleano</span><span class="sxs-lookup"><span data-stu-id="7c7fe-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="7c7fe-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c7fe-109">Remarks</span></span>

<span data-ttu-id="7c7fe-110">En un área de trabajo de ODBCDirect, puede abrir un **objeto Recordset** que contiene más de una consulta de selección en el argumento source de **OpenRecordset**o la propiedad **[SQL](querydef-sql-property-dao.md)** de una objeto **[QueryDef](querydef-object-dao.md)** , como se muestra en el siguiente ejemplo de consulta de selección.</span><span class="sxs-lookup"><span data-stu-id="7c7fe-110">In an ODBCDirect workspace, you can open a **Recordset** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="7c7fe-p101">El objeto **Recordset** devuelto se abrirá con los resultados de la primera consulta. Para obtener los conjuntos de registros resultantes de las siguientes consultas, use el método **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="7c7fe-p101">The returned **Recordset** will open with the results of the first query. To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="7c7fe-p102">Si hay disponibles más registros (es decir, había otra consulta de selección en la llamada **OpenRecordset** o en la propiedad **SQL**), los registros devueltos de la siguiente consulta se cargarán en **Recordset** y **NextRecordset** devolverá **True**, lo que indica que los registros están disponibles. Cuando no hay más registros disponibles (es decir, los resultados de la última consulta de selección se cargaron en el objeto **Recordset**), **NextRecordset** devolverá **False**, y **Recordset** estará vacío.</span><span class="sxs-lookup"><span data-stu-id="7c7fe-p102">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available. When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="7c7fe-p103">También puede usar el método **[Cancel](connection-cancel-method-dao.md)** para limpiar el contenido de un objeto **Recordset**. No obstante, **Cancel** limpia igualmente cualquier registro adicional no cargado todavía.</span><span class="sxs-lookup"><span data-stu-id="7c7fe-p103">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**. However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="7c7fe-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c7fe-117">Example</span></span>

<span data-ttu-id="7c7fe-p104">En este ejemplo, se usa el método **NextRecordset** para ver los datos de una consulta SELECT compuesta. La propiedad **DefaultCursorDriver** debe estar establecida en **dbUseODBCCursor** al ejecutar dichas consultas. El método **NextRecordset** devolverá **True** incluso si todas o algunas de las instrucciones SELECT devuelven cero registros; solo devolverá **False** después de que se hayan comprobado todas las cláusulas SQL individuales.</span><span class="sxs-lookup"><span data-stu-id="7c7fe-p104">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset2 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="7c7fe-p105">Esta misma tarea se puede realizar también creando una instrucción preparada que contenga la instrucción SQL compuesta. La propiedad **CacheSize** del objeto **QueryDef** debe estar establecida en 1 y el objeto **Recordset** debe ser de sólo avance y de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7c7fe-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset2 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

