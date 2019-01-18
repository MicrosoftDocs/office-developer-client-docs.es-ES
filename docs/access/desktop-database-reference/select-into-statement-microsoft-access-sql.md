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
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="07456-102">SELECCIONE ESTA OPCIÓN. EN la instrucción (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="07456-102">SELECT.INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="07456-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07456-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07456-104">Crea una consulta de creación de tabla.</span><span class="sxs-lookup"><span data-stu-id="07456-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="07456-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07456-105">Syntax</span></span>

<span data-ttu-id="07456-106">SELECT *campo1*\[, *field2*\[,... \] \] INTO *nuevaTabla* \[IN *basededatosexterna* \] de *origen*</span><span class="sxs-lookup"><span data-stu-id="07456-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="07456-107">La instrucción SELECT…INTO consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="07456-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07456-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="07456-108">Part</span></span></p></th>
<th><p><span data-ttu-id="07456-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="07456-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07456-110"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="07456-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="07456-111">Nombre de los campos que se copiarán a la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="07456-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07456-112"><em>nuevaTabla</em></span><span class="sxs-lookup"><span data-stu-id="07456-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="07456-p101">Nombre de la tabla que se va a crear. Debe seguir las convenciones de nomenclatura estándar. Si <em>nuevaTabla</em> es la misma que el nombre de una tabla existente, se produce un error capturable.</span><span class="sxs-lookup"><span data-stu-id="07456-p101">The name of the table to be created. It must conform to standard naming conventions. If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07456-116"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="07456-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="07456-p102">La ruta de acceso a una base de datos externa. Para obtener una descripción de la ruta de acceso, consulte la cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </span><span class="sxs-lookup"><span data-stu-id="07456-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07456-119"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="07456-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="07456-p103">Nombre de la tabla existente en la que se seleccionan los registros. Puede tratarse de una o varias tablas, o una consulta.</span><span class="sxs-lookup"><span data-stu-id="07456-p103">The name of the existing table from which records are selected. This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="07456-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07456-122">Remarks</span></span>

<span data-ttu-id="07456-p104">Puede usar consultas de creación de tabla para archivar registros, crear copias de seguridad de las tablas o realizar copias para exportarlas a otra base de datos o usarlas como base para informes que muestren datos de un período de tiempo determinado. Por ejemplo, puede generar un informe de ventas mensuales por región ejecutando la misma consulta de creación de tabla cada mes.</span><span class="sxs-lookup"><span data-stu-id="07456-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="07456-p105">Puede que desee definir una clave principal para la nueva tabla. Al crear la tabla, los campos de la nueva tabla heredan el tipo de datos y tamaño de campo de cada campo de las tablas base de la consulta, pero no se transfiere ninguna otra propiedad de campo o tabla.</span><span class="sxs-lookup"><span data-stu-id="07456-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="07456-127">Para agregar datos a una tabla existente, use la instrucción [INSERT INTO](insert-into-statement-microsoft-access-sql.md) en lugar de crear una consulta de datos anexados.</span><span class="sxs-lookup"><span data-stu-id="07456-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="07456-128">Para averiguar qué registros se seleccionarán antes de ejecutar la consulta de creación de tabla, examine primero los resultados de una instrucción [SELECT](select-statement-microsoft-access-sql.md) que use los mismos criterios de selección.</span><span class="sxs-lookup"><span data-stu-id="07456-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="07456-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07456-129">Example</span></span>

<span data-ttu-id="07456-130">En este ejemplo, se seleccionan todos los registros de la tabla Employees y se copian en una nueva tabla llamada Emp Backup.</span><span class="sxs-lookup"><span data-stu-id="07456-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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
