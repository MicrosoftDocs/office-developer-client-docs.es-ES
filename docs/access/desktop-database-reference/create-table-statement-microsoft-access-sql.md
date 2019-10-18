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
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="7a191-102">Instrucción CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7a191-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7a191-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a191-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a191-104">Crear una tabla.</span><span class="sxs-lookup"><span data-stu-id="7a191-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="7a191-105">El motor de base de datos de Microsoft Access no admite el uso de CREATE TABLE, ni de ninguna de las instrucciones DDL, con bases de datos que no son del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7a191-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="7a191-106">En su lugar, use los métodos **Create** de DAO.</span><span class="sxs-lookup"><span data-stu-id="7a191-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a191-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a191-107">Syntax</span></span>

<span data-ttu-id="7a191-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="7a191-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="7a191-109">La instrucción CREATE TABLE consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="7a191-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a191-110">Part</span><span class="sxs-lookup"><span data-stu-id="7a191-110">Part</span></span></p></th>
<th><p><span data-ttu-id="7a191-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a191-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a191-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="7a191-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="7a191-113">El nombre de la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="7a191-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a191-114"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="7a191-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="7a191-p102">El nombre del campo o campos que se van a crear en la nueva tabla. Debe crear al menos un campo.</span><span class="sxs-lookup"><span data-stu-id="7a191-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a191-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="7a191-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="7a191-118">El tipo de datos de <em>campo</em> en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="7a191-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a191-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="7a191-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="7a191-120">Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</span><span class="sxs-lookup"><span data-stu-id="7a191-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a191-121"><em>índice1</em>, <em>índice2</em></span><span class="sxs-lookup"><span data-stu-id="7a191-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="7a191-122">Una cláusula CONSTRAINT que define un índice de un solo campo.</span><span class="sxs-lookup"><span data-stu-id="7a191-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="7a191-123">Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="7a191-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a191-124"><em>índice_de_varios_campos</em></span><span class="sxs-lookup"><span data-stu-id="7a191-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="7a191-125">Una cláusula CONSTRAINT que define un índice de varios campos.</span><span class="sxs-lookup"><span data-stu-id="7a191-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="7a191-126">Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="7a191-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7a191-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a191-127">Remarks</span></span>

<span data-ttu-id="7a191-128">Use la instrucción CREATE TABLE para definir una nueva tabla y sus campos y restricciones de campo.</span><span class="sxs-lookup"><span data-stu-id="7a191-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="7a191-129">Si se especifica NOT NULL para un campo, los nuevos registros deben tener datos válidos en ese campo.</span><span class="sxs-lookup"><span data-stu-id="7a191-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="7a191-p106">Cláusula CONSTRAINT que establece varias restricciones en un campo y que se puede usar para establecer la clave primaria. También puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para crear una clave primaria o índices adicionales en tablas existentes.</span><span class="sxs-lookup"><span data-stu-id="7a191-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="7a191-p107">Puede usar NOT NULL en un solo campo o en una cláusula CONSTRAINT con nombre que se aplica a un solo campo o a una cláusula CONSTRAINT con nombre de varios campos. Pero solo puede aplicar la restricción NOT NULL una vez a un campo. Intentar aplicar esta restricción más de una vez produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7a191-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="7a191-135">Cuando se crea una tabla TEMPORARY, queda visible solamente en la sesión en que fue creada.</span><span class="sxs-lookup"><span data-stu-id="7a191-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="7a191-136">Se elimina de manera automática cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="7a191-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="7a191-137">Más de un usuario puede tener acceso a las tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="7a191-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="7a191-138">Solo se puede usar el atributo WITH COMPRESSION con los tipos de datos CHARACTER y MEMO (también conocido como TEXT) y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="7a191-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="7a191-139">El atributo WITH COMPRESSION se agregó para las columnas CHARACTER debido al cambio en el formato de representación de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a191-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="7a191-140">Los caracteres Unicode requieren de manera uniforme dos bytes para cada carácter.</span><span class="sxs-lookup"><span data-stu-id="7a191-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="7a191-141">Para bases de datos existentes de Microsoft Jet que contienen datos de caracteres principalmente, esto podría significar que el archivo de la base de datos tendría casi el doble de tamaño al convertirse a formato de motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7a191-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="7a191-142">Sin embargo, se puede comprimir fácilmente en un byte simple la representación Unicode de muchos conjuntos de caracteres, aquellos antes denominados como Single-Byte Character Sets (SBCS).</span><span class="sxs-lookup"><span data-stu-id="7a191-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="7a191-143">Si define una columna CHARACTER con este atributo, los datos se comprimirán automáticamente cuando se almacenan y se descomprimen cuando se recuperan de la columna.</span><span class="sxs-lookup"><span data-stu-id="7a191-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="7a191-p110">También se pueden definir columnas MEMO para almacenar los datos en un formato comprimido. Pero hay una limitación. Solo se comprimirán las instancias de las columnas MEMO que, cuando se comprimen, encajan en 4096 bytes o menos. Todas las demás instancias de las columnas MEMO permanecerán sin comprimir. Esto significa que dentro de una tabla determinada, de una columna MEMO determinada, puede haber datos comprimidos y datos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="7a191-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="7a191-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a191-149">Example</span></span>

<span data-ttu-id="7a191-150">Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.</span><span class="sxs-lookup"><span data-stu-id="7a191-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="7a191-151">Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.</span><span class="sxs-lookup"><span data-stu-id="7a191-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="7a191-p111">Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="7a191-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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

<span data-ttu-id="7a191-154">Este ejemplo crea una nueva tabla denominada `~~Kitsch'n Sync` que muestra todos los diferentes tipos de campo e índice.</span><span class="sxs-lookup"><span data-stu-id="7a191-154">This example creates a new table called `~~Kitsch'n Sync` that demonstrates all the different field and index types.</span></span> <span data-ttu-id="7a191-155">El campo Autonumeración es la clave principal.</span><span class="sxs-lookup"><span data-stu-id="7a191-155">The SSN field is the primary key.</span></span>

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
