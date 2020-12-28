---
title: Instrucción ALTER TABLE (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 07a83c16368caa6e5c05c7554300c5589a437067
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734185"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="dd787-102">Instrucción ALTER TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="dd787-102">ALTER TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="dd787-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd787-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd787-104">Modifica el diseño de una tabla después de que se ha creado con la instrucción [CREATE TABLE](create-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="dd787-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="dd787-105">El motor de base de datos de Microsoft Access no admite el uso de ALTER TABLE, ni las instrucciones de lenguaje de definición de datos (DDL), con bases de datos que no sean de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd787-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="dd787-106">En su lugar, use los métodos **Create** de DAO.</span><span class="sxs-lookup"><span data-stu-id="dd787-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd787-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd787-107">Syntax</span></span>

<span data-ttu-id="dd787-108">ALTER TABLE *tabla* {ADD {COLUMN *campo tipo*\[(*tamaño*)\] \[NOT NULL\] \[CONSTRAINT *índice*\] | ALTER COLUMN *campo tipo*\[(*tamaño*)\] | CONSTRAINT *índiceDeVariosCampos*} | DROP {COLUMN *campo* I CONSTRAINT *nombreDeÍndice*} }</span><span class="sxs-lookup"><span data-stu-id="dd787-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="dd787-109">La instrucción ALTER TABLE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dd787-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd787-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="dd787-110">Part</span></span></p></th>
<th><p><span data-ttu-id="dd787-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd787-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd787-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="dd787-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-113">Nombre de la tabla que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="dd787-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd787-114"><em>campo</em></span><span class="sxs-lookup"><span data-stu-id="dd787-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-p102">Nombre del campo que se va a agregar o eliminar en la <em>tabla</em>. O bien, nombre del campo que se va a modificar en la <em>tabla</em>.</span><span class="sxs-lookup"><span data-stu-id="dd787-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd787-117"><em>tipo</em></span><span class="sxs-lookup"><span data-stu-id="dd787-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-118">Tipo de datos del <em>campo</em>.</span><span class="sxs-lookup"><span data-stu-id="dd787-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd787-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="dd787-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-120">Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</span><span class="sxs-lookup"><span data-stu-id="dd787-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd787-121"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="dd787-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-122">El índice de <em>campo</em>.</span><span class="sxs-lookup"><span data-stu-id="dd787-122">The index for <em>field</em>.</span></span> <span data-ttu-id="dd787-123">Para obtener más información acerca de cómo construir este índice, vea la <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="dd787-123">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd787-124"><em>índiceDeVariosCampos</em></span><span class="sxs-lookup"><span data-stu-id="dd787-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-125">La definición de un índice de varios campos que se va a agregar a <em>tabla</em>.</span><span class="sxs-lookup"><span data-stu-id="dd787-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="dd787-126">Para obtener más información acerca de cómo construir este índice, vea la <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="dd787-126">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd787-127"><em>nombre_del_índice</em></span><span class="sxs-lookup"><span data-stu-id="dd787-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="dd787-128">Nombre del índice de varios campos que se eliminará.</span><span class="sxs-lookup"><span data-stu-id="dd787-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dd787-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd787-129">Remarks</span></span>

<span data-ttu-id="dd787-130">Mediante la instrucción ALTER TABLE se puede modificar una tabla existente de varias formas.</span><span class="sxs-lookup"><span data-stu-id="dd787-130">By using the ALTER TABLE statement, you can alter an existing table in several ways.</span></span> <span data-ttu-id="dd787-131">Podrá:</span><span class="sxs-lookup"><span data-stu-id="dd787-131">You can:</span></span>

- <span data-ttu-id="dd787-p106">Usar ADD COLUMN para agregar un campo nuevo a la tabla. Debe especificar el nombre del campo, el tipo de datos y (para los campos de tipo texto y binario) un tamaño opcional. Por ejemplo, la siguiente instrucción agrega un campo de texto de 25 caracteres llamado Notes a la tabla Employees:</span><span class="sxs-lookup"><span data-stu-id="dd787-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="dd787-135">También se puede definir un índice en ese campo.</span><span class="sxs-lookup"><span data-stu-id="dd787-135">You can also define an index on that field.</span></span> <span data-ttu-id="dd787-136">Para obtener más información sobre los índices de un solo campo, consulte [Cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="dd787-136">For more information about single-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="dd787-137">Si especifica NOT NULL en un campo, será obligatorio que los nuevos registros tengan datos válidos en ese campo.</span><span class="sxs-lookup"><span data-stu-id="dd787-137">If you specify NOT NULL for a field, new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="dd787-p108">Usar ALTER COLUMN para cambiar el tipo de datos de un campo existente. Debe especificar el nombre del campo, el nuevo tipo de datos y un tamaño opcional para los campos de tipo texto y binario. Por ejemplo, la siguiente instrucción cambia el tipo de datos de un campo de la tabla Employees llamado ZipCode (definido originalmente como Integer) a un campo Texto de 10 caracteres:</span><span class="sxs-lookup"><span data-stu-id="dd787-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- <span data-ttu-id="dd787-141">Use ADD CONSTRAINT para agregar un índice de varios campos.</span><span class="sxs-lookup"><span data-stu-id="dd787-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="dd787-142">Para obtener más información acerca de los índices de varios campos, vea la [Cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="dd787-142">For more information about multiple-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="dd787-p110">Usar DROP COLUMN para eliminar un campo. Sólo debe especificar el nombre del campo.</span><span class="sxs-lookup"><span data-stu-id="dd787-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

- <span data-ttu-id="dd787-p111">Usar DROP CONSTRAINT para eliminar un índice de varios campos. Sólo debe especificar el nombre del índice a continuación de la palabra reservada CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="dd787-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE] 
> - <span data-ttu-id="dd787-147">No se puede agregar o eliminar más de un campo o índice a la vez.</span><span class="sxs-lookup"><span data-stu-id="dd787-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="dd787-148">Puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para agregar un índice de un solo campo o de varios campos a un tabla y puede usar ALTER TABLE o la instrucción [DROP](drop-statement-microsoft-access-sql.md) para eliminar un índice creado con ALTER TABLE o CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="dd787-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="dd787-149">Puede usar NOT NULL en un solo campo o en una cláusula CONSTRAINT con nombre que se aplica a un solo campo o a una cláusula CONSTRAINT con nombre de varios campos.</span><span class="sxs-lookup"><span data-stu-id="dd787-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="dd787-150">Pero solo puede aplicar la restricción NOT NULL una vez a un campo.</span><span class="sxs-lookup"><span data-stu-id="dd787-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="dd787-151">Intentar aplicar esta restricción más de una vez produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="dd787-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="dd787-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd787-152">Example</span></span>

<span data-ttu-id="dd787-153">En este ejemplo, se agrega un campo Salary con el tipo de datos **Money** a la tabla Employees.</span><span class="sxs-lookup"><span data-stu-id="dd787-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="dd787-154">En este ejemplo, se cambia el tipo de datos del campo Salary de **Money** a **Char**.</span><span class="sxs-lookup"><span data-stu-id="dd787-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Modify the existing Salary field of the Employees table  
        ' by changing it to a CHAR data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="dd787-155">En este ejemplo, se quita el campo Salary de la tabla Employees.</span><span class="sxs-lookup"><span data-stu-id="dd787-155">This example removes the Salary field from the Employees table.</span></span>

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="dd787-p113">En este ejemplo, se agrega una clave externa a la tabla Orders. La clave externa se basa en el campo EmployeeID y hace referencia al campo EmployeeID de la tabla Employees. En este ejemplo, no tiene que enumerar el campo EmployeeID después de la tabla Employees en la cláusula REFERENCES porque EmployeeID es la clave principal de la tabla Employees.</span><span class="sxs-lookup"><span data-stu-id="dd787-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="dd787-159">En este ejemplo, se elimina la clave externa de la tabla Orders.</span><span class="sxs-lookup"><span data-stu-id="dd787-159">This example removes the foreign key from the Orders table.</span></span>

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
