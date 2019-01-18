---
title: SELECCIONE ESTA OPCIÓN. EN la instrucción (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705501"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECCIONE ESTA OPCIÓN. EN la instrucción (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Crea una consulta de creación de tabla.

## <a name="syntax"></a>Sintaxis

SELECT *campo1*\[, *field2*\[,... \] \] INTO *nuevaTabla* \[IN *basededatosexterna* \] de *origen*

La instrucción SELECT…INTO consta de los siguientes elementos:

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
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Nombre de los campos que se copiarán a la nueva tabla.</p></td>
</tr>
<tr class="even">
<td><p><em>nuevaTabla</em></p></td>
<td><p>Nombre de la tabla que se va a crear. Debe seguir las convenciones de nomenclatura estándar. Si <em>nuevaTabla</em> es la misma que el nombre de una tabla existente, se produce un error capturable.</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>La ruta de acceso a una base de datos externa. Para obtener una descripción de la ruta de acceso, consulte la cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Nombre de la tabla existente en la que se seleccionan los registros. Puede tratarse de una o varias tablas, o una consulta.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar consultas de creación de tabla para archivar registros, crear copias de seguridad de las tablas o realizar copias para exportarlas a otra base de datos o usarlas como base para informes que muestren datos de un período de tiempo determinado. Por ejemplo, puede generar un informe de ventas mensuales por región ejecutando la misma consulta de creación de tabla cada mes.

> [!NOTE]
> - Puede que desee definir una clave principal para la nueva tabla. Al crear la tabla, los campos de la nueva tabla heredan el tipo de datos y tamaño de campo de cada campo de las tablas base de la consulta, pero no se transfiere ninguna otra propiedad de campo o tabla.
> - Para agregar datos a una tabla existente, use la instrucción [INSERT INTO](insert-into-statement-microsoft-access-sql.md) en lugar de crear una consulta de datos anexados.
> - Para averiguar qué registros se seleccionarán antes de ejecutar la consulta de creación de tabla, examine primero los resultados de una instrucción [SELECT](select-statement-microsoft-access-sql.md) que use los mismos criterios de selección.



## <a name="example"></a>Ejemplo

En este ejemplo, se seleccionan todos los registros de la tabla Employees y se copian en una nueva tabla llamada Emp Backup.

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
