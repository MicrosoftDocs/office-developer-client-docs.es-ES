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
ms.openlocfilehash: 4f9593e8bf0175ee6a25bd53d886c291eed6f75c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929442"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>Operación INNER JOIN (Microsoft Access SQL)


**Se aplica a**: Access 2013, Office 2013


Combina registros de dos tablas si hay valores coincidentes en un campo común.

## <a name="syntax"></a>Sintaxis

FROM *tabla1* INNER JOIN *tabla2* ON *tabla1*. *campo1* *operadordecomparación tabla2*. *Field2*

La operación INNER JOIN consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>tabla1</em>, <em>tabla2</em></p></td>
<td><p>Nombres de las tablas en las que se combinan los registros.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Nombres de los campos que se combinan. Si no son numéricos, los campos deben tener el mismo tipo de datos y contener el mismo tipo de datos, pero no es necesario que tengan el mismo nombre.</p></td>
</tr>
<tr class="odd">
<td><p><em>operadorDeComparación</em></p></td>
<td><p>Cualquier operador de comparación relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; o &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar una operación INNER JOIN en una cláusula [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)). Este tipo de combinación es el más común. Las combinaciones internas combinan registros de dos tablas si hay valores coincidentes en un campo común a ambas.

Puede usar INNER JOIN con las tablas Departments y Employees para seleccionar todos los empleados de cada departamento En contraste, para seleccionar todos los departamentos (incluso si alguno no tiene empleados asignados) o todos los empleados (incluso si alguno no está asignado a un departamento), puede usar una operación [LEFT JOIN o RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) para crear una combinación externa.

Si se intenta combinar campos que contienen datos de tipo Memo u Objeto OLE, se produce un error.

Puede combinar dos campos numéricos de tipos similares. Por ejemplo, puede combinar campos de tipo AutoNumber y Long porque son similares. Sin embargo, no puede combinar campos de tipo Single y Double.

En el siguiente ejemplo, se muestra cómo puede combinar las tablas Categories y Products por el campo CategoryID:

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

En el ejemplo anterior, CategoryID es el campo combinado, pero no se incluye en el resultado de la consulta porque no está contenido en la instrucción [SELECT](select-statement-microsoft-access-sql.md). Para incluir el campo combinado, incluya el nombre del campo en la instrucción SELECT, en este caso, SELECT.

También puede vincular varias cláusulas ON en una instrucción JOIN mediante la siguiente sintaxis:

Seleccione *los campos* FROM *tabla1* INNER JOIN *tabla2* ON *tabla1*. *campo1* *operadorDeComparación* *tabla2*. *campo1* Y en la *tabla table1*. *Field2* *operadorDeComparación* *tabla2*. *field2*) O bien, en la *tabla table1*. *Field3* *operadorDeComparación* *tabla2*. *field3*) \];

También puede anidar instrucciones JOIN mediante la siguiente sintaxis:

Seleccione *los campos* FROM *tabla1* INNER JOIN (*tabla2* INNER JOIN \[( \] *tabla3* \[INNER JOIN \[( \] *tablax* \[INNER JOIN...) \] En *tabla3*. *Field3* *operadorDeComparación* *tablax*. *fieldx*) \] En *tabla2*. *Field2* *operadorDeComparación* *tabla3*. *field3*) EN la *tabla table1*. *campo1* *operadorDeComparación* *tabla2*. *field2*;

Una operación LEFT JOIN o RIGHT JOIN se puede anidar en una operación INNER JOIN, pero una operación INNER JOIN no se puede anidar en una operación LEFT JOIN o RIGHT JOIN.

## <a name="example"></a>Ejemplo

En este ejemplo, se crean dos combinaciones de equivalencia: una entre las tablas Order Details y Orders, y otra entre las tablas Orders y Employees. Esto es necesario porque la tabla Employees no contiene datos de ventas y la tabla Order Details no contiene datos de empleados. La consulta produce una lista de empleados y sus ventas totales.

En este ejemplo, se llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.

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
