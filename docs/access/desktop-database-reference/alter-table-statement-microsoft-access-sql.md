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
ms.openlocfilehash: f7dfaa7a8c3d6b3e41b2443bcca621d083c3a167
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889633"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>Instrucción ALTER TABLE (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Modifica el diseño de una tabla después de que se ha creado con la instrucción [CREATE TABLE](create-table-statement-microsoft-access-sql.md).

> [!NOTE]
> [!NOTA] El motor de base de datos de Microsoft Access no admite el uso de ALTER TABLE, ni las instrucciones de lenguaje de definición de datos (DDL), con bases de datos que no sean de Microsoft Access. Utilice en su lugar los métodos **Create de DAO** .

## <a name="syntax"></a>Sintaxis

ALTER TABLE *tabla* {agregar {el *tipo de campo*de columna\[(*tamaño*)\] \[NOT NULL\] \[CONSTRAINT *índice* \] | ALTER COLUMN *tipo de campo*\[(*tamaño*)\] | CONSTRAINT *índicedevarioscampos*} | DROP {COLUMN *campo* I CONSTRAINT *nombreDeÍndice*}}

La instrucción ALTER TABLE consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>tabla</em></p></td>
<td><p>Nombre de la tabla que se va a modificar.</p></td>
</tr>
<tr class="even">
<td><p><em>campo</em></p></td>
<td><p>Nombre del campo que se va a agregar o eliminar en la <em>tabla</em>. O bien, nombre del campo que se va a modificar en la <em>tabla</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Tipo de datos del <em>campo</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</p></td>
</tr>
<tr class="odd">
<td><p><em>índice</em></p></td>
<td><p>Índice del <em>campo</em>. Para obtener más información acerca de cómo construir este índice, vea <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>índiceDeVariosCampos</em></p></td>
<td><p>La definición de un índice de varios campos que se agregará a <em>la tabla</em>. Para obtener más información acerca de cómo construir este índice, vea <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>nombreDeÍndice</em></p></td>
<td><p>Nombre del índice de varios campos que se eliminará.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Mediante el uso de la instrucción ALTER TABLE, puede modificar una tabla existente de varias maneras. Se puede:

- Usar ADD COLUMN para agregar un campo nuevo a la tabla. Debe especificar el nombre del campo, el tipo de datos y (para los campos de tipo texto y binario) un tamaño opcional. Por ejemplo, la siguiente instrucción agrega un campo de texto de 25 caracteres llamado Notes a la tabla Employees:
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  También puede definir un índice en ese campo. Para obtener más información acerca de los índices de un solo campo, vea la [cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).
    
  Si se especifica NOT NULL para un campo, se requieren nuevos registros tengan datos válidos en ese campo.

- Usar ALTER COLUMN para cambiar el tipo de datos de un campo existente. Debe especificar el nombre del campo, el nuevo tipo de datos y un tamaño opcional para los campos de tipo texto y binario. Por ejemplo, la siguiente instrucción cambia el tipo de datos de un campo de la tabla Employees llamado ZipCode (definido originalmente como Integer) a un campo Texto de 10 caracteres:
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- Usar ADD CONSTRAINT para agregar un índice de varios campos. Para obtener más información acerca de los índices de varios campos, vea la [cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).

- Usar DROP COLUMN para eliminar un campo. Sólo debe especificar el nombre del campo.

- Usar DROP CONSTRAINT para eliminar un índice de varios campos. Sólo debe especificar el nombre del índice a continuación de la palabra reservada CONSTRAINT.


> [!NOTE] 
> - [!NOTA] No se puede agregar o eliminar más de un campo o índice a la vez.
> - Puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para agregar un índice de un solo campo o de varios campos a un tabla y puede usar ALTER TABLE o la instrucción [DROP](drop-statement-microsoft-access-sql.md) para eliminar un índice creado con ALTER TABLE o CREATE INDEX.
> - No puede usar NOT NULL en un campo único o en una cláusula CONSTRAINT con nombre que se aplique a un solo campo o a una cláusula CONSTRAINT con nombre de varios campos. Sin embargo, puede aplicar la restricción NOT NULL sólo una vez a un campo. Si intenta aplicar esta restricción más de una vez, se producirá un error en tiempo de ejecución. 


## <a name="example"></a>Ejemplo

En este ejemplo, se agrega un campo Salary con el tipo de datos **Money** a la tabla Employees.

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

En este ejemplo, se cambia el tipo de datos del campo Salary de **Money** a **Char**.

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

En este ejemplo, se quita el campo Salary de la tabla Employees.

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

En este ejemplo, se agrega una clave externa a la tabla Orders. La clave externa se basa en el campo EmployeeID y hace referencia al campo EmployeeID de la tabla Employees. En este ejemplo, no tiene que enumerar el campo EmployeeID después de la tabla Employees en la cláusula REFERENCES porque EmployeeID es la clave principal de la tabla Employees.

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

En este ejemplo, se elimina la clave externa de la tabla Orders.

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
