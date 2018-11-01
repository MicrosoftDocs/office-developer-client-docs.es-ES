---
title: Recordset2.FillCache Method (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6b3645346482e3abef474fc6801d5f2a9a988b50
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889892"
---
# <a name="recordset2fillcache-method-dao"></a>Recordset2.FillCache Method (DAO)


**Se aplica a**: Access 2013, Office 2013

Rellena parcial o totalmente una memoria caché local de un objeto **Recordset** que contiene datos de un origen de datos ODBC conectado al motor de base de datos de Microsoft Access (solo bases de datos ODBC conectadas al motor de base de datos de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . FillCache (***filas***, ***StartBookmark***)

*expresión* Variable que representa un objeto **Recordset2** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Filas</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica el número de filas que se van a almacenar en caché. Si omite este argumento, el valor se determina mediante el valor de la propiedad <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p>StartBookmark</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que especifica un marcador. La caché se rellena empezando por el registro indicado por este marcador. Si omite este argumento, la caché se rellena empezando por el registro indicado por la propiedad <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

El almacenamiento en caché mejora el rendimiento de una aplicación que recupera datos de un servidor remoto. Una caché es un espacio en la memoria local que almacena los datos recuperados más recientemente desde el servidor, bajo el supuesto de que los datos se volverán probablemente a recuperar mientras se ejecute la aplicación. Cuando un usuario solicita datos, el motor de base de datos de Microsoft Access comprueba primero los datos en la caché en lugar de recuperarlos del servidor, ya que este proceso tarda más tiempo. La caché no guarda los datos que no proceden de un origen de datos ODBC.

En lugar de esperar a que la caché se rellene con registros conforme éstos se recuperan, puede utilizar el método **FillCache** para rellenar explícitamente la caché en cualquier momento. Éste es un método más rápido para rellenar la caché porque **FillCache** recupera varios registros simultáneamente en lugar de recuperarlos uno por uno. Por ejemplo, mientras ve cada pantalla de registros, la aplicación utiliza **FillCache** para recuperar la siguiente pantalla de registros para su consulta.

Cualquier origen de datos ODBC conectado al motor de base de datos de Microsoft Access al que obtenga acceso con objetos **Recordset** puede tener una memoria caché local. Para crear la memoria caché, abra un objeto **Recordset** desde el origen de datos remoto y, a continuación, establezca las propiedades **CacheSize** y **CacheStart** del objeto **Recordset**.

Si rows y startbookmark crean un intervalo de registros que está parcial o totalmente fuera del intervalo de registros especificado por las propiedades **CacheSize** y **CacheStart** , la parte de recordset fuera de este intervalo se omite y no se cargará en la memoria caché.

Si **FillCache** solicita más registros que el número restante en el origen de datos remoto, el motor de base de datos de Microsoft Access sólo recupera los registros restantes y no se produce ningún error.


> [!NOTE]
> <UL>
> <LI>
> <P>Los registros recuperados de la caché no reflejan los cambios simultáneos realizados por otros usuarios en el origen de datos.</P>
> <LI>
> <P><STRONG>FillCache</STRONG> solo recupera los registros que aún no están almacenados en la memoria caché. Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad <STRONG>CacheSize</STRONG> del objeto <STRONG>Recordset</STRONG> en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, a continuación, use <STRONG>FillCache</STRONG>.</P></LI></UL>



## <a name="example"></a>Ejemplo

En este ejemplo se utilizan los métodos **CreateTableDef** y **FillCache** y las propiedades **CacheSize**, **CacheStart** y **SourceTableName** para enumerar dos veces los registros de una tabla vinculada. A continuación, se enumeran dos veces los registros con una caché de 50 registros. Por último, se muestran las estadísticas de rendimiento de las ejecuciones con y sin caché a través de la tabla vinculada.

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
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
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
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
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
