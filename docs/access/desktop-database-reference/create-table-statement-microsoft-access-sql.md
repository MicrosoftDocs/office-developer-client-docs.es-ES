---
title: Instrucción CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4beb013b09ce136d6ffa7558225e01fae80da645
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937095"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="526ec-102">Instrucción CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="526ec-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="526ec-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="526ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="526ec-104">Crea una tabla nueva.</span><span class="sxs-lookup"><span data-stu-id="526ec-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="526ec-105">[!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE TABLE, o ninguna de las instrucciones DDL, con bases de datos cuyo motor no sea de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="526ec-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="526ec-106">Utilice los métodos DAO **crear** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="526ec-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="526ec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="526ec-107">Syntax</span></span>

<span data-ttu-id="526ec-108">CREAR \[temporal\] tabla *tabla* (*campo1 tipo* \[(*tamaño*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[ *índice1* \] \[, *campo2* *tipo* \[(*tamaño*)\] \[NOT NULL\] \[ *índice2* \] \[,... \] \] \[, CONSTRAINT *índicedevarioscampos* \[,... \]\])</span><span class="sxs-lookup"><span data-stu-id="526ec-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="526ec-109">La instrucción CREATE TABLE tiene estas partes:</span><span class="sxs-lookup"><span data-stu-id="526ec-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="526ec-110">Parte</span><span class="sxs-lookup"><span data-stu-id="526ec-110">Part</span></span></p></th>
<th><p><span data-ttu-id="526ec-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="526ec-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="526ec-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="526ec-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="526ec-113">Nombre de la tabla que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="526ec-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="526ec-114"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="526ec-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="526ec-p102">El nombre del campo o de los campos que se crearán en la tabla nueva. Debe crear al menos un campo.</span><span class="sxs-lookup"><span data-stu-id="526ec-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="526ec-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="526ec-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="526ec-118">El tipo de datos del <em>campo</em> en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="526ec-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="526ec-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="526ec-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="526ec-120">Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</span><span class="sxs-lookup"><span data-stu-id="526ec-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="526ec-121"><em>index1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="526ec-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="526ec-122">Cláusula CONSTRAINT que define un índice de un solo campo.</span><span class="sxs-lookup"><span data-stu-id="526ec-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="526ec-123">Para obtener más información acerca de cómo crear este índice, vea <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="526ec-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="526ec-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="526ec-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="526ec-125">Cláusula CONSTRAINT que define un índice de varios campos.</span><span class="sxs-lookup"><span data-stu-id="526ec-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="526ec-126">Para obtener más información acerca de cómo crear este índice, vea <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="526ec-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="526ec-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="526ec-127">Remarks</span></span>

<span data-ttu-id="526ec-128">Use la instrucción CREATE TABLE para definir una nueva tabla y sus campos y restricciones de campos.</span><span class="sxs-lookup"><span data-stu-id="526ec-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="526ec-129">Si no se especifica NULL para un campo, se requieren nuevos registros tengan datos válidos en ese campo.</span><span class="sxs-lookup"><span data-stu-id="526ec-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="526ec-p106">Cláusula CONSTRAINT que establece varias restricciones en un campo y que se puede usar para establecer la clave primaria. También puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para crear una clave primaria o índices adicionales en tablas existentes.</span><span class="sxs-lookup"><span data-stu-id="526ec-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="526ec-p107">Puede usar NOT NULL en un solo campo o en una cláusula llamada CONSTRAINT que se aplica a un solo campo o a varios campos llamados CONSTRAINT. Sin embargo, puede aplicar la restricción NOT NULL una sola vez en un campo. Al intentar aplicar esta restricción más de una sola vez, se genera un error en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="526ec-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="526ec-135">Cuando se crea una tabla temporal, está visible sólo dentro de la sesión en el que se creó.</span><span class="sxs-lookup"><span data-stu-id="526ec-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="526ec-136">Se elimina automáticamente cuando la sesión finaliza.</span><span class="sxs-lookup"><span data-stu-id="526ec-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="526ec-137">Más de un usuario puede tener acceso a las tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="526ec-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="526ec-138">El atributo WITH COMPRESSION puede usarse solo con los tipos de datos CHARACTER y MEMO (también conocidos como TEXT) y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="526ec-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="526ec-139">El atributo WITH COMPRESSION se añadió para las columnas CHARACTER debido al cambio a formato de representación de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="526ec-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="526ec-140">Los caracteres Unicode requieren uniformemente dos bytes para cada carácter.</span><span class="sxs-lookup"><span data-stu-id="526ec-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="526ec-141">Para las bases de datos Microsoft Jet existentes que contienen predominantemente datos de caracteres, esto podría significar que el archivo de base de datos casi doblaría su tamaño cuando se convierte en el formato del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="526ec-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="526ec-142">Sin embargo, la representación Unicode de muchos juegos de caracteres, aquéllos previamente indicados como de Byte único carácter establece (SBCS), se puede comprimir fácilmente en un solo byte.</span><span class="sxs-lookup"><span data-stu-id="526ec-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="526ec-143">Si define una columna CHARACTER con este atributo, los datos se comprimirán automáticamente mientras se almacenan y se descomprimirán al recuperarse de la columna.</span><span class="sxs-lookup"><span data-stu-id="526ec-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="526ec-p110">Las columnas MEMO también pueden definirse para almacenar datos en un formato comprimido. Sin embargo, existe una limitación. Solamente se comprimirán las instancias de columnas MEMO que, al comprimirse, tengan 4096 bytes o menos. Todas las demás instancias de columnas MEMO permanecerán sin comprimir. Esto significa que en una tabla determinada, para una columna MEMO determinada, algunos datos pueden comprimirse y algunos datos pueden no comprimirse.</span><span class="sxs-lookup"><span data-stu-id="526ec-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="526ec-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="526ec-149">Example</span></span>

<span data-ttu-id="526ec-150">Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.</span><span class="sxs-lookup"><span data-stu-id="526ec-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="526ec-151">Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.</span><span class="sxs-lookup"><span data-stu-id="526ec-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="526ec-p111">Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="526ec-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
