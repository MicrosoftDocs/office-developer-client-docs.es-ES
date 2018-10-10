---
title: Recordset2.NextRecordset Method (DAO)
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
ms.openlocfilehash: 4c0206b13fb8a846f50b5a2358d60d6807bdec26
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483999"
---
# <a name="recordset2nextrecordset-method-dao"></a>Recordset2.NextRecordset Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . NextRecordset

*expresión* Variable que representa un objeto **Recordset2** .

### <a name="return-value"></a>Valor devuelto

Booleano

## <a name="remarks"></a>Comentarios

En un área de trabajo de ODBCDirect, puede abrir un **objeto Recordset** que contiene más de una consulta de selección en el argumento source de **OpenRecordset**o la propiedad **[SQL](querydef-sql-property-dao.md)** de una objeto **[QueryDef](querydef-object-dao.md)** , como se muestra en el siguiente ejemplo de consulta de selección.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

El objeto **Recordset** devuelto se abrirá con los resultados de la primera consulta. Para obtener los conjuntos de registros resultantes de las siguientes consultas, use el método **NextRecordset**.

Si hay disponibles más registros (es decir, había otra consulta de selección en la llamada **OpenRecordset** o en la propiedad **SQL**), los registros devueltos de la siguiente consulta se cargarán en **Recordset** y **NextRecordset** devolverá **True**, lo que indica que los registros están disponibles. Cuando no hay más registros disponibles (es decir, los resultados de la última consulta de selección se cargaron en el objeto **Recordset**), **NextRecordset** devolverá **False**, y **Recordset** estará vacío.

También puede usar el método **[Cancel](connection-cancel-method-dao.md)** para limpiar el contenido de un objeto **Recordset**. No obstante, **Cancel** limpia igualmente cualquier registro adicional no cargado todavía.

## <a name="example"></a>Ejemplo

En este ejemplo, se usa el método **NextRecordset** para ver los datos de una consulta SELECT compuesta. La propiedad **DefaultCursorDriver** debe estar establecida en **dbUseODBCCursor** al ejecutar dichas consultas. El método **NextRecordset** devolverá **True** incluso si todas o algunas de las instrucciones SELECT devuelven cero registros; solo devolverá **False** después de que se hayan comprobado todas las cláusulas SQL individuales.

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

Esta misma tarea se puede realizar también creando una instrucción preparada que contenga la instrucción SQL compuesta. La propiedad **CacheSize** del objeto **QueryDef** debe estar establecida en 1 y el objeto **Recordset** debe ser de sólo avance y de solo lectura.

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

