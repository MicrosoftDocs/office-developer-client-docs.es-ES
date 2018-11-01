---
title: Método Database.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e72de1f266b1dc24267b1c7f3c43be489d92fb5e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889598"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="02c12-102">Método Database.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="02c12-102">Database.Execute Method (DAO)</span></span>

<span data-ttu-id="02c12-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02c12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02c12-104">Ejecuta una consulta de acción o una instrucción SQL en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="02c12-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c12-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02c12-105">Syntax</span></span>

<span data-ttu-id="02c12-106">*expresión* . Ejecutar (***consulta***, ***Opciones***)</span><span class="sxs-lookup"><span data-stu-id="02c12-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="02c12-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="02c12-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="02c12-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02c12-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02c12-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="02c12-109">Name</span></span></p></th>
<th><p><span data-ttu-id="02c12-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="02c12-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="02c12-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="02c12-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="02c12-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="02c12-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c12-113">Query</span><span class="sxs-lookup"><span data-stu-id="02c12-113">Query</span></span></p></td>
<td><p><span data-ttu-id="02c12-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="02c12-114">Required</span></span></p></td>
<td><p><span data-ttu-id="02c12-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c12-116">Options</span><span class="sxs-lookup"><span data-stu-id="02c12-116">Options</span></span></p></td>
<td><p><span data-ttu-id="02c12-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="02c12-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="02c12-118"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="02c12-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02c12-119">Remarks</span></span>

<span data-ttu-id="02c12-120">Puede usar las siguientes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para ver las opciones.</span><span class="sxs-lookup"><span data-stu-id="02c12-120">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02c12-121">Constante</span><span class="sxs-lookup"><span data-stu-id="02c12-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="02c12-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="02c12-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c12-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-124">Deniega el permiso de escritura a otros usuarios (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02c12-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c12-125"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-126">(Valor predeterminado) Ejecuta actualizaciones no coherentes (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02c12-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c12-127"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-128">Ejecuta actualizaciones coherentes (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02c12-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c12-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-p101">Ejecuta una consulta de paso a través de SQL. Establecer esta opción pasa la instrucción SQL a una base de datos ODBC para procesamiento (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02c12-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c12-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-133">Deshace las actualizaciones si se produce un error (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02c12-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c12-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-135">Genera un error en tiempo de ejecución si otro usuario cambia los datos que está usted editando (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02c12-135">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c12-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-137">Ejecuta la consulta de forma asincrónica (sólo conexiones ODBCDirect y objetos QueryDef).</span><span class="sxs-lookup"><span data-stu-id="02c12-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c12-138"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="02c12-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="02c12-139">Ejecuta la instrucción sin llamar primero a la función API de ODBC SQLPrepare (sólo conexiones ODBCDirect y objetos QueryDef).</span><span class="sxs-lookup"><span data-stu-id="02c12-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="02c12-p102">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="02c12-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="02c12-p103">[!NOTA] Las constantes **dbConsistent** y **dbInconsistent** son mutuamente excluyentes. Puede usar una o la otra, pero no ambas, en una instancia específica de **OpenRecordset**. Si se usan **dbConsistent** y **dbInconsistent**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="02c12-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="02c12-p104">El método **Execute** solo es válido para consultas de acción. Si utiliza **Execute** con otro tipo de consulta, se produce un error. Como una consulta de acción no devuelve registros, **Execute** no devuelve un objeto **Recordset**. (La ejecución de una consulta de paso SQL en un área de trabajo de ODBCDirect no devuelve un error si no se devuelve un objeto **Recordset**.)</span><span class="sxs-lookup"><span data-stu-id="02c12-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="02c12-p105">Utilice la propiedad **RecordsAffected** del objeto **Connection**, **Database** o **QueryDef** para determinar el número de registros afectados por el método **Execute** más reciente. Por ejemplo, **RecordsAffected** contiene el número de registros eliminados, actualizados o insertados al ejecutar una consulta de acción. Cuando se utiliza el método **Execute** para ejecutar una consulta, la propiedad **RecordsAffected** del objeto **QueryDef** se establece en el número de registros afectados.</span><span class="sxs-lookup"><span data-stu-id="02c12-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="02c12-p106">En un área de trabajo de Microsoft Access, si especifica una instrucción SQL sintácticamente correcta y dispone de los permisos correspondientes, el método **Execute** no producirá un error, aunque no pueda modificarse ni eliminarse una fila. Por tanto, utilice siempre la opción **dbFailOnError** cuando use el método **Execute** para ejecutar una actualización o eliminar una consulta. Esta opción genera un error en tiempo de ejecución y deshace todos los cambios que se han realizado correctamente si alguno de los registros afectados está bloqueado y no se puede actualizar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="02c12-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="02c12-p107">En versiones anteriores del motor de base de datos de Microsoft Jet, las instrucciones SQL se insertaban automáticamente en transacciones implícitas. Si parte de una instrucción ejecutada con **dbFailOnError** producía un error, se revertía toda la instrucción. Para mejorar el rendimiento, desde la versión 3.5 estas instrucciones implícitas ya no existen. Si actualiza código DAO antiguo, no olvide que debe usar transacciones explícitas con las instrucciones **Execute**.</span><span class="sxs-lookup"><span data-stu-id="02c12-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="02c12-p108">Para mejorar el rendimiento en un área de trabajo de Microsoft Access, especialmente en un entorno multiusuario, anide el método **Execute** dentro de una transacción. Use el método **BeginTrans** en el objeto **Workspace** actual, use el método **Execute** y complete la transacción con el método **CommitTrans** en el objeto **Workspace**. Esto guarda los cambios en el disco y libera todos los bloqueos aplicados mientras se ejecutaba la consulta.</span><span class="sxs-lookup"><span data-stu-id="02c12-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="02c12-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02c12-162">Example</span></span>

<span data-ttu-id="02c12-p109">Este ejemplo muestra el método **Execute** cuando se ejecuta desde un objeto **QueryDef** y un objeto **Database**. Se necesitan los procedimientos ExecuteQueryDef y PrintOutput para que se pueda ejecutar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="02c12-p109">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

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
     Debug.Print " " & rstTemp!LastName & _ 
     ", " & rstTemp!Country 
     rstTemp.MoveNext 
     Loop 
     
    End Sub
```
