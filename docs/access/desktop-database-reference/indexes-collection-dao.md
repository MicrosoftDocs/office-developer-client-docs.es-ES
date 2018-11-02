---
title: Colección Indexes (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c6f610c329057156875065e149db1e914a282e4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920455"
---
# <a name="indexes-collection-dao"></a>Colección Indexes (DAO)


**Se aplica a**: Access 2013, Office 2013

Una colección **Indexes** contiene todos los objetos **Index** almacenados de un objeto **TableDef** (sólo áreas de trabajo de Microsoft Access).

## <a name="remarks"></a>Observaciones

Cuando obtenga acceso a un objeto Recordset de tipo de tabla, use la propiedad **Index** del objeto para especificar el orden de los registros. Establezca esta propiedad en el valor de la propiedad **Name** de un objeto **Index** existente en la colección **Indexes** del objeto **[TableDef](tabledef-object-dao.md)** subyacente al objeto **[Recordset](recordset-object-dao.md)**.


> [!NOTE]
> <P>[!NOTA] Sólo puede utilizar el método <STRONG>Append</STRONG> o <STRONG>Delete</STRONG> en una colección <STRONG>Indexes</STRONG> si el valor de la propiedad <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> del objeto <STRONG>TableDef</STRONG> integrante es <STRONG>True</STRONG>.</P>



Una vez creado un nuevo objeto **Index**, debe utilizar el método **Append** para agregarlo a la colección **Indexes** del objeto **TableDef**.


> [!IMPORTANT]
> <P>[!IMPORTANTE] Asegúrese de que los datos son compatibles con los atributos del nuevo índice. Si el índice requiere valores únicos, compruebe que no hay duplicados en los registros de datos existentes. Si hay duplicados, el motor de base de datos de Microsoft Access no puede crear el índice; se producirá un error capturable al intentar utilizar el método Append en el nuevo índice.</P>



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
