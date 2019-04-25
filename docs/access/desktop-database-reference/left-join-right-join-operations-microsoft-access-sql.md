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
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>Operaciones LEFT JOIN y RIGHT JOIN (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Combina registros de una tabla de origen cuando se usa en una cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).

## <a name="syntax"></a>Sintaxis

FROM *tabla1* \[ LEFT | RIGHT \] JOIN *tabla2* ON *tabla1.campo1* *operadorDeComparación tabla2.campo2*

Las operaciones LEFT JOIN y RIGHT JOIN constan de las siguientes partes:

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
<td><p><em>tabla1</em>, <em>tabla2</em></p></td>
<td><p>Nombres de las tablas cuyos registros se combinan.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Nombres de los campos que se combinan. Estos campos deben ser del mismo tipo de datos y contener la misma clase de datos, pero no tienen que tener el mismo nombre.</p></td>
</tr>
<tr class="odd">
<td><p><em>opcomp</em></p></td>
<td><p>Cualquier operador de comparación relacional: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; o &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use una operación LEFT JOIN para crear una combinación externa izquierda. Estas combinaciones incluyen todos los registros de la primera (izquierda) de dos tablas, incluso si no hay valores coincidentes para los registros en la segunda tabla (derecha).

Use una operación RIGHT JOIN para crear una combinación externa derecha. Estas combinaciones incluyen todos los registros de la segunda (derecha) de dos tablas, incluso si no hay valores coincidentes para los registros de la primera tabla (izquierda).

Por ejemplo, puede usar LEFT JOIN con las tablas Departamentos (izquierda) y Empleados (derecha) para seleccionar todos los departamentos, incluidos aquellos que no tengan ningún empleado asignado. Para seleccionar todos los empleados, incluidos aquellos que no estén asignados a un departamento, use RIGHT JOIN.

En el ejemplo siguiente se muestra cómo combinar las tablas Categorías y Productos en el campo CategoryID. La consulta genera una lista de todas las categorías, incluidas aquellas que no contienen ningún producto:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

En este ejemplo, CategoryID es el campo combinado, pero no está incluido en los resultados de la consulta porque no está contenido en la instrucción [SELECT](select-statement-microsoft-access-sql.md). Para incluir el campo combinado, escriba el nombre de campo en la instrucción SELECT (en este caso, Categories.CategoryID).

> [!NOTE]
> - Para crear una consulta que incluya sólo los registros en los que los datos de los campos de combinación sean iguales, use una operación [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Las operaciones LEFT JOIN o RIGHT JOIN se pueden anidar dentro de una operación INNER JOIN, pero una operación INNER JOIN no se puede anidar dentro de una operación LEFT JOIN o RIGHT JOIN. Vea la discusión sobre anidamiento en el tema INNER JOIN para conocer cómo se anidan las combinaciones dentro de otras combinaciones.
> - Se pueden vincular varias cláusulas ON. Vea la discusión sobre la vinculación de cláusulas en el tema INNER JOIN para conocer el procedimiento.
> - Si intenta combinar campos que contienen datos Memo u Objeto OLE, se produce un error.

## <a name="example"></a>Ejemplo

Este ejemplo:
- Supone la existencia de los campos hipotéticos Department Name (Nombre del departamento) y Department ID (Id. de departamento) en una tabla Employees (Empleados). Tenga en cuenta que estos campos no existen realmente en la tabla de empleados de la base de datos de Northwind.

- Selecciona todos los departamentos, incluidos los que no tienen empleados.

- Llama al procedimiento EnumFields, que se incluye en el ejemplo de la instrucción SELECT.


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
