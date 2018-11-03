---
title: Subconsultas SQL (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b2a7bdadeb700bdbc6bf18dda2e73401afb7df86
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937354"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="6e7e0-102">Subconsultas SQL (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6e7e0-102">SQL subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="6e7e0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e7e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e7e0-104">Una subconsulta es una instrucción [SELECT](select-statement-microsoft-access-sql.md) anidada en una instrucción SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) o [UPDATE](update-statement-microsoft-access-sql.md) o en otra subconsulta.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e7e0-105">Syntax</span></span>

<span data-ttu-id="6e7e0-106">Puede usar tres formas de sintaxis para crear una subconsulta:</span><span class="sxs-lookup"><span data-stu-id="6e7e0-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="6e7e0-107">*comparación* \[ANY | TODOS LOS | Algunos\] (*instrucciónsql*)</span><span class="sxs-lookup"><span data-stu-id="6e7e0-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span></span>

<span data-ttu-id="6e7e0-108">*expresión* \[No\] IN (*instrucciónsql*)</span><span class="sxs-lookup"><span data-stu-id="6e7e0-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="6e7e0-109">\[NO\] EXISTS (*instrucciónsql*)</span><span class="sxs-lookup"><span data-stu-id="6e7e0-109">\[NOT\] EXISTS (*sqlstatement*)</span></span>

<span data-ttu-id="6e7e0-110">Una subconsulta consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6e7e0-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e7e0-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="6e7e0-111">Part</span></span></p></th>
<th><p><span data-ttu-id="6e7e0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e7e0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e7e0-113"><em>comparación</em></span><span class="sxs-lookup"><span data-stu-id="6e7e0-113"><em>comparison</em></span></span></p></td>
<td><p><span data-ttu-id="6e7e0-114">Expresión y operador de comparación que compara la expresión con los resultados de una subconsulta.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7e0-115"><em>expresión</em></span><span class="sxs-lookup"><span data-stu-id="6e7e0-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="6e7e0-116">Expresión que se busca en el conjunto de resultados de la subconsulta.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7e0-117"><em>instrucciónSQL</em></span><span class="sxs-lookup"><span data-stu-id="6e7e0-117"><em>sqlstatement</em></span></span></p></td>
<td><p><span data-ttu-id="6e7e0-p101">Instrucción SELECT que sigue el mismo formato y las mismas reglas que todas las instrucciones SELECT. Debe incluirse entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p101">A SELECT statement, following the same format and rules as any other SELECT statement. It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6e7e0-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e7e0-120">Remarks</span></span>

<span data-ttu-id="6e7e0-p102">Puede usar una subconsulta en lugar de una expresión en la lista de campos de una instrucción SELECT o en una cláusula [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) o [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)). En una subconsulta, una instrucción SELECT se usa para proporcionar un conjunto de uno o varios valores específicos que evaluar en la expresión de la cláusula WHERE o HAVING.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p102">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) or [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) clause. In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="6e7e0-p103">Use el predicado ANY o SOME, que son sinónimos, para recuperar registros de la consulta principal que cumplan los criterios de la comparación con los registros recuperados en la subconsulta. En el siguiente ejemplo, se devuelven todos los productos cuyo precio unitario es mayor que el de cualquier producto vendido con un descuento mínimo del 25 por ciento:</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p103">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery. The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="6e7e0-p104">Use el predicado [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) para recuperar sólo los registros de la consulta principal que cumplan los criterios de la comparación con todos los registros recuperados en al subconsulta. Si se cambia ANY por ALL en el ejemplo anterior, la consulta sólo devolvería los productos cuyo precio unitario fuera mayor que el de todos los productos vendidos con un descuento mínimo del 25 por ciento. Esto es mucho más restrictivo.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p104">Use the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery. If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more. This is much more restrictive.</span></span>

<span data-ttu-id="6e7e0-p105">Use el predicado IN para recuperar únicamente los registros de la consulta principal para los que algún registro de la subconsulta contenga un valor igual. En el siguiente ejemplo, se devuelven todos los productos con un descuento mínimo del 25 por ciento:</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p105">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value. The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="6e7e0-130">Por otro lado, puede usar NOT IN para recuperar sólo los registros de la consulta principal para los que ningún registro de la subconsulta contiene un valor igual.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="6e7e0-131">Use el predicado EXISTS (con la palabra reservada NOT opcional) en comparaciones de tipo verdadero/falso para determinar si la subconsulta devuelve algún registro.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="6e7e0-p106">También puede usar alias de nombre de tabla en una subconsulta para hacer referencia a las tablas enumeradas en una cláusula [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) fuera de la subconsulta. En el siguiente ejemplo, se devuelven los nombres de los empleados cuyos salarios son iguales o mayores que el salario medio de todos los empleados que tienen el mismo cargo. A la tabla Employees se asigna el alias "T1":</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="6e7e0-135">En el ejemplo anterior, la palabra reservada AS es opcional.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="6e7e0-p107">En consultas de tabla de referencias cruzadas se permiten algunas subconsultas, específicamente como predicados (los de la cláusula WHERE). En las consultas de tabla de referencias cruzadas no se permiten subconsultas como salida (las de la lista SELECT).</span><span class="sxs-lookup"><span data-stu-id="6e7e0-p107">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause). Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="6e7e0-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e7e0-138">Example</span></span>

<span data-ttu-id="6e7e0-139">En este ejemplo, se muestra el nombre y el contacto de todos los clientes que realizaron pedidos en el segundo trimestre de 1995.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="6e7e0-140">Se llama al procedimiento EnumFields, que puede encontrar en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="6e7e0-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```
