---
title: QueryDef.Prepare Property (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cec1fde6bc76438da2292ae30545337eaeea6cf4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484792"
---
# <a name="querydefprepare-property-dao"></a><span data-ttu-id="f7b20-102">QueryDef.Prepare Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7b20-102">QueryDef.Prepare Property (DAO)</span></span>


<span data-ttu-id="f7b20-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7b20-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b20-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7b20-104">Syntax</span></span>

<span data-ttu-id="f7b20-105">*expresión* . Preparar</span><span class="sxs-lookup"><span data-stu-id="f7b20-105">*expression* .Prepare</span></span>

<span data-ttu-id="f7b20-106">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="f7b20-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b20-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7b20-107">Remarks</span></span>

<span data-ttu-id="f7b20-p101">Puede utilizar la propiedad **Prepare** para crear y tener en el servidor un procedimiento de almacenado temporal desde su consulta y después ejecutarla, o simplemente ejecutar la consulta directamente. De forma predeterminada la propiedad **Prepare** está establecida en **dbQPrepare**. Sin embargo, puede establecer esta propiedad en **dbQUnprepare** para prohibir la preparación de la consulta. En este caso, la consulta se ejecuta utilizando la función API de **SQLExecDirect**.</span><span class="sxs-lookup"><span data-stu-id="f7b20-p101">You can use the **Prepare** property to either have the server create a temporary stored procedure from your query and then execute it, or just have the query executed directly. By default the **Prepare** property is set to **dbQPrepare**. However, you can set this property to **dbQUnprepare** to prohibit preparing of the query. In this case, the query is executed using the **SQLExecDirect** API.</span></span>

<span data-ttu-id="f7b20-p102">Cuando se crea un procedimiento de almacenado se puede ralentizar la operación inicial, pero se aumenta el rendimiento de todas las referencias subsiguientes a la consulta. Sin embargo, algunas consultas no se pueden ejecutar en el formulario de procedimientos de almacenado. En estos casos, debe establecer la propiedad **Prepare** en **dbQUnprepare**.</span><span class="sxs-lookup"><span data-stu-id="f7b20-p102">Creating a stored procedure can slow down the initial operation, but increases performance of all subsequent references to the query. However, some queries cannot be executed in the form of stored procedures. In these cases, you must set the **Prepare** property to **dbQUnprepare**.</span></span>

<span data-ttu-id="f7b20-115">Si **Prepare** está establecida en **dbQPrepare**, esto puede reemplazar cuando la consulta se ejecuta estableciendo el argumento options del método **[Execute](querydef-execute-method-dao.md)** en **dbExecDirect**.</span><span class="sxs-lookup"><span data-stu-id="f7b20-115">If **Prepare** is set to **dbQPrepare**, this can be overridden when the query is executed by setting the **[Execute](querydef-execute-method-dao.md)** method's options argument to **dbExecDirect**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f7b20-p103">[!NOTA] La API de ODBC de <STRONG>SQLPrepare</STRONG> se llama tan pronto como se establece la propiedad <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> con DAO. Por tanto, si desea mejorar el rendimiento utilizando la opción <STRONG>dbQUnprepare</STRONG>, debe establecer la propiedad <STRONG>Prepare</STRONG> antes que la propiedad <STRONG>SQL</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f7b20-p103">The ODBC <STRONG>SQLPrepare</STRONG> API is called as soon as the DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> property is set. Therefore, if you want to improve performance using the <STRONG>dbQUnprepare</STRONG> option, you must set the <STRONG>Prepare</STRONG> property before setting the <STRONG>SQL</STRONG> property.</span></span></P>



## <a name="example"></a><span data-ttu-id="f7b20-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7b20-118">Example</span></span>

<span data-ttu-id="f7b20-119">En este ejemplo se utiliza la propiedad **Prepare** para especificar que una consulta se debería ejecutar directamente en vez de crear previamente un procedimiento de almacenado temporal en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f7b20-119">This example uses the **Prepare** property to specify that a query should be executed directly rather than first creating a temporary stored procedure on the server.</span></span>

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```

