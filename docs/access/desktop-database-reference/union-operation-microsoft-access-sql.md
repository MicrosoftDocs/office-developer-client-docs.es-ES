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
# <a name="union-operation-microsoft-access-sql"></a>Operación UNION (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crea una consulta de unión, que combina los resultados de dos o más consultas o tablas independientes.

## <a name="syntax"></a>Sintaxis

\[TABLE\] *consulta1* UNION \[ALL\] \[TABLE\] *consulta2* \[UNION \[ALL\] \[TABLE\] *consultan* \[ … \]\]

La operación UNION consta de las siguientes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>consulta1-n</em></p></td>
<td><p>Instrucción SELECT, nombre de una consulta almacenada o nombre de una tabla almacenada precedido de la palabra clave TABLE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede combinar los resultados de dos o más consultas, tablas e instrucciones SELECT en cualquier combinación, en una sola operación UNION. En el ejemplo siguiente se combina una tabla existente denominada Nuevas cuentas y una instrucción SELECT:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

De forma predeterminada, no se devuelven registros duplicados cuando se usa la operación UNION; sin embargo, puede incluir el predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para asegurarse de que se devuelven todos los registros. Además, de esta manera, la consulta se ejecuta más rápidamente.

Todas las consultas de una operación UNION deben solicitar el mismo número de campos; sin embargo, no es necesario que los campos sean del mismo tamaño o tipo de datos.

Use alias solo en la primera instrucción SELECT ya que en las demás se ignorarán. En la cláusula ORDER BY, haga referencia a los campos por su nombre en la primera instrucción SELECT.

> [!NOTE]
> - Puede usar una cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) o [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) en cada argumento de *consulta* para agrupar los datos devueltos.
> - Puede usar una cláusula [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) al final del último argumento de *consulta* para mostrar los datos devueltos en un orden especificado.

## <a name="example"></a>Ejemplo

En este ejemplo se recuperan los nombres y ciudades de todos los proveedores y los clientes de Brasil. Llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.

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
