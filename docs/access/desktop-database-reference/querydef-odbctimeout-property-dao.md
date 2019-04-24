---
title: Propiedad QueryDef. ODBCTimeout (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d34aee30e649b1c25ddc6af8078da2af9dd3b84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301004"
---
# <a name="querydefodbctimeout-property-dao"></a>Propiedad QueryDef. ODBCTimeout (DAO)


**Se aplica a:** Access 2013, Office 2013

Indica el número de segundos que hay que esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta **[QueryDef](querydef-object-dao.md)** en una base de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . ODBCTimeout

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Comentarios

Cuando la propiedad **ODBCTimeout** está establecida en -1, el tiempo de espera establece el valor actual de la propiedad **[QueryTimeout](database-querytimeout-property-dao.md)** del objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)** que contiene **QueryDef**. Cuando la propiedad **ODBCTimeout** está establecida en 0, no se produce un error de tiempo de espera.

Cuando esté utilizando una base de datos ODBC como, por ejemplo Microsoft SQL Server, pueden producirse demoras debido al tráfico en la red o a una sobrecarga en el servidor ODBC. En vez de esperar indefinidamente, puede especificar el tiempo de espera antes de que se devuelva un error.

Al establecer la propiedad **ODBCTimeout** de un objeto **QueryDef** se anula el valor especificado por la propiedad **QueryTimeout** del objeto **Connection** o **Database** que contiene **QueryDef**, pero únicamente para ese objeto **QueryDef**.

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

