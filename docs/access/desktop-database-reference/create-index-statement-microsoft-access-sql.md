---
title: Instrucción CREATE INDEX (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 90dbaae5ab803173493e5348b77b124d83f8f9d6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873036"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="45cf2-102">Instrucción CREATE INDEX (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="45cf2-102">CREATE INDEX statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="45cf2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45cf2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45cf2-104">Crea un índice nuevo en una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="45cf2-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="45cf2-105">Para las bases de datos del motor de base de datos de no sean de Microsoft Access, el motor de base de datos de Microsoft Access no admite el uso de CREATE INDEX (excepto para crear un pseudoíndice en una tabla vinculada ODBC) o cualquiera de las instrucciones de lenguaje (DDL) de definición de datos.</span><span class="sxs-lookup"><span data-stu-id="45cf2-105">For non-Microsoft Access database engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="45cf2-106">Utilice en su lugar los métodos **Create de DAO** .</span><span class="sxs-lookup"><span data-stu-id="45cf2-106">Use the **DAO Create** methods instead.</span></span> <span data-ttu-id="45cf2-107">Si desea más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="45cf2-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cf2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45cf2-108">Syntax</span></span>

<span data-ttu-id="45cf2-109">CREAR \[ UNIQUE \] INDEX *índice* ON *tabla* (*campo* \[ASC | DESC\]\[, *campo* \[ASC | DESC\],... \]) \[WITH {principal | DISALLOW NULL | IGNORE NULL}\]</span><span class="sxs-lookup"><span data-stu-id="45cf2-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span></span>

<span data-ttu-id="45cf2-110">La instrucción CREATE INDEX consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45cf2-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45cf2-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="45cf2-111">Part</span></span></p></th>
<th><p><span data-ttu-id="45cf2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="45cf2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45cf2-113"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="45cf2-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="45cf2-114">Nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="45cf2-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45cf2-115"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="45cf2-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="45cf2-116">Nombre de la tabla existente que contendrá el índice.</span><span class="sxs-lookup"><span data-stu-id="45cf2-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45cf2-117"><em>campo</em></span><span class="sxs-lookup"><span data-stu-id="45cf2-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="45cf2-p102">Nombre del campo o los campos que se van a indizar. Para crear un índice de campo único, enumere el nombre del campo entre paréntesis a continuación del nombre de la tabla. Para crear un índice de varios campos, enumere el nombre de cada campo que se incluirá en el índice. Para crear índices descendentes, use la palabra reservada DESC; de lo contrario, se supone que el orden de los índices es ascendente.</span><span class="sxs-lookup"><span data-stu-id="45cf2-p102">The name of the field or fields to be indexed. To create a single-field index, list the field name in parentheses following the table name. To create a multiple-field index, list the name of each field to be included in the index. To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="45cf2-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45cf2-122">Remarks</span></span>

<span data-ttu-id="45cf2-123">Para prohibir valores duplicados en el campo o campos indizados de diferentes registros, use la palabra reservada UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="45cf2-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="45cf2-124">En la cláusula opcional WITH, puede aplicar las reglas de validación de datos.</span><span class="sxs-lookup"><span data-stu-id="45cf2-124">In the optional WITH clause, you can enforce data validation rules.</span></span> <span data-ttu-id="45cf2-125">Se puede:</span><span class="sxs-lookup"><span data-stu-id="45cf2-125">You can:</span></span>

- <span data-ttu-id="45cf2-126">Prohibir entradas Null en el campo o campos indizados de nuevos registros mediante la opción DISALLOW NULL.</span><span class="sxs-lookup"><span data-stu-id="45cf2-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="45cf2-127">Impedir que los registros con valores **Null** en el campo o campos indizados se incluyan en el índice mediante la opción IGNORE NULL.</span><span class="sxs-lookup"><span data-stu-id="45cf2-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="45cf2-p104">Designar el campo o campos indizados como la clave principal mediante la palabra reservada PRIMARY. Esto implica que la clave es única, por lo que se puede omitir la palabra reservada UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="45cf2-p104">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word. This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="45cf2-130">Puede utilizar CREATE INDEX para crear un pseudoíndice en una tabla vinculada en un origen de datos ODBC, como Microsoft SQL Server, que ya no tiene un índice.</span><span class="sxs-lookup"><span data-stu-id="45cf2-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft SQL Server, that does not already have an index.</span></span> <span data-ttu-id="45cf2-131">No es necesario permiso o acceso al servidor remoto para crear un pseudoíndice y éste no es conocido por la base de datos remota ni le afecta.</span><span class="sxs-lookup"><span data-stu-id="45cf2-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="45cf2-132">Se usa la misma sintaxis para las tablas vinculadas y nativas.</span><span class="sxs-lookup"><span data-stu-id="45cf2-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="45cf2-133">Puede ser especialmente útil la creación de un pseudoíndice en una tabla que normalmente será de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="45cf2-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="45cf2-134">También puede usar la instrucción [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para agregar un índice de campo único o de varios campos a una tabla y puede usar la instrucción ALTER TABLE o la instrucción [DROP](drop-statement-microsoft-access-sql.md) para eliminar un índice creado con ALTER TABLE o CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="45cf2-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="45cf2-135">[!NOTA] No use la palabra reservada PRIMARY al crear un nuevo índice en una tabla que ya tenga una clave principal; si lo hace, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="45cf2-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="45cf2-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45cf2-136">Example</span></span>

<span data-ttu-id="45cf2-137">En este ejemplo, se crea un índice formado por los campos Home Phone (Teléfono particular) y Extension (Extensión) de la tabla Employees (Empleados).</span><span class="sxs-lookup"><span data-stu-id="45cf2-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

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

<span data-ttu-id="45cf2-p106">En este ejemplo, se crea un índice en la tabla Customers (Clientes) con el campo CustomerID (IDCliente). No puede haber dos registros que tengan los mismos datos en el campo CustomerID y no se permiten valores Null.</span><span class="sxs-lookup"><span data-stu-id="45cf2-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

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
