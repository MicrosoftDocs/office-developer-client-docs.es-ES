---
title: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 050226506b3dc1d00f4323ae727763f7ba6bdc66
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026116"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="76caf-102">LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="76caf-102">LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="76caf-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76caf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76caf-104">Combina registros de una tabla de origen cuando se usa en una cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="76caf-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="76caf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76caf-105">Syntax</span></span>

<span data-ttu-id="76caf-106">FROM *tabla1* \[ izquierda | DERECHA \] JOIN *tabla2* ON *tabla1.campo1* *operadordecomparación tabla2.campo2*</span><span class="sxs-lookup"><span data-stu-id="76caf-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="76caf-107">Las operaciones LEFT JOIN y RIGHT JOIN constan de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="76caf-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76caf-108">Parte</span><span class="sxs-lookup"><span data-stu-id="76caf-108">Part</span></span></p></th>
<th><p><span data-ttu-id="76caf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="76caf-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76caf-110"><em>tabla1</em>, <em>tabla2</em></span><span class="sxs-lookup"><span data-stu-id="76caf-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="76caf-111">Nombres de las tablas en las que se combinan los registros.</span><span class="sxs-lookup"><span data-stu-id="76caf-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76caf-112"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="76caf-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="76caf-p101">Nombres de los campos que se combinan. Los campos deben ser del mismo tipo de datos y contener la misma clase de datos, pero no es necesario que tengan el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="76caf-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76caf-115"><em>operadorDeComparación</em></span><span class="sxs-lookup"><span data-stu-id="76caf-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="76caf-116">Cualquier operador de comparación relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; o &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="76caf-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="76caf-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76caf-117">Remarks</span></span>

<span data-ttu-id="76caf-p102">Use una operación LEFT JOIN para crear una combinación externa izquierda. Estas combinaciones incluyen todos los registros de la primera (izquierda) de dos tablas, incluso si no hay valores coincidentes para los registros en la segunda tabla (derecha).</span><span class="sxs-lookup"><span data-stu-id="76caf-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="76caf-p103">Use una operación RIGHT JOIN para crear una combinación externa derecha. Estas combinaciones incluyen todos los registros de la segunda (derecha) de dos tablas, incluso si no hay valores coincidentes para los registros de la primera tabla (izquierda).</span><span class="sxs-lookup"><span data-stu-id="76caf-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="76caf-p104">Por ejemplo, podría usar LEFT JOIN con las tablas Departamentos (izquierda) y Empleados (derecha) para seleccionar todos los departamentos, incluidos los que no tengan empleados asignados. Para seleccionar todos los empleados, incluidos los que no estén asignados a ningún departamento, utilizaría RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="76caf-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="76caf-p105">En el siguiente ejemplo, se muestra cómo puede combinar las tablas Categories y Products por el campo CategoryID. La consulta produce una lista de todas las categorías, incluidas las que no contienen ningún producto:</span><span class="sxs-lookup"><span data-stu-id="76caf-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="76caf-126">En este ejemplo, CategoryID es el campo combinado, pero no está incluido en los resultados de la consulta porque no está contenido en la instrucción [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="76caf-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="76caf-127">Para incluir el campo combinado, introduzca el nombre del campo en la instrucción SELECT, en este caso, SELECT.</span><span class="sxs-lookup"><span data-stu-id="76caf-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="76caf-128">[!NOTA] Para crear una consulta que incluya sólo los registros en los que los datos de los campos de combinación sean iguales, use una operación [INNER JOIN](inner-join-operation-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="76caf-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="76caf-p107">Las operaciones LEFT JOIN y RIGHT JOIN se pueden anidar en una operación INNER JOIN, pero una operación INNER JOIN no se puede anidar en una operación LEFT JOIN o RIGHT JOIN. Vea la descripción del anidamiento en el tema INNER JOIN acerca de cómo anidar unas combinaciones en otras.</span><span class="sxs-lookup"><span data-stu-id="76caf-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="76caf-p108">Puede vincular varias cláusulas ON. Vea la descripción de la vinculación de cláusulas en el tema de INNER JOIN acerca de cómo llevarlo a cabo.</span><span class="sxs-lookup"><span data-stu-id="76caf-p108">You can link multiple ON clauses. See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="76caf-133">Si se intenta combinar campos que contienen datos de tipo Memo u Objeto OLE, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="76caf-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="76caf-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76caf-134">Example</span></span>

<span data-ttu-id="76caf-135">En este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76caf-135">This example:</span></span>
- <span data-ttu-id="76caf-136">Se presupone la existencia de campos de nombre de departamento y el identificador de departamento hipotéticos en una tabla empleados.</span><span class="sxs-lookup"><span data-stu-id="76caf-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="76caf-137">Tenga en cuenta que estos campos no existen realmente en la tabla Employees (Empleados) de la base de datos Northwind (Neptuno).</span><span class="sxs-lookup"><span data-stu-id="76caf-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="76caf-138">Selecciona todos los departamentos, incluidos los que no tienen empleados.</span><span class="sxs-lookup"><span data-stu-id="76caf-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="76caf-139">Llama al procedimiento EnumFields, que puede encontrar en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="76caf-139">Calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


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
