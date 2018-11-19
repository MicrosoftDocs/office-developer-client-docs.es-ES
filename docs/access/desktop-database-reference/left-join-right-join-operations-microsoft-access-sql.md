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
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Combina registros de una tabla de origen cuando se usa en una cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).

## <a name="syntax"></a>Sintaxis

FROM *tabla1* \[ izquierda | DERECHA \] JOIN *tabla2* ON *tabla1.campo1* *operadordecomparación tabla2.campo2*

Las operaciones LEFT JOIN y RIGHT JOIN constan de los siguientes elementos:

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
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Nombres de los campos que se combinan. Los campos deben ser del mismo tipo de datos y contener la misma clase de datos, pero no es necesario que tengan el mismo nombre.</p></td>
</tr>
<tr class="odd">
<td><p><em>operadorDeComparación</em></p></td>
<td><p>Cualquier operador de comparación relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; o &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use una operación LEFT JOIN para crear una combinación externa izquierda. Estas combinaciones incluyen todos los registros de la primera (izquierda) de dos tablas, incluso si no hay valores coincidentes para los registros en la segunda tabla (derecha).

Use una operación RIGHT JOIN para crear una combinación externa derecha. Estas combinaciones incluyen todos los registros de la segunda (derecha) de dos tablas, incluso si no hay valores coincidentes para los registros de la primera tabla (izquierda).

Por ejemplo, podría usar LEFT JOIN con las tablas Departamentos (izquierda) y Empleados (derecha) para seleccionar todos los departamentos, incluidos los que no tengan empleados asignados. Para seleccionar todos los empleados, incluidos los que no estén asignados a ningún departamento, utilizaría RIGHT JOIN.

En el siguiente ejemplo, se muestra cómo puede combinar las tablas Categories y Products por el campo CategoryID. La consulta produce una lista de todas las categorías, incluidas las que no contienen ningún producto:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

En este ejemplo, CategoryID es el campo combinado, pero no está incluido en los resultados de la consulta porque no está contenido en la instrucción [SELECT](select-statement-microsoft-access-sql.md). Para incluir el campo combinado, introduzca el nombre del campo en la instrucción SELECT, en este caso, SELECT.

> [!NOTE]
> - [!NOTA] Para crear una consulta que incluya sólo los registros en los que los datos de los campos de combinación sean iguales, use una operación [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Las operaciones LEFT JOIN y RIGHT JOIN se pueden anidar en una operación INNER JOIN, pero una operación INNER JOIN no se puede anidar en una operación LEFT JOIN o RIGHT JOIN. Vea la descripción del anidamiento en el tema INNER JOIN acerca de cómo anidar unas combinaciones en otras.
> - Puede vincular varias cláusulas ON. Vea la descripción de la vinculación de cláusulas en el tema de INNER JOIN acerca de cómo llevarlo a cabo.
> - Si se intenta combinar campos que contienen datos de tipo Memo u Objeto OLE, se produce un error.

## <a name="example"></a>Ejemplo

En este ejemplo:
- Se presupone la existencia de campos de nombre de departamento y el identificador de departamento hipotéticos en una tabla empleados. Tenga en cuenta que estos campos no existen realmente en la tabla Employees (Empleados) de la base de datos Northwind (Neptuno).

- Selecciona todos los departamentos, incluidos los que no tienen empleados.

- Llama al procedimiento EnumFields, que puede encontrar en el ejemplo de la instrucción SELECT.


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
