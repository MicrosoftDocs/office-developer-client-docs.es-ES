---
title: Operación UNION (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314703"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="6ec03-102">Operación UNION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6ec03-102">UNION Operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="6ec03-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ec03-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ec03-104">Crea una consulta de unión, que combina los resultados de dos o más consultas o tablas independientes.</span><span class="sxs-lookup"><span data-stu-id="6ec03-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ec03-105">Syntax</span></span>

<span data-ttu-id="6ec03-106">\[TABLE\] *consulta1* UNION \[ALL\] \[TABLE\] *consulta2* \[UNION \[ALL\] \[TABLE\] *consultan* \[ …</span><span class="sxs-lookup"><span data-stu-id="6ec03-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="6ec03-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="6ec03-107"></span></span>

<span data-ttu-id="6ec03-108">La operación UNION consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="6ec03-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ec03-109">Part</span><span class="sxs-lookup"><span data-stu-id="6ec03-109">Part</span></span></p></th>
<th><p><span data-ttu-id="6ec03-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ec03-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ec03-111"><em>consulta1-n</em></span><span class="sxs-lookup"><span data-stu-id="6ec03-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="6ec03-112">Instrucción SELECT, nombre de una consulta almacenada o nombre de una tabla almacenada precedido de la palabra clave TABLE.</span><span class="sxs-lookup"><span data-stu-id="6ec03-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6ec03-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ec03-113">Remarks</span></span>

<span data-ttu-id="6ec03-p102">Puede combinar los resultados de dos o más consultas, tablas e instrucciones SELECT en cualquier combinación, en una sola operación UNION. En el ejemplo siguiente se combina una tabla existente denominada Nuevas cuentas y una instrucción SELECT:</span><span class="sxs-lookup"><span data-stu-id="6ec03-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="6ec03-p103">De forma predeterminada, no se devuelven registros duplicados cuando se usa la operación UNION; sin embargo, puede incluir el predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para asegurarse de que se devuelven todos los registros. Además, de esta manera, la consulta se ejecuta más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="6ec03-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="6ec03-118">Todas las consultas de una operación UNION deben solicitar el mismo número de campos; sin embargo, no es necesario que los campos sean del mismo tamaño o tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6ec03-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="6ec03-p104">Use alias solo en la primera instrucción SELECT ya que en las demás se ignorarán. En la cláusula ORDER BY, haga referencia a los campos por su nombre en la primera instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="6ec03-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="6ec03-121">Puede usar una cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) o [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) en cada argumento de *consulta* para agrupar los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="6ec03-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="6ec03-122">Puede usar una cláusula [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) al final del último argumento de *consulta* para mostrar los datos devueltos en un orden especificado.</span><span class="sxs-lookup"><span data-stu-id="6ec03-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="6ec03-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ec03-123">Example</span></span>

<span data-ttu-id="6ec03-124">En este ejemplo se recuperan los nombres y ciudades de todos los proveedores y los clientes de Brasil.</span><span class="sxs-lookup"><span data-stu-id="6ec03-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="6ec03-125">Llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="6ec03-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.

</span></span>

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
