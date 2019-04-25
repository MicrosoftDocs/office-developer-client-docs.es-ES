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
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295362"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="ec109-102">Instrucción CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ec109-102">CREATE TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ec109-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec109-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec109-104">Crear una tabla.</span><span class="sxs-lookup"><span data-stu-id="ec109-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="ec109-105">El motor de base de datos de Microsoft Access no admite el uso de CREATE TABLE, ni de ninguna de las instrucciones DDL, con bases de datos que no son del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ec109-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="ec109-106">En su lugar, use los métodos **Create** de DAO.</span><span class="sxs-lookup"><span data-stu-id="ec109-106">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec109-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec109-107">Syntax</span></span>

<span data-ttu-id="ec109-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="ec109-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="ec109-109">La instrucción CREATE TABLE consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="ec109-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec109-110">Part</span><span class="sxs-lookup"><span data-stu-id="ec109-110">Part</span></span></p></th>
<th><p><span data-ttu-id="ec109-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec109-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec109-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="ec109-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="ec109-113">El nombre de la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="ec109-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec109-114"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="ec109-114"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="ec109-p102">El nombre del campo o campos que se van a crear en la nueva tabla. Debe crear al menos un campo.</span><span class="sxs-lookup"><span data-stu-id="ec109-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec109-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="ec109-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="ec109-118">El tipo de datos de <em>campo</em> en la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="ec109-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec109-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="ec109-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="ec109-120">Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</span><span class="sxs-lookup"><span data-stu-id="ec109-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec109-121"><em>índice1</em>, <em>índice2</em></span><span class="sxs-lookup"><span data-stu-id="ec109-121"><em>index1</em>  ,  <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="ec109-122">Una cláusula CONSTRAINT que define un índice de un solo campo.</span><span class="sxs-lookup"><span data-stu-id="ec109-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="ec109-123">Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="ec109-123">For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec109-124"><em>índice_de_varios_campos</em></span><span class="sxs-lookup"><span data-stu-id="ec109-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="ec109-125">Una cláusula CONSTRAINT que define un índice de varios campos.</span><span class="sxs-lookup"><span data-stu-id="ec109-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="ec109-126">Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="ec109-126">For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ec109-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec109-127">Remarks</span></span>

<span data-ttu-id="ec109-128">Use la instrucción CREATE TABLE para definir una nueva tabla y sus campos y restricciones de campo.</span><span class="sxs-lookup"><span data-stu-id="ec109-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="ec109-129">Si se especifica NOT NULL para un campo, los nuevos registros deben tener datos válidos en ese campo.</span><span class="sxs-lookup"><span data-stu-id="ec109-129">If NOT NULL is specified for a field, then new records are required to have valid data in that field.</span></span>

<span data-ttu-id="ec109-p106">Cláusula CONSTRAINT que establece varias restricciones en un campo y que se puede usar para establecer la clave primaria. También puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para crear una clave primaria o índices adicionales en tablas existentes.</span><span class="sxs-lookup"><span data-stu-id="ec109-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="ec109-p107">Puede usar NOT NULL en un solo campo o en una cláusula CONSTRAINT con nombre que se aplica a un solo campo o a una cláusula CONSTRAINT con nombre de varios campos. Pero solo puede aplicar la restricción NOT NULL una vez a un campo. Intentar aplicar esta restricción más de una vez produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ec109-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="ec109-135">Cuando se crea una tabla TEMPORARY, queda visible solamente en la sesión en que fue creada.</span><span class="sxs-lookup"><span data-stu-id="ec109-135">When a TEMPORARY table is created it is visible only within the session in which it was created.</span></span> <span data-ttu-id="ec109-136">Se elimina de manera automática cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="ec109-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="ec109-137">Más de un usuario puede tener acceso a las tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="ec109-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="ec109-138">Solo se puede usar el atributo WITH COMPRESSION con los tipos de datos CHARACTER y MEMO (también conocido como TEXT) y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="ec109-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="ec109-139">El atributo WITH COMPRESSION se agregó para las columnas CHARACTER debido al cambio en el formato de representación de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ec109-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="ec109-140">Los caracteres Unicode requieren de manera uniforme dos bytes para cada carácter.</span><span class="sxs-lookup"><span data-stu-id="ec109-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="ec109-141">Para bases de datos existentes de Microsoft Jet que contienen datos de caracteres principalmente, esto podría significar que el archivo de la base de datos tendría casi el doble de tamaño al convertirse a formato de motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ec109-141">For existing Microsoft® Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="ec109-142">Sin embargo, se puede comprimir fácilmente en un byte simple la representación Unicode de muchos conjuntos de caracteres, aquellos antes denominados como Single-Byte Character Sets (SBCS).</span><span class="sxs-lookup"><span data-stu-id="ec109-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS) can easily be compressed to a single byte.</span></span> <span data-ttu-id="ec109-143">Si define una columna CHARACTER con este atributo, los datos se comprimirán automáticamente cuando se almacenan y se descomprimen cuando se recuperan de la columna.</span><span class="sxs-lookup"><span data-stu-id="ec109-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="ec109-p110">También se pueden definir columnas MEMO para almacenar los datos en un formato comprimido. Pero hay una limitación. Solo se comprimirán las instancias de las columnas MEMO que, cuando se comprimen, encajan en 4096 bytes o menos. Todas las demás instancias de las columnas MEMO permanecerán sin comprimir. Esto significa que dentro de una tabla determinada, de una columna MEMO determinada, puede haber datos comprimidos y datos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="ec109-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="ec109-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec109-149">Example</span></span>

<span data-ttu-id="ec109-150">Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.</span><span class="sxs-lookup"><span data-stu-id="ec109-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="ec109-151">Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.</span><span class="sxs-lookup"><span data-stu-id="ec109-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="ec109-p111">Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="ec109-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
