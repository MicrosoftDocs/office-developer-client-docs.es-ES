---
title: Objeto Relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cfabb36e539aaff1f6e12d431d2cfcfe79ff5d04
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928092"
---
# <a name="relation-object-dao"></a>Objeto Relation (DAO)


**Se aplica a**: Access 2013, Office 2013

Un objeto **Relation** representa una relación entre campos de tablas o consultas (sólo bases de datos del motor de base de datos de Microsoft Access).

## <a name="remarks"></a>Observaciones

Puede usar el objeto **Relation** para crear nuevas relaciones y examinar las relaciones existentes en la base de datos.

Mediante un objeto **Relation** y sus propiedades, se puede:

  - Especificar una relación exigida entre campos de tablas base (pero no una relación que incluya una consulta o una tabla vinculada).

  - Establecer relaciones no exigidas entre cualquier tipo de tabla o consulta, ya sea nativa o vinculada.

  - Usar la propiedad **Name** para especificar la relación entre los campos de la tabla principal a la que se hace referencia y la tabla externa de referencia.

  - Usar la propiedad **Attributes** para determinar si la relación entre los campos de la tabla es uno a uno o uno a varios, y cómo exigir la integridad referencial.

  - Usar la propiedad **Attributes** para determinar si el motor de base de datos de Microsoft Access puede realizar operaciones de actualización y eliminación en cascada en tablas principales y externas.

  - Usar la propiedad **Attributes** para determinar si la relación entre los campos de la tabla es una combinación izquierda o una combinación derecha.

  - Usar la propiedad **Name** de todos los objetos **Field** de la colección **Fields** de un objeto **Relation**, para establecer o devolver los nombres de los campos de la clave principal de la tabla a la que se hace referencia o la configuración de la propiedad **ForeignName** de los objetos **Field**, para establecer o devolver los nombres de los campos de la clave externa de la tabla de referencia.

Si se realizan cambios que infringen las relaciones establecidas para la base de datos, se produce un error capturable. Si se solicitan operaciones de actualización en cascada o eliminación en cascada, el motor de base de datos de Microsoft Access también modifica las tablas de clave principal o clave externa para exigir las relaciones que se establezcan.

Por ejemplo, la base de datos Neptuno contiene una relación entre la tabla Pedidos y la tabla Clientes. El campo IdCliente de la tabla Clientes es la clave principal y el campo IdCliente de la tabla Pedidos es la clave externa. Para que el motor de base de datos de Microsoft Access acepte un registro nuevo en la tabla Pedidos, busca en la tabla Clientes una coincidencia en el campo IdCliente de la tabla Pedidos. Si el motor de base de datos de Microsoft Access no encuentra una coincidencia, no acepta el nuevo registro y se produce un error capturable.

Cuando se exige la integridad referencial, debe existir un índice único para el campo de clave de la tabla a la que se hace referencia. El motor de base de datos de Microsoft Access crea automáticamente un índice con la propiedad **Foreign** establecida para actuar como la clave externa de la tabla de referencia.

Para crear un nuevo objeto **Relation**, utilice el método **CreateRelation**. Para hacer referencia a un objeto **Relation** de una colección por su número ordinal o por su valor de la propiedad **Name**, utilice uno de los siguientes formatos de sintaxis:

**Relations**(0)

**Relaciones** ("nombre")

**Relaciones de**\!\[nombre\]

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo un objeto **Relation** existente puede controlar la entrada de datos. El procedimiento intenta agregar un registro con un CategoryID deliberadamente incorrecto, que desencadena una rutina de tratamiento de errores.

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

En este ejemplo se utiliza el método **CreateRelation** para crear una **Relation** entre el objeto **TableDef** de empleados y un nuevo objeto **TableDef** denominado Departments (departamentos). En este ejemplo se muestra también cómo al crear una nueva **Relation** se crean también los **Indexes** necesarios en la tabla externa (el índice DepartmentsEmployees de la tabla Employees).

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
