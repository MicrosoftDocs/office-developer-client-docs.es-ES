---
title: Instrucción DROP (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f08da4f5a5b8dd0bd2604598cf72ab15d994c529
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880946"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="7e222-102">Instrucción DROP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7e222-102">DROP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7e222-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e222-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e222-104">Elimina una tabla, procedimiento o vista existente en una base de datos o elimina un índice existente en una tabla.</span><span class="sxs-lookup"><span data-stu-id="7e222-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="7e222-p101">[!NOTA] El motor de base de datos de Microsoft Access no admite el uso de DROP, ni las instrucciones DDL, con bases de datos que no sean del motor de base de datos de Microsoft Access. En su lugar, use el método **Delete** de DAO.</span><span class="sxs-lookup"><span data-stu-id="7e222-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e222-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e222-107">Syntax</span></span>

<span data-ttu-id="7e222-108">DROP {TABLE *tabla* | INDEX *índice* ON *tabla* | PROCEDURE *procedimiento* | VIEW *vista*}</span><span class="sxs-lookup"><span data-stu-id="7e222-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="7e222-109">La instrucción DROP consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7e222-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e222-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e222-110">Part</span></span></p></th>
<th><p><span data-ttu-id="7e222-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e222-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e222-112"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="7e222-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="7e222-113">Nombre de la tabla que se va a eliminar o en la que se va a eliminar un índice.</span><span class="sxs-lookup"><span data-stu-id="7e222-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e222-114"><em>procedimiento</em></span><span class="sxs-lookup"><span data-stu-id="7e222-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="7e222-115">Nombre del procedimiento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="7e222-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e222-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="7e222-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="7e222-117">Nombre de la vista que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="7e222-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e222-118"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="7e222-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="7e222-119">Nombre del índice que se va a eliminar en la <em>tabla.</em></span><span class="sxs-lookup"><span data-stu-id="7e222-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7e222-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e222-120">Remarks</span></span>

<span data-ttu-id="7e222-121">Debe cerrar la tabla para poder eliminarla o eliminar un índice en ella.</span><span class="sxs-lookup"><span data-stu-id="7e222-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="7e222-122">También puede usar [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para eliminar un índice en la tabla.</span><span class="sxs-lookup"><span data-stu-id="7e222-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="7e222-p102">Puede usar [CREATE TABLE](create-table-statement-microsoft-access-sql.md)para crear una tabla y [CREATE INDEX](create-index-statement-microsoft-access-sql.md) o ALTER TABLE para crear un índice. Para modificar una tabla, use ALTER TABLE.</span><span class="sxs-lookup"><span data-stu-id="7e222-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="7e222-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e222-125">Example</span></span>

<span data-ttu-id="7e222-126">En el siguiente ejemplo, se supone la existencia de un índice hipotético NewIndex en la tabla Employees de la base de datos Neptuno.</span><span class="sxs-lookup"><span data-stu-id="7e222-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="7e222-127">En este ejemplo, se elimina el índice MyIndex de la tabla Employees.</span><span class="sxs-lookup"><span data-stu-id="7e222-127">This example deletes the index MyIndex from the Employees table.</span></span>

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="7e222-128">En este ejemplo se elimina la tabla Employees de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7e222-128">This example deletes the Employees table from the database.</span></span>

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
