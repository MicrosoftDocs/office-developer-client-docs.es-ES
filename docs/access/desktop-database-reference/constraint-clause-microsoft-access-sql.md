---
title: Cláusula CONSTRAINT (Microsoft Access SQL)
TOCTitle: CONSTRAINT Clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7b26033c8026591c87e4d0f9e077380862e39f16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483569"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="8b879-102">Cláusula CONSTRAINT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8b879-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="8b879-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b879-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8b879-104">Una restricción es similar a un índice, aunque se puede usar para establecer una relación con otra tabla.</span><span class="sxs-lookup"><span data-stu-id="8b879-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="8b879-p101">La cláusula CONSTRAINT se usa en las instrucciones [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) y [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para crear o eliminar restricciones. Hay dos tipos de cláusulas CONSTRAINT: uno para crear una restricción en un único campo y otro para crear una restricción en varios campos.</span><span class="sxs-lookup"><span data-stu-id="8b879-p101">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints. There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>


> [!NOTE]
> <span data-ttu-id="8b879-p102">[!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CONSTRAINT, ni las instrucciones de lenguaje de definición de datos (DDL), con bases de datos que no sean del motor de base de datos de Microsoft Access. En su lugar, use los métodos Create de DAO.</span><span class="sxs-lookup"><span data-stu-id="8b879-p102">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases. Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b879-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b879-109">Syntax</span></span>

<span data-ttu-id="8b879-110">Restricción de un único campo:</span><span class="sxs-lookup"><span data-stu-id="8b879-110">Single-field constraint:</span></span>

<span data-ttu-id="8b879-111">CONSTRAINT *nombre* {PRIMARY KEY | ÚNICO | NOT NULL | REFERENCES *tablaexterna* \[(*campoexterno1, campoexterno2*)\] \[ON UPDATE CASCADE | ESTABLECER como NULL\] \[ON DELETE CASCADE | ESTABLECER como NULL\]}</span><span class="sxs-lookup"><span data-stu-id="8b879-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="8b879-112">Restricción de varios campos:</span><span class="sxs-lookup"><span data-stu-id="8b879-112">Multiple-field constraint:</span></span>

<span data-ttu-id="8b879-113">CONSTRAINT *nombre* {PRIMARY KEY (*principal1*\[, *principal2* \[,... \]\]) | ÚNICO (*único1*\[, *único2* \[,... \]\]) | NOT NULL (*noNull1*\[, *noNull2* \[,... \]\]) | CLAVE externa \[sin índice\] (*referencia1*\[, *referencia2* \[,... \] \]) REFERENCES *tablaexterna* \[(*campoexterno1* \[, *campoexterno2* \[,... \] \])\] \[ON UPDATE CASCADE | ESTABLECER como NULL\] \[ON DELETE CASCADE | ESTABLECER como NULL\]}</span><span class="sxs-lookup"><span data-stu-id="8b879-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="8b879-114">La cláusula CONSTRAINT consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8b879-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b879-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b879-115">Part</span></span></p></th>
<th><p><span data-ttu-id="8b879-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b879-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b879-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="8b879-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-118">Nombre de la restricción que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="8b879-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b879-119"><em>principal1</em>, <em>principal2</em></span><span class="sxs-lookup"><span data-stu-id="8b879-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-120">Nombre del campo o campos que se designarán como clave principal.</span><span class="sxs-lookup"><span data-stu-id="8b879-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b879-121"><em>único1</em>, <em>único2</em></span><span class="sxs-lookup"><span data-stu-id="8b879-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-122">Nombre del campo o campos que se designarán como clave única.</span><span class="sxs-lookup"><span data-stu-id="8b879-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b879-123"><em>noNull1, noNull2</em></span><span class="sxs-lookup"><span data-stu-id="8b879-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-124">Nombre del campo o campos restringidos a valores distintos de Null.</span><span class="sxs-lookup"><span data-stu-id="8b879-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b879-125"><em>referencia1</em>, <em>referencia2</em></span><span class="sxs-lookup"><span data-stu-id="8b879-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-126">Nombre del campo o campos de clave externa que hacen referencia a campos de otra tabla.</span><span class="sxs-lookup"><span data-stu-id="8b879-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b879-127"><em>tablaExterna</em></span><span class="sxs-lookup"><span data-stu-id="8b879-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-128">Nombre de la tabla externa que contiene el campo o los campos especificados en <em>campoExterno</em>.</span><span class="sxs-lookup"><span data-stu-id="8b879-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b879-129"><em>campoExterno1</em>, <em>campoExterno2</em></span><span class="sxs-lookup"><span data-stu-id="8b879-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="8b879-p103">Nombre del campo o los campos de <em>tablaExterna</em> especificados en <em>referencia1</em>, <em>referencia2</em>. Esta cláusula se puede omitir si el campo al que se hace referencia es la clave principal de <em>tablaExterna</em>.</span><span class="sxs-lookup"><span data-stu-id="8b879-p103">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>. You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8b879-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b879-132">Remarks</span></span>

<span data-ttu-id="8b879-133">La sintaxis de una restricción de campo único se usa en la cláusula de definición de campos de una instrucción ALTER TABLE o CREATE TABLE que sigue inmediatamente a la especificación del tipo de datos del campo.</span><span class="sxs-lookup"><span data-stu-id="8b879-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="8b879-134">La sintaxis de una restricción de varios campos se usa cuando se utiliza la palabra reservada CONSTRAINT fuera de una cláusula de definición de campos en una instrucción ALTER TABLE o CREATE TABLE.</span><span class="sxs-lookup"><span data-stu-id="8b879-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="8b879-135">Mediante CONSTRAINT, puede designar un campo como uno de los siguientes tipos de restricciones:</span><span class="sxs-lookup"><span data-stu-id="8b879-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="8b879-p104">Puede usar la palabra reservada UNIQUE para designar un campo como una clave única. Esto significa que no puede haber dos registros en la tabla que tengan el mismo valor en este campo. Puede restringir cualquier campo o lista de campos como único. Si se designa una restricción de varios campos como una clave única, los valores combinados de todos los campos del índice deben ser únicos, incluso si dos o más registros tienen el mismo valor en uno solo de los campos.</span><span class="sxs-lookup"><span data-stu-id="8b879-p104">You can use the UNIQUE reserved word to designate a field as a unique key. This means that no two records in the table can have the same value in this field. You can constrain any field or list of fields as unique. If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="8b879-p105">Puede usar las palabras reservadas PRIMARY KEY para designar un campo o conjunto de campos de una tabla como clave principal. Todos los valores de la clave principal deben ser únicos y distintos de **Null**, y sólo puede haber una clave principal para una tabla.</span><span class="sxs-lookup"><span data-stu-id="8b879-p105">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key. All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="8b879-142">[!NOTA] No establezca una restricción PRIMARY KEY en una tabla que ya tenga una clave principal; si lo hace, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8b879-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="8b879-p106">Puede usar las palabras reservadas FOREIGN KEY para designar un campo como una clave externa. Si la clave principal de la tabla externa consta de varios campos, debe usar una definición de restricción de varios campos en la que se enumeren todos los campos de referencia, el nombre de la tabla externa y los nombres de los campos a los que se hace referencia en la tabla externa en el mismo orden en que se enumeran los campos que tienen la referencia. Si el campo o los campos a los que se hace referencia son la clave principal de la tabla externa, no es necesario especificar los campos a los que se hace referencia. De forma predeterminada, el motor de base de datos se comporta como si la clave principal de la tabla externa fueran los campos a los que se hace referencia. Las restricciones de clave externa definen acciones específicas que se deben realizar cuando se cambia un valor de clave principal correspondiente:</span><span class="sxs-lookup"><span data-stu-id="8b879-p106">You can use the FOREIGN KEY reserved words to designate a field as a foreign key. If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed. If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields. By default the database engine behaves as if the foreign table's primary key is the referenced fields. Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="8b879-p107">Puede especificar acciones que se deben llevar a cabo en la tabla externa en función de una acción correspondiente realizada en una clave principal de la tabla en la que se define CONSTRAINT. Por ejemplo, considere la siguiente definición para la tabla Customers:</span><span class="sxs-lookup"><span data-stu-id="8b879-p107">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined. For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="8b879-150">Considere la siguiente definición de la tabla Orders, que define una relación de clave externa que hace referencia a la clave principal de la tabla Customers:</span><span class="sxs-lookup"><span data-stu-id="8b879-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="8b879-p108">Las cláusulas ON UPDATE CASCADE y ON DELETE CASCADE están definidas en la clave externa. La cláusula ON UPDATE CASCADE significa que si se actualiza el identificador de un cliente (CustId) en la tabla Customers, la actualización se propagará en cascada en la tabla Orders. Cada pedido que contenga un valor de identificador de cliente correspondiente se actualizará automáticamente con el nuevo valor. La cláusula ON DELETE CASCADE significa que si se elimina un cliente de la tabla Customers, todas las filas de la tabla Orders que contengan el mismo valor de identificador de cliente también se eliminarán. Considere la siguiente definición diferente de la tabla Orders, en la que se usa la acción SET NULL en lugar de la acción CASCADE:</span><span class="sxs-lookup"><span data-stu-id="8b879-p108">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key. The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table. Each order containing a corresponding customer identifier value will be updated automatically with the new value. The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted. Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="8b879-p109">La cláusula ON UPDATE SET NULL significa que si se actualiza el identificador de un cliente (CustId) en la tabla Customers, los valores de clave externa correspondientes en la tabla Orders se establecerán automáticamente en NULL. Igualmente, la cláusula ON DELETE SET NULL significa que si se elimina un cliente de la tabla Customers, todas las claves externas correspondientes en la tabla Orders se establecerán automáticamente en NULL.</span><span class="sxs-lookup"><span data-stu-id="8b879-p109">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL. Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="8b879-p110">Para impedir la creación automática de índices para claves externas, se puede usar el modificador NO INDEX. Esta forma de definición de clave externa sólo debe usarse en casos en que los valores de índice resultantes se duplicarían con frecuencia. Si los valores de un índice de clave externa se duplican con frecuencia, el uso de un índice puede ser menos eficaz que simplemente realizar un recorrido de la tabla. El mantenimiento de este tipo de índice, con inserción y eliminación de filas en la tabla, disminuye el rendimiento y no aporta ninguna ventaja.</span><span class="sxs-lookup"><span data-stu-id="8b879-p110">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used. This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated. Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan. Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="8b879-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b879-162">Example</span></span>

<span data-ttu-id="8b879-163">Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.</span><span class="sxs-lookup"><span data-stu-id="8b879-163">This example creates a new table called ThisTable with two text fields.</span></span>

```vb 
 Sub CreateTableX1()    
Dim dbs As Database 
 
    ' Modify this line to include the path to Northwind 
    ' on your computer. 
    Set dbs = OpenDatabase("Northwind.mdb") 
 
    ' Create a table with two text fields. 
    dbs.Execute "CREATE TABLE ThisTable " _ 
        & "(FirstName CHAR, LastName CHAR);" 
 
    dbs.Close 
 
End Sub
```

<br/>

<span data-ttu-id="8b879-164">Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.</span><span class="sxs-lookup"><span data-stu-id="8b879-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="8b879-p111">Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="8b879-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

