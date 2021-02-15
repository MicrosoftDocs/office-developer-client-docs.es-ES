---
title: Propiedad Database.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f47d6c51079bf36cb7e1ca596a3476f1a7219c5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294742"
---
# <a name="databasequerytimeout-property-dao"></a>Propiedad Database.QueryTimeout (DAO)


**Se aplica a:** Access 2013, Office 2013


Establece o devuelve un valor que especifica el número de segundos que se deben esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta una consulta en un origen de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . QueryTimeout

*expression* Variable que representa un objeto **Database**.

## <a name="remarks"></a>Comentarios

El valor predeterminado es 60.

Cuando se utiliza una base de datos ODBC, como Microsoft SQL Server, pueden producirse retrasos debido al tráfico de la red o al uso intensivo del servidor ODBC. En lugar de esperar indefinidamente, se puede especificar cuánto tiempo se desea esperar.

Cuando se utiliza **QueryTimeout** con un objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)**, especifica un valor global para todas las consultas asociadas con la base de datos. Puede invalidar este valor para una consulta específica estableciendo la propiedad **ODBCTimeout** del objeto **[QueryDef](querydef-object-dao.md)** en particular.

## <a name="example"></a>Ejemplo

En este ejemplo se utilizan las propiedades **ODBCTimeout** y **QueryTimeout** para mostrar cómo el valor **QueryTimeout** en un objeto **Database** establece el valor **ODBCTimeout** predeterminado en cualquier objeto **QueryDef** creado desde un objeto **Database**.

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

