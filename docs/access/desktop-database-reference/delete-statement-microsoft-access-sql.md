---
title: Instrucción DELETE (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a4ef478e74f9851012d6f749e64b4ddb34f3a959
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294046"
---
# <a name="delete-statement-microsoft-access-sql"></a>Instrucción DELETE (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crea una consulta de eliminación que elimina los registros de una o varias tablas enumeradas en la cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) que cumplen la cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).

## <a name="syntax"></a>Sintaxis

DELETE \[*tabla*.\* \] FROM *tabla* WHERE *criterios*

La instrucción DELETE consta de las siguientes partes:

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
<td><p><em>tabla</em></p></td>
<td><p>Nombre opcional de la tabla de la que se eliminan los registros.</p></td>
</tr>
<tr class="even">
<td><p><em>tabla</em></p></td>
<td><p>Nombre de la tabla de la que se eliminan los registros.</p></td>
</tr>
<tr class="odd">
<td><p><em>criterios</em></p></td>
<td><p>Expresión que determina qué registros se van a eliminar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

DELETE resulta especialmente útil para eliminar muchos registros.

Para eliminar una tabla completa de la base de datos, puede usar el método **Execute** con la instrucción [DROP](drop-statement-microsoft-access-sql.md). Sin embargo, si elimina la tabla, se pierde la estructura. En contraste, si se usa DELETE, sólo se eliminan los datos; la estructura de la tabla y todas las propiedades de la tabla, como los atributos de campo y los índices, permanecen intactos.

Puede usar DELETE para eliminar registros en tablas que formen parte de una relación de uno a varios con otras tablas. Las operaciones de eliminación en cascada causan que los registros de las tablas que se encuentran en el lado varios de la relación se eliminen cuando el registro correspondiente del lado uno de la relación se elimina en la consulta. Por ejemplo, en la relación entre las tablas Clientes y Pedidos, la tabla Clientes se encuentra en el lado uno y la tabla Pedidos se encuentra en el lado varios de la relación. Si se elimina un registro de Clientes, se eliminan los registros correspondientes de Pedidos si se ha especificado la opción de eliminación en cascada.

Una consulta de eliminación elimina registros completos, no sólo los datos de campos específicos. Si desea eliminar valores en un campo específico, cree una consulta de actualización que cambie los valores a **Null**.

> [!IMPORTANT]
> - Después de eliminar registros con una consulta de eliminación, no se puede deshacer la operación. Si desea saber qué registros se han eliminado, examine primero los resultados de una consulta de selección que utilice los mismos criterios y, después, ejecute la consulta de eliminación.
> - Mantenga copias de seguridad de los datos en todo momento. Si elimina los registros incorrectos, podrá recuperarlos de las copias de seguridad.

## <a name="example"></a>Ejemplo

En este ejemplo, se eliminan todos los registros de empleados cuyo título sea Trainee (Aprendiz). Si la cláusula FROM sólo incluye una tabla, no es necesario enumerar el nombre de la tabla en la instrucción DELETE.

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```
