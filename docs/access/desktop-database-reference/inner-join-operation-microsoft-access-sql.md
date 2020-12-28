---
title: Operación INNER JOIN (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: d865d005604ed7422c8e33ff8508551b720c30ba
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734220"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="e2066-102">Operación INNER JOIN (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e2066-102">INNER JOIN operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="e2066-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2066-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e2066-104">Combina los registros de dos tablas si hay valores coincidentes en un campo común.</span><span class="sxs-lookup"><span data-stu-id="e2066-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2066-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2066-105">Syntax</span></span>

<span data-ttu-id="e2066-106">FROM *tabla1* INNER JOIN *tabla2* ON *tabla1*.*campo1\*\*operadorDeComparación tabla2*.*campo2*</span><span class="sxs-lookup"><span data-stu-id="e2066-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="e2066-107">La operación INNER JOIN consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="e2066-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2066-108">Part</span><span class="sxs-lookup"><span data-stu-id="e2066-108">Part</span></span></p></th>
<th><p><span data-ttu-id="e2066-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2066-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2066-110"><em>tabla1</em>, <em>tabla2</em></span><span class="sxs-lookup"><span data-stu-id="e2066-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="e2066-111">Nombres de las tablas cuyos registros se combinan.</span><span class="sxs-lookup"><span data-stu-id="e2066-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2066-112"><em>campo1 </em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="e2066-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="e2066-p101">Nombres de los campos que se combinan. Si no son numéricos, los campos deben ser del mismo tipo de datos y contener la misma clase de datos, pero pueden tener nombres distintos.</span><span class="sxs-lookup"><span data-stu-id="e2066-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2066-115"><em>opcomp</em></span><span class="sxs-lookup"><span data-stu-id="e2066-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="e2066-116">Cualquier operador de comparación relacional: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; o &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="e2066-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e2066-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2066-117">Remarks</span></span>

<span data-ttu-id="e2066-p102">Puede usar una operación INNER JOIN en una cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Este tipo de combinación es el más común. Las combinaciones internas combinan registros de dos tablas si hay valores coincidentes en un campo común a ambas.</span><span class="sxs-lookup"><span data-stu-id="e2066-p102">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="e2066-p103">Puede usar INNER JOIN con las tablas Departments y Employees para seleccionar todos los empleados de cada departamento En contraste, para seleccionar todos los departamentos (incluso si alguno no tiene empleados asignados) o todos los empleados (incluso si alguno no está asignado a un departamento), puede usar una operación [LEFT JOIN o RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) para crear una combinación externa.</span><span class="sxs-lookup"><span data-stu-id="e2066-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="e2066-123">Si intenta combinar campos que contienen datos Memo u Objeto OLE, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="e2066-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="e2066-p104">Puede combinar dos campos numéricos de tipos similares. Por ejemplo, puede combinar en campos Autonumeración y Largo porque son tipos similares. Pero no puede combinar los tipos de campo Sencillo y Doble.</span><span class="sxs-lookup"><span data-stu-id="e2066-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="e2066-127">En el siguiente ejemplo se muestra cómo se pueden combinar las tablas Categorías y Productos en el campo IdCategoría:</span><span class="sxs-lookup"><span data-stu-id="e2066-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="e2066-128">En el ejemplo anterior, CategoryID es el campo combinado, pero no se incluye en el resultado de la consulta porque no está contenido en la instrucción [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="e2066-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="e2066-129">Para incluir el campo combinado, escriba el nombre de campo en la instrucción SELECT (en este caso, Categories.CategoryID).</span><span class="sxs-lookup"><span data-stu-id="e2066-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="e2066-130">También puede vincular varias cláusulas ON en una instrucción JOIN mediante la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e2066-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="e2066-131">SELECT *campos* FROM *tabla1* INNER JOIN *tabla2* ON *tabla1*.*campo1* *operadorDeComparación* *tabla2*.*campo1* AND *tabla1*.*campo2* *operadorDeComparación* *tabla2*.*campo2* OR *tabla1*.*campo3* *operadorDeComparación* *tabla2*.*campo3*;</span><span class="sxs-lookup"><span data-stu-id="e2066-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span></span>

<span data-ttu-id="e2066-132">También puede anidar instrucciones JOIN mediante la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e2066-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="e2066-133">SELECT *campos* FROM *tabla1* INNER JOIN (*tabla2* INNER JOIN \[( \]*tabla3* \[INNER JOIN \[( \]*tablax* \[INNER JOIN …)\] ON *tabla3*.*campo3* *operadorDeComparación* *tablax*.*campox*)\] ON *tabla2*.*campo2* *operadorDeComparación* *tabla3*.*campo3*) ON *tabla1*.*campo1* *operadorDeComparación* *tabla2*.*campo2*;</span><span class="sxs-lookup"><span data-stu-id="e2066-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="e2066-134">LEFT JOIN o RIGHT JOIN se pueden anidar dentro de INNER JOIN, pero INNER JOIN no se puede anidar dentro de LEFT JOIN o RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="e2066-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="e2066-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2066-135">Example</span></span>

<span data-ttu-id="e2066-p106">En este ejemplo, se crean dos combinaciones de equivalencia: una entre las tablas Order Details y Orders, y otra entre las tablas Orders y Employees. Esto es necesario porque la tabla Employees no contiene datos de ventas y la tabla Order Details no contiene datos de empleados. La consulta produce una lista de empleados y sus ventas totales.</span><span class="sxs-lookup"><span data-stu-id="e2066-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="e2066-139">En este ejemplo, se llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="e2066-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
