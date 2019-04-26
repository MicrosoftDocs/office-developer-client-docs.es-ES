---
title: Método QueryDef.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 7ef7f61ef632617b8d64a3fd9c34e5887e50065c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302964"
---
# <a name="querydefexecute-method-dao"></a>Método QueryDef.Execute (DAO)

**Se aplica a:** Access 2013, Office 2013

Ejecuta una instrucción SQL en el objeto especificado.

## <a name="syntax"></a>Sintaxis

*expression* .Execute(***Options***)

*expression* Variable que representa un objeto **QueryDef**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Opciones</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar las siguientes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para Options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Deniega el permiso de escritura a otros usuarios (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Valor predeterminado) Ejecuta actualizaciones no coherentes (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Ejecuta actualizaciones coherentes (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Ejecuta una consulta de paso a través de SQL. Establecer esta opción pasa la instrucción SQL a una base de datos ODBC para procesamiento (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Deshace las actualizaciones si se produce un error (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Genera un error en tiempo de ejecución si otro usuario cambia los datos que está usted editando (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Ejecuta la consulta de forma asincrónica (sólo conexiones ODBCDirect y objetos QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Ejecuta la instrucción sin llamar primero a la función API de ODBC SQLPrepare (sólo conexiones ODBCDirect y objetos QueryDef).</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.

> [!NOTE]
> Las constantes **dbConsistent** y **dbInconsistent** son mutuamente excluyentes. Puede usar una o la otra, pero no ambas, en una instancia específica de **OpenRecordset**. Si se usan **dbConsistent** y **dbInconsistent**, se produce un error.

Use la propiedad **[RecordsAffected](querydef-recordsaffected-property-dao.md)** del objeto **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)** o **[QueryDef](querydef-object-dao.md)** para determinar el número de registros afectados por el método **[Execute](querydef-execute-method-dao.md)** más reciente. Por ejemplo, **RecordsAffected** contiene el número de registros eliminados, actualizados o insertados cuando se ejecuta una consulta de acciones. Cuando usa el método **Execute** para ejecutar una consulta, la propiedad **RecordsAffected** del objeto **QueryDef** se configura en el número de registros afectados.

En un área de trabajo de Microsoft Access, si proporciona una instrucción SQL sintácticamente correcta y tiene los permisos adecuados, el método **Execute** no provocará errores, incluso si no se puede modificar ni eliminar una sola línea. Por lo tanto, use siempre la opción **dbFailOnError** al uasr el método **Execute** para ejecutar o eliminar una consulta. Esta opción genera un error en tiempo de ejecución y deshace todos los cambios correctos si los objetos afectados están bloqueados y no se pueden actualizar ni eliminar.

En versiones anteriores del motor de base de datos de Microsoft Jet, las instrucciones SQL se insertaban automáticamente en transacciones implícitas. Si parte de una instrucción ejecutada con **dbFailOnError** producía un error, se revertía toda la instrucción. Para mejorar el rendimiento, desde la versión 3.5 estas instrucciones implícitas ya no existen. Si actualiza código DAO antiguo, no olvide que debe usar transacciones explícitas con las instrucciones **Execute**.

Para mejorar el rendimiento de un área de trabajo de Microsoft Access, especialmente en un entorno multiusuario, anide el método **Execute** dentro de una transacción. Use el método **[BeginTrans](workspace-begintrans-method-dao.md)** en el objeto **[Workspace](workspace-object-dao.md)** actual, use el método **Execute** y complete la transacción con el método **[CommitTrans](workspace-committrans-method-dao.md)** en el objeto **Workspace**. Esto guarda los cambios en el disco y libera cualquier bloqueo existente mientras se ejecuta la consulta.

## <a name="example"></a>Ejemplo

Este ejemplo muestra el método **Execute** cuando se ejecuta desde un objeto **QueryDef** y un objeto **Database**. Se necesitan los procedimientos ExecuteQueryDef y PrintOutput para que se pueda ejecutar este procedimiento.

```vb
    Sub ExecuteX() 
     
       Dim dbsNorthwind As Database 
       Dim strSQLChange As String 
       Dim strSQLRestore As String 
       Dim qdfChange As QueryDef 
       Dim rstEmployees As Recordset 
       Dim errLoop As Error 
     
       ' Define two SQL statements for action queries. 
       strSQLChange = "UPDATE Employees SET Country = " & _ 
          "'United States' WHERE Country = 'USA'" 
       strSQLRestore = "UPDATE Employees SET Country = " & _ 
          "'USA' WHERE Country = 'United States'" 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Create temporary QueryDef object. 
       Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
          strSQLChange) 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "SELECT LastName, Country FROM Employees", _ 
          dbOpenForwardOnly) 
     
       ' Print report of original data. 
       Debug.Print _ 
          "Data in Employees table before executing the query" 
       PrintOutput rstEmployees 
        
       ' Run temporary QueryDef. 
       ExecuteQueryDef qdfChange, rstEmployees 
        
       ' Print report of new data. 
       Debug.Print _ 
          "Data in Employees table after executing the query" 
       PrintOutput rstEmployees 
     
       ' Run action query to restore data. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       dbsNorthwind.Execute strSQLRestore, dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstEmployees.Requery 
     
       ' Print report of restored data. 
       Debug.Print "Data after executing the query " & _ 
          "to restore the original information" 
       PrintOutput rstEmployees 
     
       rstEmployees.Close 
        
       Exit Sub 
        
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
       rstTemp As Recordset) 
     
       Dim errLoop As Error 
        
       ' Run the specified QueryDef object. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       qdfTemp.Execute dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstTemp.Requery 
        
       Exit Sub 
     
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
       ' Enumerate Recordset. 
       Do While Not rstTemp.EOF 
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

El siguiente ejemplo muestra cómo ejecutar una consulta de parámetros. La colección Parameters se usa para establecer el parámetro Organization de la consulta myActionQuery antes de que esta se ejecute.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
