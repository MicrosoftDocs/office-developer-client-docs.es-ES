---
title: Operaciones LEFT JOIN y RIGHT JOIN (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: c6e37cd68d586e39a06fd650ccb453f35477253f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290148"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="c1277-102">Operaciones LEFT JOIN y RIGHT JOIN (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c1277-102">LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="c1277-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1277-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1277-104">Combina registros de una tabla de origen cuando se usa en una cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="c1277-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1277-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1277-105">Syntax</span></span>

<span data-ttu-id="c1277-106">FROM *tabla1* \[ LEFT | RIGHT \] JOIN *tabla2* ON *tabla1.campo1* *operadorDeComparación tabla2.campo2*</span><span class="sxs-lookup"><span data-stu-id="c1277-106">FROM *table1* \[ [ LEFT | RIGHT ] JOIN *table2* 
    ON \*table1.field1 \* *compopr table2.field2*</span></span>

<span data-ttu-id="c1277-107">Las operaciones LEFT JOIN y RIGHT JOIN constan de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="c1277-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1277-108">Part</span><span class="sxs-lookup"><span data-stu-id="c1277-108">Part</span></span></p></th>
<th><p><span data-ttu-id="c1277-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1277-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1277-110"><em>tabla1</em>, <em>tabla2</em></span><span class="sxs-lookup"><span data-stu-id="c1277-110"><em>table1</em>  ,  <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="c1277-111">Nombres de las tablas cuyos registros se combinan.</span><span class="sxs-lookup"><span data-stu-id="c1277-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1277-112"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="c1277-112"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="c1277-p101">Nombres de los campos que se combinan. Estos campos deben ser del mismo tipo de datos y contener la misma clase de datos, pero no tienen que tener el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="c1277-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1277-115"><em>opcomp</em></span><span class="sxs-lookup"><span data-stu-id="c1277-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="c1277-116">Cualquier operador de comparación relacional: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; o &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="c1277-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c1277-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1277-117">Remarks</span></span>

<span data-ttu-id="c1277-p102">Use una operación LEFT JOIN para crear una combinación externa izquierda. Estas combinaciones incluyen todos los registros de la primera (izquierda) de dos tablas, incluso si no hay valores coincidentes para los registros en la segunda tabla (derecha).</span><span class="sxs-lookup"><span data-stu-id="c1277-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="c1277-p103">Use una operación RIGHT JOIN para crear una combinación externa derecha. Estas combinaciones incluyen todos los registros de la segunda (derecha) de dos tablas, incluso si no hay valores coincidentes para los registros de la primera tabla (izquierda).</span><span class="sxs-lookup"><span data-stu-id="c1277-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="c1277-p104">Por ejemplo, puede usar LEFT JOIN con las tablas Departamentos (izquierda) y Empleados (derecha) para seleccionar todos los departamentos, incluidos aquellos que no tengan ningún empleado asignado. Para seleccionar todos los empleados, incluidos aquellos que no estén asignados a un departamento, use RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="c1277-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="c1277-p105">En el ejemplo siguiente se muestra cómo combinar las tablas Categorías y Productos en el campo CategoryID. La consulta genera una lista de todas las categorías, incluidas aquellas que no contienen ningún producto:</span><span class="sxs-lookup"><span data-stu-id="c1277-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="c1277-126">En este ejemplo, CategoryID es el campo combinado, pero no está incluido en los resultados de la consulta porque no está contenido en la instrucción [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c1277-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="c1277-127">Para incluir el campo combinado, escriba el nombre de campo en la instrucción SELECT (en este caso, Categories.CategoryID).</span><span class="sxs-lookup"><span data-stu-id="c1277-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="c1277-128">Para crear una consulta que incluya sólo los registros en los que los datos de los campos de combinación sean iguales, use una operación [INNER JOIN](inner-join-operation-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c1277-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="c1277-p107">Las operaciones LEFT JOIN o RIGHT JOIN se pueden anidar dentro de una operación INNER JOIN, pero una operación INNER JOIN no se puede anidar dentro de una operación LEFT JOIN o RIGHT JOIN. Vea la discusión sobre anidamiento en el tema INNER JOIN para conocer cómo se anidan las combinaciones dentro de otras combinaciones.</span><span class="sxs-lookup"><span data-stu-id="c1277-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="c1277-131">Se pueden vincular varias cláusulas ON.</span><span class="sxs-lookup"><span data-stu-id="c1277-131">You can link multiple ON clauses.</span></span> <span data-ttu-id="c1277-132">Vea la discusión sobre la vinculación de cláusulas en el tema INNER JOIN para conocer el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c1277-132">See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="c1277-133">Si intenta combinar campos que contienen datos Memo u Objeto OLE, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c1277-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="c1277-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1277-134">Example</span></span>

<span data-ttu-id="c1277-135">Este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c1277-135">This is an example.</span></span>
- <span data-ttu-id="c1277-136">Supone la existencia de los campos hipotéticos Department Name (Nombre del departamento) y Department ID (Id. de departamento) en una tabla Employees (Empleados).</span><span class="sxs-lookup"><span data-stu-id="c1277-136">This example assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="c1277-137">Tenga en cuenta que estos campos no existen realmente en la tabla de empleados de la base de datos de Northwind.</span><span class="sxs-lookup"><span data-stu-id="c1277-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="c1277-138">Selecciona todos los departamentos, incluidos los que no tienen empleados.</span><span class="sxs-lookup"><span data-stu-id="c1277-138">This example selects all departments, including those without employees.</span></span>

- <span data-ttu-id="c1277-139">Llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="c1277-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example. 
 
</span></span>


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
