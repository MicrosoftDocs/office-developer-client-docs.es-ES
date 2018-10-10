---
title: DELETE (instrucción de Microsoft Access SQL)
TOCTitle: DELETE Statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8a0d78350a9689af67f33262ff510d8638de40c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485074"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="04d67-102">DELETE (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="04d67-102">DELETE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="04d67-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="04d67-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="04d67-104">Crea una consulta de eliminación que elimina los registros de una o varias tablas enumeradas en la cláusula [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) que cumplen la cláusula [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="04d67-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause that satisfy the [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04d67-105">Syntax</span></span>

<span data-ttu-id="04d67-106">ELIMINAR \[ *tabla*. \* \] De *tabla* WHERE *criterios*</span><span class="sxs-lookup"><span data-stu-id="04d67-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="04d67-107">La instrucción DELETE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="04d67-107">The DELETE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04d67-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="04d67-108">Part</span></span></p></th>
<th><p><span data-ttu-id="04d67-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="04d67-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04d67-110"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="04d67-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="04d67-111">Nombre opcional de la tabla en la que se eliminarán los registros.</span><span class="sxs-lookup"><span data-stu-id="04d67-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04d67-112"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="04d67-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="04d67-113">Nombre de la tabla en la que se eliminarán los registros.</span><span class="sxs-lookup"><span data-stu-id="04d67-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04d67-114"><em>criterios</em></span><span class="sxs-lookup"><span data-stu-id="04d67-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="04d67-115">Expresión que determina qué registros se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="04d67-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="04d67-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04d67-116">Remarks</span></span>

<span data-ttu-id="04d67-117">DELETE es especialmente útil cuando se desea eliminar muchos registros.</span><span class="sxs-lookup"><span data-stu-id="04d67-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="04d67-p101">Para eliminar una tabla completa de la base de datos, puede usar el método **Execute** con la instrucción [DROP](drop-statement-microsoft-access-sql.md). Sin embargo, si elimina la tabla, se pierde la estructura. En contraste, si se usa DELETE, sólo se eliminan los datos; la estructura de la tabla y todas las propiedades de la tabla, como los atributos de campo y los índices, permanecen intactos.</span><span class="sxs-lookup"><span data-stu-id="04d67-p101">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement. If you delete the table, however, the structure is lost. In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="04d67-p102">Puede usar DELETE para eliminar registros en tablas que formen parte de una relación de uno a varios con otras tablas. Las operaciones de eliminación en cascada causan que los registros de las tablas que se encuentran en el lado varios de la relación se eliminen cuando el registro correspondiente del lado uno de la relación se elimina en la consulta. Por ejemplo, en la relación entre las tablas Clientes y Pedidos, la tabla Clientes se encuentra en el lado uno y la tabla Pedidos se encuentra en el lado varios de la relación. Si se elimina un registro de Clientes, se eliminan los registros correspondientes de Pedidos si se ha especificado la opción de eliminación en cascada.</span><span class="sxs-lookup"><span data-stu-id="04d67-p102">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables. Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query. For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship. Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="04d67-p103">Una consulta de eliminación elimina registros completos, no sólo los datos de campos específicos. Si desea eliminar valores en un campo específico, cree una consulta de actualización que cambie los valores a **Null**.</span><span class="sxs-lookup"><span data-stu-id="04d67-p103">A delete query deletes entire records, not just data in specific fields. If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="04d67-p104">Después de eliminar registros con una consulta de eliminación, no se puede deshacer la operación. Si desea saber qué registros se han eliminado, examine primero los resultados de una consulta de selección que utilice los mismos criterios y, después, ejecute la consulta de eliminación.</span><span class="sxs-lookup"><span data-stu-id="04d67-p104">After you remove records using a delete query, you cannot undo the operation. If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="04d67-p105">Guarde copias de seguridad de los datos en todo momento. Si elimina los registros incorrectos, podrá recuperarlos a partir de las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="04d67-p105">Maintain backup copies of your data at all times. If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="04d67-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04d67-131">Example</span></span>

<span data-ttu-id="04d67-p106">En este ejemplo, se eliminan todos los registros de empleados cuyo título sea Trainee (Aprendiz). Si la cláusula FROM sólo incluye una tabla, no es necesario enumerar el nombre de la tabla en la instrucción DELETE.

</span><span class="sxs-lookup"><span data-stu-id="04d67-p106">This example deletes all records for employees whose title is Trainee. When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

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