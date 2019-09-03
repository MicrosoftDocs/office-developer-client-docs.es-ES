---
title: Instrucción CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706176"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Instrucción CREATE TABLE (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crear una tabla.

> [!NOTE]
> El motor de base de datos de Microsoft Access no admite el uso de CREATE TABLE, ni de ninguna de las instrucciones DDL, con bases de datos que no son del motor de base de datos de Microsoft Access. En su lugar, use los métodos **Create** de DAO.

## <a name="syntax"></a>Sintaxis

CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])

La instrucción CREATE TABLE consta de las siguientes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>El nombre de la tabla que se va a crear.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>El nombre del campo o campos que se van a crear en la nueva tabla. Debe crear al menos un campo.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>El tipo de datos de <em>campo</em> en la nueva tabla.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</p></td>
</tr>
<tr class="odd">
<td><p><em>índice1</em>, <em>índice2</em></p></td>
<td><p>Una cláusula CONSTRAINT que define un índice de un solo campo. Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>índice_de_varios_campos</em></p></td>
<td><p>Una cláusula CONSTRAINT que define un índice de varios campos. Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use la instrucción CREATE TABLE para definir una nueva tabla y sus campos y restricciones de campo. Si se especifica NOT NULL para un campo, los nuevos registros deben tener datos válidos en ese campo.

Cláusula CONSTRAINT que establece varias restricciones en un campo y que se puede usar para establecer la clave primaria. También puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para crear una clave primaria o índices adicionales en tablas existentes.

Puede usar NOT NULL en un solo campo o en una cláusula CONSTRAINT con nombre que se aplica a un solo campo o a una cláusula CONSTRAINT con nombre de varios campos. Pero solo puede aplicar la restricción NOT NULL una vez a un campo. Intentar aplicar esta restricción más de una vez produce un error en tiempo de ejecución.

Cuando se crea una tabla TEMPORARY, queda visible solamente en la sesión en que fue creada. Se elimina de manera automática cuando finaliza la sesión. Más de un usuario puede tener acceso a las tablas temporales.

Solo se puede usar el atributo WITH COMPRESSION con los tipos de datos CHARACTER y MEMO (también conocido como TEXT) y sus sinónimos.

El atributo WITH COMPRESSION se agregó para las columnas CHARACTER debido al cambio en el formato de representación de caracteres Unicode. Los caracteres Unicode requieren de manera uniforme dos bytes para cada carácter. Para bases de datos existentes de Microsoft Jet que contienen datos de caracteres principalmente, esto podría significar que el archivo de la base de datos tendría casi el doble de tamaño al convertirse a formato de motor de base de datos de Microsoft Access. Sin embargo, se puede comprimir fácilmente en un byte simple la representación Unicode de muchos conjuntos de caracteres, aquellos antes denominados como Single-Byte Character Sets (SBCS). Si define una columna CHARACTER con este atributo, los datos se comprimirán automáticamente cuando se almacenan y se descomprimen cuando se recuperan de la columna.

También se pueden definir columnas MEMO para almacenar los datos en un formato comprimido. Pero hay una limitación. Solo se comprimirán las instancias de las columnas MEMO que, cuando se comprimen, encajan en 4096 bytes o menos. Todas las demás instancias de las columnas MEMO permanecerán sin comprimir. Esto significa que dentro de una tabla determinada, de una columna MEMO determinada, puede haber datos comprimidos y datos sin comprimir.

## <a name="example"></a>Ejemplo

Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Este ejemplo crea una nueva tabla denominada `~~Kitsch'n Sync` que muestra todos los diferentes tipos de campo e índice. El campo Autonumeración es la clave principal.

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
