---
title: 'Objetos de objeto de campo: acceso a datos (DAO)'
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc4fa671fd6b98d036101c7f5df06221a0a9ff74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484543"
---
# <a name="field-object-dao"></a>Field Object (DAO)

**Se aplica a**: Access 2013 | Office 2013

Un objeto **Field** representa una columna de datos con un tipo de datos común y un conjunto de propiedades común.

## <a name="remarks"></a>Observaciones

Las colecciones **Fields** de los objetos **Index**, **QueryDef**, **Relation** y **TableDef** contienen las especificaciones para los campos que estos objetos representan. La colección **Fields** de un objeto **Recordset** representa los objetos **Field** de una fila de datos o de un registro. Use los objetos **Field** de un objeto **Recordset** para leer y establecer valores para los campos en el registro activo del objeto **Recordset**.

En un área de trabajo de Microsoft Access, puede modificar un campo mediante un objeto **Field** y sus métodos y propiedades. Por ejemplo, puede:

  - Utilizar la propiedad **OrdinalPosition** para establecer o devolver el orden de presentación del objeto **Field** en una colección **Fields**.

  - Usar la propiedad **Value** de un campo en un objeto **Recordset** para establecer o devolver datos guardados.

  - Usar los métodos **AppendChunk** y **GetChunk** y la propiedad **FieldSize** para obtener o establecer un valor en un campo de tipo Objeto o Memo OLE de un objeto **Recordset**.

  - Usar las propiedades **Type**, **Size** y **Attributes** para determinar el tipo de datos que se pueden guardar en el campo.

  - Utilizar las propiedades **SourceField** y **SourceTable** para determinar el origen de los datos original.

  - Usar la propiedad **ForeignName** para establecer o devolver información sobre un campo externo de un objeto **Relation**.

  - Utilizar las propiedades **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** o **ValidationText** para establecer o devolver condiciones de validación.

  - Usar la propiedad **DefaultValue** de un campo en un **TableDef** para establecer el valor predeterminado para este campo cuando se agregan nuevos registros.

Para crear un nuevo objeto **Field** en un objeto **Index**, **TableDef** o **Relation**, utilice el método **CreateField**.

Cuando tiene acceso a un objeto **Field** como parte de un objeto **Recordset**, los datos del registro activo están visibles en la propiedad **Value** del objeto **Field**. Para manipular datos en el objeto **Recordset**, no suele hacer referencia a la colección **Fields** directamente, sino que hace referencia indirectamente a la propiedad **Value** del objeto **Field** en la colección **Fields** del objeto **Recordset**.

Para hacer referencia a un objeto **Field** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

- **Fields**(0)

- **Campos** ("nombre")

- **Campos**\!\[nombre\]

Con las mismas formas sintácticas, puede hacer referencia igualmente a la propiedad **Value** de un objeto **Field** que crea y anexa a la colección **Fields**. El contexto de la referencia del campo determinará si hace referencia al objeto **Field** o a la propiedad **Value** del objeto **Field**.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra qué propiedades son válidas para un objeto **Field** según dónde resida el objeto **Field** (por ejemplo, la colección **Fields** de un objeto **TableDef**, la colección **Fields** de un objeto **QueryDef**, etc.). Se requiere el procedimiento FieldOutput para que pueda ejecutarse este procedimiento.

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

En este ejemplo se utiliza el método **CreateField** para crear tres **Fields** para un nuevo objeto **TableDef**. A continuación, se muestran las propiedades de estos objetos **Field** que se establecen automáticamente mediante el método **CreateField**. (No aparecen las propiedades cuyos valores están vacíos en el momento de crear **Field**.)

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
