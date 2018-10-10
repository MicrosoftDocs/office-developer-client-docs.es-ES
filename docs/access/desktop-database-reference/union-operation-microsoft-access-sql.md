---
title: UNION (operación de Microsoft Access SQL)
TOCTitle: UNION Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 9a06a5598716bb57d05048d861fcb13b1813365f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484635"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="39303-102">UNION (operación de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="39303-102">UNION Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="39303-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="39303-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="39303-104">Crea una consulta de unión, que combina los resultados de dos o más consultas o tablas independientes.</span><span class="sxs-lookup"><span data-stu-id="39303-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="39303-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39303-105">Syntax</span></span>

<span data-ttu-id="39303-106">\[TABLA\] *Consulta1* UNION \[todos los\] \[tabla\] *consulta2* \[unión \[todos los\] \[tabla\] *consultan* \[ ...</span><span class="sxs-lookup"><span data-stu-id="39303-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="39303-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="39303-107"></span></span>

<span data-ttu-id="39303-108">La operación UNION consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="39303-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39303-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="39303-109">Part</span></span></p></th>
<th><p><span data-ttu-id="39303-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="39303-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39303-111"><em>consulta1-n</em></span><span class="sxs-lookup"><span data-stu-id="39303-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="39303-112">Instrucción SELECT, nombre de una consulta almacenada o nombre de una tabla almacenada precedido de la palabra clave TABLE.</span><span class="sxs-lookup"><span data-stu-id="39303-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="39303-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39303-113">Remarks</span></span>

<span data-ttu-id="39303-p102">Puede combinar los resultados de dos o más consultas, tablas e instrucciones SELECT, en cualquier combinación, en una sola operación UNION. En el siguiente ejemplo, se combinan una tabla existente denominada New Accounts (Nuevas cuentas) y una instrucción SELECT:</span><span class="sxs-lookup"><span data-stu-id="39303-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="39303-p103">De forma predeterminada, no se devuelven registros duplicados cuando se usa la operación UNION; sin embargo, puede incluir el predicado [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) para asegurarse de que se devuelven todos los registros. Además, de esta manera, la consulta se ejecuta más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="39303-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="39303-118">Todas las consultas de una operación UNION deben solicitar el mismo número de campos; sin embargo, no es necesario que los campos sean del mismo tamaño o tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="39303-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="39303-p104">Use alias sólo en la primera instrucción SELECT, ya que en las demás se omiten. En la cláusula ORDER BY, haga referencia a los campos por el nombre que se utilice en la primera instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="39303-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="39303-121">Puede usar una cláusula <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> o <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> en cada argumento de <EM>consulta</EM> para agrupar los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="39303-121">You can use a <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> or <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> clause in each <EM>query</EM> argument to group the returned data.</span></span></P>
> <LI>
> <P><span data-ttu-id="39303-122">Puede usar una cláusula <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> al final del último argumento de <EM>consulta</EM> para mostrar los datos devueltos en un orden especificado.</span><span class="sxs-lookup"><span data-stu-id="39303-122">You can use an <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> clause at the end of the last <EM>query</EM> argument to display the returned data in a specified order.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="39303-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39303-123">Example</span></span>

<span data-ttu-id="39303-124">En este ejemplo, se recuperan los nombres y ciudades de todos los proveedores y clientes de Brasil.</span><span class="sxs-lookup"><span data-stu-id="39303-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span>

<span data-ttu-id="39303-125">En este ejemplo, se llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="39303-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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