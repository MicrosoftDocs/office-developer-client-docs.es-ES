---
title: Objeto TableDef (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e1e03cfcd1aeebc8fdfaf4287e53020a0bc8688
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881275"
---
# <a name="tabledef-object-dao"></a>Objeto TableDef (DAO)

**Se aplica a**: Access 2013, Office 2013

Un objeto **TableDef** representa la definición almacenada de una tabla base o una tabla vinculada (solo áreas de trabajo de Microsoft Access).

## <a name="remarks"></a>Comentarios

La definición de una tabla se manipula con un objeto **TableDef** y sus métodos y propiedades. Por ejemplo, puede:

- Examinar la estructura del índice y los campos de cualquier tabla local, vinculada o externa de una base de datos.

- Usar las propiedades **Connect** y **SourceTableName** para establecer o devolver información sobre las tablas vinculadas y utilizar el método **RefreshLink** para actualizar las conexiones con las tablas vinculadas.

- Usar las propiedades **ValidationRule** y **ValidationText** para establecer o devolver las condiciones de validación.

- Utilice el método **OpenRecordset** para crear una tabla –, Dynaset, dinámico, instantánea u objeto **Recordset** de tipo forward – only, según la definición de tabla.

En las tablas base, la propiedad **RecordCount** contiene el número de registros de la tabla de base de datos especificada. Para las tablas vinculadas, el valor de la propiedad **RecordCount** siempre es – 1.

Para crear un nuevo objeto **TableDef**, utilice el método **[CreateTableDef](database-createtabledef-method-dao.md)**.

### <a name="to-add-a-field-to-a-table"></a>Para agregar un campo a una tabla

1.  Compruebe que todos los objetos **[Recordset](recordset-object-dao.md)** que se basan en la tabla están cerrados.

2.  Utilice el método **CreateField** para crear una variable de objeto **Field** y establecer sus propiedades.

3.  Use el método **Append** para agregar el objeto **Field** a la colección **Fields** del objeto **TableDef**.

Puede eliminar un objeto **Field** desde una colección **TableDefs** si no tiene ningún índice asignado, pero perderá los datos del campo.

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>Para crear una tabla lista para nuevos registros en una base de datos

1.  Utilice el método **CreateTableDef** para crear un objeto **TableDef**.

2.  Establezca sus propiedades.

3.  Con cada campo de la tabla, use el método **CreateField** para crear una variable de objeto **Field** y establecer sus propiedades.

4.  Use el método **Append** para agregar los campos a la colección **Fields** del objeto **TableDef**.

5.  Utilice el método **Append** para agregar el nuevo objeto **TableDef** a la colección **TableDefs** del objeto **Database**.

Las tablas vinculadas se conectan a la base de datos con las propiedades **SourceTableName** y **Connect** del objeto **TableDef**.

### <a name="to-link-a-table-to-a-database"></a>Para vincular una tabla a una base de datos

1.  Utilice el método **CreateTableDef** para crear un objeto **TableDef**.

2.  Establezca sus propiedades **Connect** y **SourceTableName** (y, si quiere, también la propiedad **Attributes** ).

3.  Use el método **Append** para agregarlo a la colección **TableDefs** de un objeto **Database**.

Para hacer referencia a un objeto **TableDef** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

**Definiciones de tabla** (0)

**Definiciones de tabla** ("nombre")

**Definiciones de tabla**\!\[nombre\]

## <a name="example"></a>Ejemplo

En este ejemplo, se crea un nuevo objeto **TableDef** y se anexa a la colección **TableDefs** del objeto de base de datos Northwind. Luego, se enumeran la colección **TableDefs** y la colección **Properties** del nuevo **TableDef**.

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

En este ejemplo, se crea un nuevo objeto **TableDef** en la base de datos Northwind.

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
         If prpLoop <> "" Then Debug.Print "  " & _ 
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
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

En el siguiente ejemplo, se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
