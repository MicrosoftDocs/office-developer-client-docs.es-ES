---
title: Instrucción CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE Statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 749d593a0c9ed32290ee91aec20c79a141a83f56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484977"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="a4131-102">Instrucción CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a4131-102">CREATE TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a4131-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4131-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a4131-104">Crea una tabla nueva.</span><span class="sxs-lookup"><span data-stu-id="a4131-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="a4131-p101">[!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE TABLE, o ninguna de las instrucciones DDL, con bases de datos cuyo motor no sea de Microsoft Access. En su lugar, use los métodos DAO Create.</span><span class="sxs-lookup"><span data-stu-id="a4131-p101">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4131-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4131-107">Syntax</span></span>

<span data-ttu-id="a4131-108">CREAR \[temporal\] tabla *tabla* (*campo1 tipo* \[(*tamaño*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[ *índice1* \] \[, *campo2* *tipo* \[(*tamaño*)\] \[NOT NULL\] \[ *índice2* \] \[,... \] \] \[, CONSTRAINT *índicedevarioscampos* \[,... \]\])</span><span class="sxs-lookup"><span data-stu-id="a4131-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="a4131-109">La instrucción CREATE TABLE tiene estas partes:</span><span class="sxs-lookup"><span data-stu-id="a4131-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4131-110">Parte</span><span class="sxs-lookup"><span data-stu-id="a4131-110">Part</span></span></p></th>
<th><p><span data-ttu-id="a4131-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4131-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4131-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="a4131-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="a4131-113">Nombre de la tabla que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="a4131-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4131-114"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="a4131-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="a4131-p102">El nombre del campo o de los campos que se crearán en la tabla nueva. Debe crear al menos un campo.</span><span class="sxs-lookup"><span data-stu-id="a4131-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4131-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="a4131-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="a4131-118">El tipo de datos del <em>campo</em> en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="a4131-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4131-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="a4131-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="a4131-120">Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</span><span class="sxs-lookup"><span data-stu-id="a4131-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4131-121"><em>index1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="a4131-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="a4131-p103">Cláusula CONSTRAINT que define un índice de un solo campo. Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </span><span class="sxs-lookup"><span data-stu-id="a4131-p103">A CONSTRAINT clause defining a single-field index. For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4131-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="a4131-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="a4131-p104">Cláusula CONSTRAINT que define un índice de varios campos. Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </span><span class="sxs-lookup"><span data-stu-id="a4131-p104">A CONSTRAINT clause defining a multiple-field index. For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a4131-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4131-127">Remarks</span></span>

<span data-ttu-id="a4131-p105">Use la instrucción CREATE TABLE para definir una nueva tabla y sus campos y restricciones de campos. Si se especifica NOT NULL para un campo, los nuevos registros deben tener datos válidos en ese campo.</span><span class="sxs-lookup"><span data-stu-id="a4131-p105">Use the CREATE TABLE statement to define a new table and its fields and field constraints. If NOT NULL is specified for a field, then new records are required to have valid data in that field.</span></span>

<span data-ttu-id="a4131-p106">Cláusula CONSTRAINT que establece varias restricciones en un campo y que se puede usar para establecer la clave primaria. También puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para crear una clave primaria o índices adicionales en tablas existentes.</span><span class="sxs-lookup"><span data-stu-id="a4131-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="a4131-p107">Puede usar NOT NULL en un solo campo o en una cláusula llamada CONSTRAINT que se aplica a un solo campo o a varios campos llamados CONSTRAINT. Sin embargo, puede aplicar la restricción NOT NULL una sola vez en un campo. Al intentar aplicar esta restricción más de una sola vez, se genera un error en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="a4131-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="a4131-p108">Cuando se crea una tabla TEMPORARY, queda visible solamente en la sesión en que fue creada. Se elimina automáticamente cuando la sesión finaliza. Más de un usuario puede tener acceso a las tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="a4131-p108">When a TEMPORARY table is created it is visible only within the session in which it was created. It is automatically deleted when the session is terminated. Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="a4131-138">El atributo WITH COMPRESSION puede usarse solo con los tipos de datos CHARACTER y MEMO (también conocidos como TEXT) y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="a4131-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="a4131-p109">El atributo WITH COMPRESSION se añadió para las columnas CHARACTER debido al cambio a formato de representación de caracteres Unicode. Los caracteres Unicode requieren uniformemente dos bytes para cada carácter. Para bases de datos existentes de Microsoft® Jet que contienen datos de caracteres principalmente, esto podría significar que el archivo de la base de datos tendría casi el doble de tamaño al convertirse a formato de motor de base de datos de Microsoft Access. Sin embargo, se puede comprimir fácilmente en un byte simple la representación Unicode de muchos conjuntos de caracteres, aquellos antes denominados como Single-Byte Character Sets (SBCS). Si define una columna CHARACTER con este atributo, los datos se comprimirán automáticamente mientras se almacenan y se descomprimirán al recuperarse de la columna.</span><span class="sxs-lookup"><span data-stu-id="a4131-p109">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format. Unicode characters uniformly require two bytes for each character. For existing Microsoft® Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format. However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS) can easily be compressed to a single byte. If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="a4131-p110">Las columnas MEMO también pueden definirse para almacenar datos en un formato comprimido. Sin embargo, existe una limitación. Solamente se comprimirán las instancias de columnas MEMO que, al comprimirse, tengan 4096 bytes o menos. Todas las demás instancias de columnas MEMO permanecerán sin comprimir. Esto significa que en una tabla determinada, para una columna MEMO determinada, algunos datos pueden comprimirse y algunos datos pueden no comprimirse.</span><span class="sxs-lookup"><span data-stu-id="a4131-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="a4131-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4131-149">Example</span></span>

<span data-ttu-id="a4131-150">Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.</span><span class="sxs-lookup"><span data-stu-id="a4131-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="a4131-151">Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.</span><span class="sxs-lookup"><span data-stu-id="a4131-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="a4131-p111">Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="a4131-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
