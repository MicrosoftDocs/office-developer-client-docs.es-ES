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
ms.openlocfilehash: 1328dbbfe37ac1876d2839e08295a98068f52384
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889976"
---
# <a name="querydefprepare-property-dao"></a>QueryDef.Prepare Property (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Preparar

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

Puede utilizar la propiedad **Prepare** para crear y tener en el servidor un procedimiento de almacenado temporal desde su consulta y después ejecutarla, o simplemente ejecutar la consulta directamente. De forma predeterminada la propiedad **Prepare** está establecida en **dbQPrepare**. Sin embargo, puede establecer esta propiedad en **dbQUnprepare** para prohibir la preparación de la consulta. En este caso, la consulta se ejecuta utilizando la función API de **SQLExecDirect**.

Cuando se crea un procedimiento de almacenado se puede ralentizar la operación inicial, pero se aumenta el rendimiento de todas las referencias subsiguientes a la consulta. Sin embargo, algunas consultas no se pueden ejecutar en el formulario de procedimientos de almacenado. En estos casos, debe establecer la propiedad **Prepare** en **dbQUnprepare**.

Si **Prepare** está establecida en **dbQPrepare**, esto puede reemplazar cuando la consulta se ejecuta estableciendo el argumento options del método **[Execute](querydef-execute-method-dao.md)** en **dbExecDirect**.


> [!NOTE]
> <P>[!NOTA] La API de ODBC de <STRONG>SQLPrepare</STRONG> se llama tan pronto como se establece la propiedad <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> con DAO. Por tanto, si desea mejorar el rendimiento utilizando la opción <STRONG>dbQUnprepare</STRONG>, debe establecer la propiedad <STRONG>Prepare</STRONG> antes que la propiedad <STRONG>SQL</STRONG>.</P>



## <a name="example"></a>Ejemplo

En este ejemplo se utiliza la propiedad **Prepare** para especificar que una consulta se debería ejecutar directamente en vez de crear previamente un procedimiento de almacenado temporal en el servidor.

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

