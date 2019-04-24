---
title: Propiedad Recordset. CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: 8632f5fb-6e5d-5a3e-1bd7-81e1270e9531
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196807(v=office.15)
ms:contentKeyID: 48546079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 369ff9192bb592c96e17920c9771c10b70dc233b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300598"
---
# <a name="recordsetcachesize-property-dao"></a>Propiedad Recordset. CacheSize (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. **Long** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . CacheSize

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

El valor de la propiedad **CacheSize** debe estar entre 5 y 1200, pero no debe ser mayor de lo que permite la memoria disponible. Un valor típico es 100. Un valor de 0 desactiva la caché.

El almacenamiento en la memoria caché de datos mejora el rendimiento si se usan objetos **Recordset** para recuperar datos de un servidor remoto. Una memoria caché es un espacio en la memoria local que contiene los datos recuperados más recientemente en el servidor; esto es útil si los usuarios solicitan los datos de nuevo mientras se ejecuta la aplicación. Cuando los usuarios solicitan datos, el motor de base de datos de Microsoft Access busca primero en la memoria caché los datos solicitados en lugar de recuperarlos del servidor, que requiere más tiempo. En la memoria caché solo se guardan los datos procedentes de un origen de datos ODBC.

Cualquier motor de base de datos de Microsoft Access conectado a un origen de datos ODBC como, por ejemplo, una tabla vinculada, puede tener una caché local. Para crear una memoria caché, abra un objeto **Recordset** de un origen de datos remoto, establezca las propiedades **CacheSize** y **[CacheStart](recordset-cachestart-property-dao.md)** y, a continuación, use el método **[FillCache](recordset-fillcache-method-dao.md)** o examine los registros usando los métodos **Move**.

Puede basar el valor de la propiedad **CacheSize** en el número de registros que su aplicación puede tratar a la vez. Por ejemplo, si está usando un objeto **Recordset** como el origen de los datos que aparecen en pantalla, puede establecer su propiedad **CacheSize** en 20 para mostrar 20 registros a la vez.

El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché desde la caché y solicita registros fuera del intervalo de caché desde el servidor.

Los registros recuperados de la caché no reflejan los cambios concurrentes realizados por otros usuarios en el origen de datos.

Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad **CacheSize** del objeto **Recordset** en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, finalmente, use el método **FillCache**.

## <a name="example"></a>Ejemplo

En este ejemplo se utilizan los métodos **CreateTableDef** y **FillCache**, y las propiedades **CacheSize**, **CacheStart** y **SourceTableName** para enumerar los registros de una tabla vinculada dos veces. A continuación, se enumeran los registros dos veces con una caché de 50 registros. En este ejemplo se muestran luego las estadísticas de rendimiento para las ejecuciones almacenadas y no almacenadas en caché a través de la tabla vinculada.

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
