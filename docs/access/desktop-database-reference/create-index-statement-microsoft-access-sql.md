---
title: CREATE INDEX (instrucción de Microsoft Access SQL)
TOCTitle: CREATE INDEX Statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab501348d19ad8577bf1a55a3f37c6c3923381b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483718"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="026f6-102">CREATE INDEX (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="026f6-102">CREATE INDEX Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="026f6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="026f6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="026f6-104">Crea un índice nuevo en una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="026f6-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="026f6-p101">[!NOTA] Para las bases de datos que no son del motor de base de datos de Microsoft Access, el motor de base de datos de Microsoft Access no admite el uso de CREATE INDEX (excepto para crear un pseudoíndice en una tabla vinculada ODBC) ni las instrucciones de lenguaje de definición de datos (DDL). En su lugar, use los métodos Create de DAO. Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="026f6-p101">For non-Microsoft Access atabse engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements. Use the DAO Create methods instead. For more information see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="026f6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="026f6-108">Syntax</span></span>

<span data-ttu-id="026f6-109">CREAR \[ UNIQUE \] INDEX *índice* ON *tabla* (*campo* \[ASC | DESC\]\[, *campo* \[ASC | DESC\],... \]) \[WITH {principal | DISALLOW NULL | IGNORE NULL}\]</span><span class="sxs-lookup"><span data-stu-id="026f6-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span></span>

<span data-ttu-id="026f6-110">La instrucción CREATE INDEX consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="026f6-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="026f6-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="026f6-111">Part</span></span></p></th>
<th><p><span data-ttu-id="026f6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="026f6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="026f6-113"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="026f6-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="026f6-114">Nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="026f6-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="026f6-115"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="026f6-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="026f6-116">Nombre de la tabla existente que contendrá el índice.</span><span class="sxs-lookup"><span data-stu-id="026f6-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="026f6-117"><em>campo</em></span><span class="sxs-lookup"><span data-stu-id="026f6-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="026f6-p102">Nombre del campo o los campos que se van a indizar. Para crear un índice de campo único, enumere el nombre del campo entre paréntesis a continuación del nombre de la tabla. Para crear un índice de varios campos, enumere el nombre de cada campo que se incluirá en el índice. Para crear índices descendentes, use la palabra reservada DESC; de lo contrario, se supone que el orden de los índices es ascendente.</span><span class="sxs-lookup"><span data-stu-id="026f6-p102">The name of the field or fields to be indexed. To create a single-field index, list the field name in parentheses following the table name. To create a multiple-field index, list the name of each field to be included in the index. To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="026f6-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="026f6-122">Remarks</span></span>

<span data-ttu-id="026f6-123">Para prohibir valores duplicados en el campo o campos indizados de diferentes registros, use la palabra reservada UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="026f6-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="026f6-p103">En la cláusula WITH opcional, puede aplicar reglas de validación de datos. Se puede:</span><span class="sxs-lookup"><span data-stu-id="026f6-p103">In the optional WITH clause you can enforce data validation rules. You can:</span></span>

- <span data-ttu-id="026f6-126">Prohibir entradas Null en el campo o campos indizados de nuevos registros mediante la opción DISALLOW NULL.</span><span class="sxs-lookup"><span data-stu-id="026f6-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="026f6-127">Impedir que los registros con valores **Null** en el campo o campos indizados se incluyan en el índice mediante la opción IGNORE NULL.</span><span class="sxs-lookup"><span data-stu-id="026f6-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="026f6-p104">Designar el campo o campos indizados como la clave principal mediante la palabra reservada PRIMARY. Esto implica que la clave es única, por lo que se puede omitir la palabra reservada UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="026f6-p104">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word. This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="026f6-p105">Puede usar CREATE INDEX para crear un pseudoíndice en una tabla vinculada de un origen de datos ODBC, por ejemplo Microsoft® SQL Server, que no tenga un índice. No es necesario permiso o acceso al servidor remoto para crear un pseudoíndice y éste no es conocido por la base de datos remota ni le afecta. Se usa la misma sintaxis para las tablas vinculadas y nativas. Puede ser especialmente útil la creación de un pseudoíndice en una tabla que normalmente será de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="026f6-p105">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft® SQL Server™, that does not already have an index. You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index. You use the same syntax for both linked and native tables. Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="026f6-134">También puede usar la instrucción [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para agregar un índice de campo único o de varios campos a una tabla y puede usar la instrucción ALTER TABLE o la instrucción [DROP](drop-statement-microsoft-access-sql.md) para eliminar un índice creado con ALTER TABLE o CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="026f6-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="026f6-135">[!NOTA] No use la palabra reservada PRIMARY al crear un nuevo índice en una tabla que ya tenga una clave principal; si lo hace, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="026f6-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="026f6-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="026f6-136">Example</span></span>

<span data-ttu-id="026f6-137">En este ejemplo, se crea un índice formado por los campos Home Phone (Teléfono particular) y Extension (Extensión) de la tabla Employees (Empleados).</span><span class="sxs-lookup"><span data-stu-id="026f6-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="026f6-p106">En este ejemplo, se crea un índice en la tabla Customers (Clientes) con el campo CustomerID (IDCliente). No puede haber dos registros que tengan los mismos datos en el campo CustomerID y no se permiten valores Null.</span><span class="sxs-lookup"><span data-stu-id="026f6-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
