---
title: 'Objeto index: objetos de acceso a datos (DAO)'
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291771"
---
# <a name="index-object-dao"></a>Objeto index (DAO)

**Se aplica a:** Access 2013, Office 2013

El objeto **Index** especifica el orden de los registros a los que se tiene acceso desde las tablas de la base de datos y si se aceptan o no los registros duplicados, lo que proporciona un acceso a los datos eficaz. Para bases de datos externas, los objetos **Index** describen los índices establecidos para tablas externas (sólo áreas de trabajo de Microsoft Access).

## <a name="remarks"></a>Comentarios

El motor de base de datos de Microsoft Access usa índices cuando combina tablas y crea objetos **[Recordset](recordset-object-dao.md)**. Los índices determinan el orden en el que los objetos **Recordset** de tipo tabla devuelven registros pero no determinan el orden en el que el motor de base de datos de Microsoft Access guarda los registros en la tabla base o el orden en el que cualquier otro tipo de objeto **Recordset** devuelve los registros.

Con un objeto **Index**, puede:

- Utilizar la propiedad **Required** para determinar si los objetos **[Field](field-object-dao.md)** del índice requieren valores que no sean Null y utilizar luego la propiedad **IgnoreNulls** para determinar si los valores Null tienen entradas de índice.

- Usar las propiedades **Primary** y **Unique** para determinar el orden y la exclusividad del objeto **Index**.

El motor de base de datos de Microsoft Access mantiene todos los índices de la tabla base de forma automática. Actualiza los índices siempre que agrega, cambia o elimina registros en la tabla base. Una vez que haya creado la base de datos, utilice el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** periódicamente para actualizar las estadísticas del índice.

Al tener acceso a un objeto **Recordset** de tipo tabla, especifica el orden de registros que usa la propiedad **Index** del objeto. Establezca esta propiedad en el valor de la propiedad **Name** de un objeto **Index** existente en la colección **Indexes**. Esta colección está incluida en el objeto **[TableDef](tabledef-object-dao.md)** subyacente al objeto **Recordset** que está llenando.

> [!NOTE]
> [!NOTA] No es necesario crear índices para las tablas, pero en tablas grandes y sin indizar el acceso a un registro determinado o el procesamiento de combinaciones puede llevar mucho tiempo. Por el contrario, si se tienen demasiados índices se pueden ralentizar las actualizaciones de la base de datos, ya que se corrigen todos los índices de la tabla.

La propiedad **[Attributes](field-attributes-property-dao.md)** de cada objeto **Field** del índice determina el orden de registros devueltos y, en consecuencia, qué técnicas de acceso se utilizan para este índice.

Cada objeto **Field** de la colección **Fields** de un objeto **Index** es un componente del índice. Para definir un nuevo objeto **Index**, establezca sus propiedades antes de anexarlo a una colección, lo que hace que el objeto **Index** esté disponible para un uso posterior.

> [!NOTE]
> [!NOTA] Puede modificar el valor de la propiedad **Name** de un objeto **Index** existente sólo si el valor de la propiedad **[Updatable](connection-updatable-property-dao.md)** del objeto **TableDef** que lo contiene es **True**.

Cuando establece una clave principal para una tabla, el motor de base de datos de Microsoft Access la define automáticamente como el índice principal. Un índice principal consta de uno o varios campos que identifican de manera única todos los registros de una tabla según un orden predefinido. Como el campo del índice principal debe ser único, el motor de base de datos de Microsoft Access establece la propiedad **Unique** del objeto **Index** principal en **True**. Si el índice principal se compone de varios campos, cada campo puede contener valores duplicados, pero la combinación de valores de todos los campos indizados debe ser única. Un índice principal consta de una clave para la tabla e incluye siempre los mismos campos que la clave principal.

> [!IMPORTANT]
> [!IMPORTANTE] Asegúrese de que los datos son conformes a los atributos del nuevo índice. Si el índice requiere valores únicos, asegúrese de que no haya duplicados en los registros de datos existentes. Si hay duplicados, el motor de base de datos de Microsoft Access no puede crear el índice; se produce un error capturable cuando intenta utilizar el método Append en el nuevo índice.

Al crear una relación que impone una integridad referencial, el motor de base de datos de Microsoft Access crea automáticamente un índice con la propiedad **Foreign**, establecido como clave externa en la tabla de referencia. Tras establecer una relación de tabla, el motor de base de datos de Microsoft Access impide realizar adiciones o cambios en la base de datos que infrinjan la relación. Si establece la propiedad **Attributes** del objeto **[Relation](relation-object-dao.md)** para que permita actualizaciones en cascada y eliminaciones en cascada, el motor de base de datos de Microsoft Access actualiza o elimina registros en las tablas relacionadas de forma automática.

1.  Utilice el método **CreateIndex** en un objeto **TableDef**.

2.  Use el método **CreateField** del objeto **Index** para crear un objeto **Field** para cada campo (columna) que se va a incluir en el objeto **Index**.

3.  Establezca las propiedades de **Index** como sea necesario.

4.  Anexe el objeto **Field** a la colección **Fields**.

5.  Anexe el objeto **Index** a la colección **Indexes**.

    > [!NOTE]
    > [!NOTA] Se omite la propiedad **Clustered** para las bases de datos que utilizan el motor de base de datos de Microsoft Access, que no admite índices agrupados.

## <a name="example"></a>Ejemplo

En este ejemplo se crea un nuevo objeto **Index**, se anexa a la colección **Indexes** del objeto **TableDef** de Empleados y se enumera la colección **Indexes** de **TableDef**. Por último, se enumera **Recordset**, utilizando primero el objeto **Index** principal y, luego, el nuevo objeto **Index**. Se requiere el procedimiento IndexOutput para que pueda ejecutarse este procedimiento.

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

En este ejemplo se utiliza el método **CreateIndex** para crear dos nuevos objetos **Index** y anexarlos luego a la colección **Indexes** del objeto **TableDef** de Empleados. Enumera la colección **Indexes** del objeto **TableDef**, la colección **Fields** de los nuevos objetos **Index** y la colección Properties de los nuevos objetos **Index**. Se requiere la función CreateIndexOutput para que pueda ejecutarse este procedimiento.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
