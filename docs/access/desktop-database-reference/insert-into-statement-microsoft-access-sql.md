---
title: Instrucción INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1635ff8ad43af45a62cd2223be853cefb5b6e999
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870803"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="02c00-102">Instrucción INSERT INTO (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="02c00-102">INSERT INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="02c00-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02c00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02c00-p101">Añade un registro o varios registros a una tabla. A esto se le denomina consulta anexada.</span><span class="sxs-lookup"><span data-stu-id="02c00-p101">Adds a record or multiple records to a table. This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c00-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02c00-106">Syntax</span></span>

<span data-ttu-id="02c00-107">**Consulta de datos anexados de varios registros**:</span><span class="sxs-lookup"><span data-stu-id="02c00-107">**Multiple-record append query**:</span></span>

<span data-ttu-id="02c00-108">INSERT INTO *destino* \[(*campo1*\[, *field2*\[,... \] \])\] \[IN *basededatosexterna* \] seleccione \[ *origen*. \] *campo1*\[, *field2*\[,... \] FROM *expresióndetabla*</span><span class="sxs-lookup"><span data-stu-id="02c00-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

<span data-ttu-id="02c00-109">**Consulta de datos anexados de un único registro**:</span><span class="sxs-lookup"><span data-stu-id="02c00-109">**Single-record append query**:</span></span>

<span data-ttu-id="02c00-110">INSERT INTO *destino* \[(*campo1*\[, *field2*\[,... \] \])\] Valores (*valor1*\[, *valor2*\[,... \])</span><span class="sxs-lookup"><span data-stu-id="02c00-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="02c00-111">La instrucción INSERT INTO tiene estas partes:</span><span class="sxs-lookup"><span data-stu-id="02c00-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02c00-112">Parte</span><span class="sxs-lookup"><span data-stu-id="02c00-112">Part</span></span></p></th>
<th><p><span data-ttu-id="02c00-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="02c00-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c00-114"><em>target</em></span><span class="sxs-lookup"><span data-stu-id="02c00-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="02c00-115">El nombre de la tabla o consulta en la cual se anexarán los registros.</span><span class="sxs-lookup"><span data-stu-id="02c00-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c00-116"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="02c00-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="02c00-117">Los nombres de los campos para anexar datos, si sigue un argumento <em>destino</em> , o los nombres de campos para obtener datos, si la continuación del argumento <em>origen</em> .</span><span class="sxs-lookup"><span data-stu-id="02c00-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c00-118"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="02c00-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="02c00-p102">La ruta de acceso a una base de datos externa. Para obtener una descripción de la ruta de acceso, consulte la cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </span><span class="sxs-lookup"><span data-stu-id="02c00-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c00-121"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="02c00-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="02c00-122">El nombre de la tabla o consulta desde la cual se copiarán los registros.</span><span class="sxs-lookup"><span data-stu-id="02c00-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c00-123"><em>table1xpression</em></span><span class="sxs-lookup"><span data-stu-id="02c00-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="02c00-p103">El nombre de la tabla o de las tablas desde las cuales se insertarán los registros. Este argumento puede ser un único nombre de tabla o compuesto como resultado de una operación <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> o <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> o una consulta guardada.  </span><span class="sxs-lookup"><span data-stu-id="02c00-p103">The name of the table or tables from which records are inserted. This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c00-126"><em>value1</em>, <em>value2</em></span><span class="sxs-lookup"><span data-stu-id="02c00-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="02c00-p104">Los valores que se insertarán en los campos específicos del nuevo registro. Cada valor se inserta en el campo que corresponde a la posición del valor en la lista: <em>value1</em> se inserta en <em>field1</em> del nuevo registro, <em>value2</em> en <em>field2</em>, y así sucesivamente. Debe separar los valores con una coma y escribir los campos de texto entre comillas (' ').</span><span class="sxs-lookup"><span data-stu-id="02c00-p104">The values to insert into the specific fields of the new record. Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on. You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="02c00-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02c00-130">Remarks</span></span>

<span data-ttu-id="02c00-p105">Puede usar la instrucción INSERT INTO para añadir un solo registro a una tabla con la sintaxis de consulta anexada de un solo registro, tal como se muestra arriba. En este caso, el código especifica el nombre y el valor para cada campo del registro. Debe especificar cada uno de los campos del registro al cual se asignará un valor, y debe especificar un valor para ese campo. Cuando no especifica cada campo, el valor predeterminado o **Null** se inserta para las columnas que faltan. Los registros se añaden al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="02c00-p105">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above. In this case, your code specifies the name and value for each field of the record. You must specify each of the fields of the record that a value is to be assigned to and a value for that field. When you do not specify each field, the default value or **Null** is inserted for missing columns. Records are added to the end of the table.</span></span>

<span data-ttu-id="02c00-136">También puede utilizar INSERT INTO para anexar un conjunto de registros de otra tabla o consulta mediante la seleccionar...</span><span class="sxs-lookup"><span data-stu-id="02c00-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="02c00-137">FROM como se muestra en la sintaxis de consulta de datos anexados de varios registros.</span><span class="sxs-lookup"><span data-stu-id="02c00-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="02c00-138">En este caso, la cláusula SELECT especifica los campos que se anexará a la tabla de *destino* de especificado.</span><span class="sxs-lookup"><span data-stu-id="02c00-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="02c00-139">En la tabla de *origen* o *destino* puede especificar una tabla o una consulta.</span><span class="sxs-lookup"><span data-stu-id="02c00-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="02c00-140">Si se especifica una consulta, el motor de base de datos de Microsoft Access anexa los registros a cualquier tabla especificada por la consulta.</span><span class="sxs-lookup"><span data-stu-id="02c00-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="02c00-141">INSERT INTO es opcional pero, cuando se incluye, antecede a la instrucción [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="02c00-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="02c00-142">Si la tabla de destino contiene una clave primaria, asegúrese de anexar valores únicos que no sean **Null** al campo o a los campos de claves primarias. Si no lo hace, el motor de base de datos de Microsoft Access no anexará registros.</span><span class="sxs-lookup"><span data-stu-id="02c00-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="02c00-p108">Si anexa registros a una tabla con un campo AutoNumber y desea reenumerar los registros anexados, no incluya el campo AutoNumber en la consulta. Incluya el campo AutoNumber en la consulta si desea conservar los valores originales del campo.</span><span class="sxs-lookup"><span data-stu-id="02c00-p108">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query. Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="02c00-145">Use la cláusula IN para anexar registros a una tabla en otra base de datos.</span><span class="sxs-lookup"><span data-stu-id="02c00-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="02c00-146">Para crear una nueva tabla, use la instrucción [SELECT… INTO](select-into-statement-microsoft-access-sql.md) para crear una consulta de creación de tabla.</span><span class="sxs-lookup"><span data-stu-id="02c00-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="02c00-147">Para averiguar qué registros se anexarán antes de la ejecución de la consulta anexada, primero ejecute y vea los resultados de una consulta seleccionada que use los mismos criterios de selección.</span><span class="sxs-lookup"><span data-stu-id="02c00-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="02c00-p109">Una consulta anexada copia registros de una o más tablas a otra. Las tablas que contienen los registros que anexa no se ven afectadas por la consulta anexada.</span><span class="sxs-lookup"><span data-stu-id="02c00-p109">An append query copies records from one or more tables to another. The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="02c00-p110">En vez de anexar registros existentes de otra tabla, puede especificar el valor para cada campo en un solo registro nuevo con la cláusula VALUES. Si omite la lista de campos, la cláusula VALUES debe incluir un valor para cada campo en la tabla; de lo contrario, la operación INSERT fallará. Use una instrucción INSERT INTO adicional con una cláusula VALUES para cada registro adicional que desee crear.</span><span class="sxs-lookup"><span data-stu-id="02c00-p110">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause. If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail. Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="02c00-153">**Vínculos proporcionan por** la Comunidad [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="02c00-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="02c00-154">UtterAccess es el principal foro de ayuda y wiki sobre Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="02c00-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="02c00-155">Generación de números secuenciales para instrucciones INSERT/UPDATE</span><span class="sxs-lookup"><span data-stu-id="02c00-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="02c00-156">Herramienta de formato de SQL a VBA</span><span class="sxs-lookup"><span data-stu-id="02c00-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="02c00-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02c00-157">Example</span></span>

<span data-ttu-id="02c00-p112">Este ejemplo selecciona todos los registros en una tabla hipotética New Customers y los añade a la tabla Customers. Cuando no se designan columnas individuales, los nombres de columna de tabla SELECT deben coincidir exactamente con los nombres en la tabla INSERT INTO.</span><span class="sxs-lookup"><span data-stu-id="02c00-p112">This example selects all records in a hypothetical New Customers table and adds them to the Customers table. When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="02c00-160">Este ejemplo muestra un nuevo registro en la tabla Employees.</span><span class="sxs-lookup"><span data-stu-id="02c00-160">This example creates a new record in the Employees table.</span></span>

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

