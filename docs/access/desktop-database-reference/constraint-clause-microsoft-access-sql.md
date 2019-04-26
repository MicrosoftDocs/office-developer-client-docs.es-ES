---
title: Cláusula CONSTRAINT (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 356620376658bb927c690056f4de9a01554aa47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295649"
---
# <a name="constraint-clause-microsoft-access-sql"></a>Cláusula CONSTRAINT (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Una restricción es similar a un índice, aunque se puede usar para establecer una relación con otra tabla.

La cláusula CONSTRAINT se usa en las instrucciones [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) y [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para crear o eliminar restricciones. Hay dos tipos de cláusulas CONSTRAINT: uno para crear una restricción en un único campo y otro para crear una restricción en varios campos.

> [!NOTE]
> El motor de base de datos de Microsoft Access no admite el uso de CONSTRAINT, ni las instrucciones de lenguaje de definición de datos (DDL), con bases de datos que no sean del motor de base de datos de Microsoft Access. En su lugar, use los métodos **Create** de DAO.

## <a name="syntax"></a>Sintaxis

### <a name="single-field-constraint"></a>Restricción de un único campo

CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

### <a name="multiple-field-constraint"></a>Restricción de varios campos

CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

La cláusula CONSTRAINT consta de los elementos siguientes:

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
<td><p><em>name</em></p></td>
<td><p>Nombre de la restricción que se va a crear.</p></td>
</tr>
<tr class="even">
<td><p><em>primary1</em>, <em>primary2</em></p></td>
<td><p>Nombre del campo o campos que se designarán como clave principal.</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>Nombre del campo o los campos que se van a designar como clave única.</p></td>
</tr>
<tr class="even">
<td><p><em>nonulo1, nonulo2</em></p></td>
<td><p>Nombre del campo o los campos que se restringen a valores no nulos.</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>Nombre del campo o campos de clave externa que hacen referencia a campos de otra tabla.</p></td>
</tr>
<tr class="even">
<td><p><em>foreigntable</em></p></td>
<td><p>Nombre de la tabla externa que contiene el campo o los campos especificados en <em>campoExterno</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>foreignfield1</em>, <em>foreignfield2</em></p></td>
<td><p>Nombre del campo o los campos de <em>tablaExterna</em> que <em>ref1</em>, <em>ref2</em> especifiquen. Esta cláusula no se puede omitir si el campo al que se hace referencia es la clave principal de <em>tablaExterna</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use la sintaxis de una restricción de un solo campo en la cláusula de definición de campo de una instrucción ALTER TABLE o CREATE TABLE seguida inmediatamente de la especificación del tipo de datos del campo.

La sintaxis de una restricción de varios campos se usa cuando se utiliza la palabra reservada CONSTRAINT fuera de una cláusula de definición de campos en una instrucción ALTER TABLE o CREATE TABLE.

Con CONSTRAINT puede designar un campo como uno de los tipos de restricciones siguientes:

- Puede usar la palabra reservada UNIQUE para designar un campo como clave única. Esto significa que dos registros de la tabla no pueden tener el mismo valor en este campo. Puede restringir cualquier campo o lista de campos como clave única. Si una restricción de varios campos se designa como clave única, los valores combinados de todos los campos del índice deben ser únicos, aunque dos o más registros tengan el mismo valor en solo uno de los campos.

- Puede usar las palabras reservadas PRIMARY KEY para designar un campo o conjunto de campos de una tabla como clave principal. Todos los valores de la clave principal deben ser únicos y no **nulos**, y solo puede haber una clave principal para una tabla.
    
  > [!NOTE]
  > No establezca una restricción PRIMARY KEY en una tabla que ya tenga una clave principal; si lo hace, se produce un error.

- Puede usar las palabras reservadas FOREIGN KEY para designar un campo como una clave externa. Si la clave principal de la tabla externa consta de varios campos, debe usar una definición de restricción de varios campos en la que se enumeren todos los campos de referencia, el nombre de la tabla externa y los nombres de los campos a los que se hace referencia en la tabla externa en el mismo orden en que se enumeran los campos que tienen la referencia. Si el campo o los campos a los que se hace referencia son la clave principal de la tabla externa, no es necesario especificar los campos a los que se hace referencia. De forma predeterminada, el motor de base de datos se comporta como si la clave principal de la tabla externa fueran los campos a los que se hace referencia. Las restricciones de clave externa definen acciones específicas que se deben realizar cuando se cambia un valor de clave principal correspondiente:

- Puede especificar acciones que se van a realizar en la tabla externa en función de que se realice una acción correspondiente en una clave principal de la tabla en la que se define CONSTRAINT. Por ejemplo, considere la siguiente definición de la tabla Clientes:
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Considere la siguiente definición de la tabla Pedidos, que define una relación de clave externa que hace referencia a la clave principal de la tabla Clientes:
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Las cláusulas ON UPDATE CASCADE y ON DELETE CASCADE están definidas en la clave externa. La cláusula ON UPDATE CASCADE significa que si se actualiza el identificador de un cliente (CustId) en la tabla Customers, la actualización se propagará en cascada en la tabla Orders. Cada pedido que contenga un valor de identificador de cliente correspondiente se actualizará automáticamente con el nuevo valor. La cláusula ON DELETE CASCADE significa que si se elimina un cliente de la tabla Customers, todas las filas de la tabla Orders que contengan el mismo valor de identificador de cliente también se eliminarán. Considere la siguiente definición diferente de la tabla Orders, en la que se usa la acción SET NULL en lugar de la acción CASCADE:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  La cláusula ON UPDATE SET NULL indica que, si un identificador de cliente (CustId) se actualiza en la tabla Clientes, los valores de clave externa correspondientes se establecerán automáticamente en NULL. La cláusula ON DELETE SET NULL indica que, si un cliente se elimina de la tabla Clientes, todos los valores de clave externa correspondientes de la tabla Pedidos se establecerán automáticamente en NULL.

Para evitar la creación automática de índices de claves externas, se puede usar el modificador NO INDEX. Este formulario de definición de clave externa solo debe usarse en aquellos casos en que los valores resultantes de índice se duplicarían con frecuencia. Cuando los valores de un índice de clave externa se duplican con frecuencia, el uso de un índice puede ser menos eficaz que simplemente realizar un análisis de la tabla. El mantenimiento de este tipo de índice, con filas insertadas y eliminadas en la tabla, degrada el rendimiento y no ofrece ninguna ventaja.

## <a name="example"></a>Ejemplo

Este ejemplo crea una nueva tabla llamada ThisTable con dos campos de texto.

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

Este ejemplo crea una nueva tabla llamada MyTable con dos campos de texto, un campo Date/Time y un índice único formado por todos los tres campos.

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

Este ejemplo crea una nueva tabla con dos campos de texto y un campo **Integer**. El campo SSN es la clave primaria.

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

