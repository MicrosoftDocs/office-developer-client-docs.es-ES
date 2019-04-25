---
title: Método Database.CreateTableDef (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c986f0a96c14dac8a9ee4f3c7fded5a049fa451e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294949"
---
# <a name="databasecreatetabledef-method-dao"></a>Método Database.CreateTableDef (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[TableDef](tabledef-object-dao.md)** (solo áreas de trabajo de Microsoft Access). .

## <a name="syntax"></a>Sintaxis

*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)

*expression* Variable que representa un objeto **Database**.

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
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>TableDef</strong>. Vea el tema relativo a la propiedad <strong><a href="tabledef-name-property-dao.md">Name</a></strong> para obtener información sobre los nombres de <strong>TableDef</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>Atributos</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante o una combinación de constantes que indica una o varias de las características del nuevo objeto <strong>TableDef</strong>. Vea el tema relativo a la propiedad <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> para obtener más información.</p></td>
</tr>
<tr class="odd">
<td><p><em>SourceTableName</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que contiene el nombre de una tabla en una base de datos externa que es el origen de los datos. La cadena de origen se convierte en el valor de la propiedad <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> del nuevo objeto <strong>TableDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que contiene información sobre el origen de una base de datos abierta, una base de datos utilizada en una consulta de paso o una tabla vinculada. Vea el tema relativo a la propiedad <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> para obtener más información sobre las cadenas de conexión válidas.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

TableDef

## <a name="remarks"></a>Comentarios

Si omite uno o varios de los argumentos opcionales cuando utiliza el método **CreateTableDef**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunas pero no todas sus propiedades. Vea los temas correspondientes a cada propiedad para obtener información más detallada.

Si name hace referencia a un objeto que ya es un miembro de la colección, o especifica una propiedad no válida en el objeto **TableDef** o **[Field](field-object-dao.md)** que va a agregar, se produce un error en tiempo de ejecución al utilizar el método **[Append](tabledefs-append-method-dao.md)**. Asimismo, no puede agregar un objeto **TableDef** a la colección **TableDefs** hasta que defina al menos un objeto **Field** para el objeto **TableDef**.

Para quitar un objeto **TableDef** de la colección **[TableDefs](tabledefs-collection-dao.md)**, utilice el método **[Delete](tabledefs-delete-method-dao.md)** en la colección.

## <a name="example"></a>Ejemplo

En este ejemplo se crea un nuevo objeto **TableDef** en la base de datos Northwind.

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

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
