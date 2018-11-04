---
title: Database.CreateRelation (método) (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2a1ad7798fc6236f95d31c18cd864fe64e7a3fd8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949932"
---
# <a name="databasecreaterelation-method-dao"></a>Database.CreateRelation (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Crea un nuevo objeto **[Relation](relation-object-dao.md)** (solo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CreateRelation (***nombre***, ***tabla***, ***ForeignTable***, ***atributos***)

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="parameters"></a>Parámetros

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
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>Relation</strong>. Vea el tema relativo a la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener información sobre los nombres de <strong>Relation</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que designa la tabla principal de la relación. Si la tabla no existe antes de agregar el objeto <strong>Relation</strong>, se produce un error en tiempo de ejecución.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que designa la tabla externa de la relación. Si la tabla no existe antes de agregar el objeto <strong>Relation</strong>, se produce un error en tiempo de ejecución.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante o combinación de constantes que contienen información sobre el tipo de relación. Vea el tema relativo a la propiedad <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> para obtener información detallada.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Relation

## <a name="remarks"></a>Observaciones

El objeto **Relation** proporciona información al motor de base de datos de Microsoft Access sobre la relación entre los campos de dos objetos **[TableDef](tabledef-object-dao.md)** o **[QueryDef](querydef-object-dao.md)**. Puede implementar integridad referencial mediante la propiedad **Attributes**.

Si omite uno o varios de los argumentos opcionales cuando utiliza el método **CreateRelation**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, no podrá modificar todos los valores de la propiedad. Vea los temas correspondientes a cada propiedad para obtener información más detallada.

Antes de utilizar el método **[Append](fields-append-method-dao.md)** en un objeto **Relation**, debe agregar los objetos **[Field](field-object-dao.md)** correspondientes para definir las tablas principal y externa de la relación.

Si name hace referencia a un objeto que ya es un miembro de la colección, o si los nombres de objeto **Field** proporcionados en la colección **Fields** subordinada no son válidos, se produce un error en tiempo de ejecución cuando se utiliza el método **Append** .

No se puede establecer ni mantener una relación entre una tabla replicada y una tabla local.

Para quitar un objeto **Relation** de la colección **[Relations](relations-collection-dao.md)**, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.

## <a name="example"></a>Ejemplo

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
