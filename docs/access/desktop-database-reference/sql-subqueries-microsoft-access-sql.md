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
ms.openlocfilehash: 4efa4e92d7fab2dc8a4aae932ccb1ffe69c7c6c8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026102"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>Subconsultas SQL (Microsoft Access SQL)


**Se aplica a**: Access 2013, Office 2013

Una subconsulta es una instrucción [SELECT](select-statement-microsoft-access-sql.md) anidada en una instrucción SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) o [UPDATE](update-statement-microsoft-access-sql.md) o en otra subconsulta.

## <a name="syntax"></a>Sintaxis

Puede usar tres formas de sintaxis para crear una subconsulta:

*comparación* \[ANY | TODOS LOS | Algunos\] (*instrucciónsql*)

*expresión* \[No\] IN (*instrucciónsql*)

\[NO\] EXISTS (*instrucciónsql*)

Una subconsulta consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>comparación</em></p></td>
<td><p>Expresión y operador de comparación que compara la expresión con los resultados de una subconsulta.</p></td>
</tr>
<tr class="even">
<td><p><em>expresión</em></p></td>
<td><p>Expresión que se busca en el conjunto de resultados de la subconsulta.</p></td>
</tr>
<tr class="odd">
<td><p><em>instrucciónSQL</em></p></td>
<td><p>Instrucción SELECT que sigue el mismo formato y las mismas reglas que todas las instrucciones SELECT. Debe incluirse entre paréntesis.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar una subconsulta en lugar de una expresión en la lista de campos de una instrucción SELECT o en una cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) o [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql). En una subconsulta, una instrucción SELECT se usa para proporcionar un conjunto de uno o varios valores específicos que evaluar en la expresión de la cláusula WHERE o HAVING.

Use el predicado ANY o SOME, que son sinónimos, para recuperar registros de la consulta principal que cumplan los criterios de la comparación con los registros recuperados en la subconsulta. En el siguiente ejemplo, se devuelven todos los productos cuyo precio unitario es mayor que el de cualquier producto vendido con un descuento mínimo del 25 por ciento:

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

Use el predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para recuperar sólo los registros de la consulta principal que cumplan los criterios de la comparación con todos los registros recuperados en al subconsulta. Si se cambia ANY por ALL en el ejemplo anterior, la consulta sólo devolvería los productos cuyo precio unitario fuera mayor que el de todos los productos vendidos con un descuento mínimo del 25 por ciento. Esto es mucho más restrictivo.

Use el predicado IN para recuperar únicamente los registros de la consulta principal para los que algún registro de la subconsulta contenga un valor igual. En el siguiente ejemplo, se devuelven todos los productos con un descuento mínimo del 25 por ciento:

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

Por otro lado, puede usar NOT IN para recuperar sólo los registros de la consulta principal para los que ningún registro de la subconsulta contiene un valor igual.

Use el predicado EXISTS (con la palabra reservada NOT opcional) en comparaciones de tipo verdadero/falso para determinar si la subconsulta devuelve algún registro.

También puede usar alias de nombre de tabla en una subconsulta para hacer referencia a las tablas enumeradas en una cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) fuera de la subconsulta. En el siguiente ejemplo, se devuelven los nombres de los empleados cuyos salarios son iguales o mayores que el salario medio de todos los empleados que tienen el mismo cargo. A la tabla Employees se asigna el alias "T1":

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

En el ejemplo anterior, la palabra reservada AS es opcional.

En consultas de tabla de referencias cruzadas se permiten algunas subconsultas, específicamente como predicados (los de la cláusula WHERE). En las consultas de tabla de referencias cruzadas no se permiten subconsultas como salida (las de la lista SELECT).

## <a name="example"></a>Ejemplo

En este ejemplo, se muestra el nombre y el contacto de todos los clientes que realizaron pedidos en el segundo trimestre de 1995. Se llama al procedimiento EnumFields, que puede encontrar en el ejemplo de la instrucción SELECT.

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
