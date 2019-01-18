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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703786"
---
# <a name="constraint-clause-microsoft-access-sql"></a>Cláusula CONSTRAINT (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Una restricción es similar a un índice, aunque se puede usar para establecer una relación con otra tabla.

La cláusula CONSTRAINT se usa en las instrucciones [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) y [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para crear o eliminar restricciones. Hay dos tipos de cláusulas CONSTRAINT: uno para crear una restricción en un único campo y otro para crear una restricción en varios campos.

> [!NOTE]
> [!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CONSTRAINT, ni las instrucciones de lenguaje de definición de datos (DDL), con bases de datos que no sean del motor de base de datos de Microsoft Access. Utilice los métodos DAO **crear** en su lugar.

## <a name="syntax"></a>Sintaxis

### <a name="single-field-constraint"></a>Restricción de campo único

CONSTRAINT *nombre* {PRIMARY KEY | ÚNICO | NOT NULL | REFERENCES *tablaexterna* \[(*campoexterno1, campoexterno2*)\] \[ON UPDATE CASCADE | ESTABLECER como NULL\] \[ON DELETE CASCADE | ESTABLECER como NULL\]}

### <a name="multiple-field-constraint"></a>Restricción de varios campos

CONSTRAINT *nombre* {PRIMARY KEY (*principal1*\[, *principal2* \[,... \]\]) | ÚNICO (*único1*\[, *único2* \[,... \]\]) | NOT NULL (*noNull1*\[, *noNull2* \[,... \]\]) | CLAVE externa \[sin índice\] (*referencia1*\[, *referencia2* \[,... \] \]) REFERENCES *tablaexterna* \[(*campoexterno1* \[, *campoexterno2* \[,... \] \])\] \[ON UPDATE CASCADE | ESTABLECER como NULL\] \[ON DELETE CASCADE | ESTABLECER como NULL\]}

La cláusula CONSTRAINT consta de los siguientes elementos:

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
<td><p><em>name</em></p></td>
<td><p>Nombre de la restricción que se va a crear.</p></td>
</tr>
<tr class="even">
<td><p><em>principal1</em>, <em>principal2</em></p></td>
<td><p>Nombre del campo o campos que se designarán como clave principal.</p></td>
</tr>
<tr class="odd">
<td><p><em>único1</em>, <em>único2</em></p></td>
<td><p>Nombre del campo o campos que se designarán como clave única.</p></td>
</tr>
<tr class="even">
<td><p><em>noNull1, noNull2</em></p></td>
<td><p>Nombre del campo o campos restringidos a valores distintos de Null.</p></td>
</tr>
<tr class="odd">
<td><p><em>referencia1</em>, <em>referencia2</em></p></td>
<td><p>Nombre del campo o campos de clave externa que hacen referencia a campos de otra tabla.</p></td>
</tr>
<tr class="even">
<td><p><em>tablaExterna</em></p></td>
<td><p>Nombre de la tabla externa que contiene el campo o los campos especificados en <em>campoExterno</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>campoExterno1</em>, <em>campoExterno2</em></p></td>
<td><p>Nombre del campo o los campos de <em>tablaExterna</em> especificados en <em>referencia1</em>, <em>referencia2</em>. Esta cláusula se puede omitir si el campo al que se hace referencia es la clave principal de <em>tablaExterna</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La sintaxis de una restricción de campo único se usa en la cláusula de definición de campos de una instrucción ALTER TABLE o CREATE TABLE que sigue inmediatamente a la especificación del tipo de datos del campo.

La sintaxis de una restricción de varios campos se usa cuando se utiliza la palabra reservada CONSTRAINT fuera de una cláusula de definición de campos en una instrucción ALTER TABLE o CREATE TABLE.

Mediante CONSTRAINT, puede designar un campo como uno de los siguientes tipos de restricciones:

- Puede usar la palabra reservada UNIQUE para designar un campo como una clave única. Esto significa que no puede haber dos registros en la tabla que tengan el mismo valor en este campo. Puede restringir cualquier campo o lista de campos como único. Si se designa una restricción de varios campos como una clave única, los valores combinados de todos los campos del índice deben ser únicos, incluso si dos o más registros tienen el mismo valor en uno solo de los campos.

- Puede usar las palabras reservadas PRIMARY KEY para designar un campo o conjunto de campos de una tabla como clave principal. Todos los valores de la clave principal deben ser únicos y distintos de **Null**, y sólo puede haber una clave principal para una tabla.
    
  > [!NOTE]
  > [!NOTA] No establezca una restricción PRIMARY KEY en una tabla que ya tenga una clave principal; si lo hace, se producirá un error.

- Puede usar las palabras reservadas FOREIGN KEY para designar un campo como una clave externa. Si la clave principal de la tabla externa consta de varios campos, debe usar una definición de restricción de varios campos en la que se enumeren todos los campos de referencia, el nombre de la tabla externa y los nombres de los campos a los que se hace referencia en la tabla externa en el mismo orden en que se enumeran los campos que tienen la referencia. Si el campo o los campos a los que se hace referencia son la clave principal de la tabla externa, no es necesario especificar los campos a los que se hace referencia. De forma predeterminada, el motor de base de datos se comporta como si la clave principal de la tabla externa fueran los campos a los que se hace referencia. Las restricciones de clave externa definen acciones específicas que se deben realizar cuando se cambia un valor de clave principal correspondiente:

- Puede especificar acciones que se deben llevar a cabo en la tabla externa en función de una acción correspondiente realizada en una clave principal de la tabla en la que se define CONSTRAINT. Por ejemplo, considere la siguiente definición para la tabla Customers:
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Considere la siguiente definición de la tabla Orders, que define una relación de clave externa que hace referencia a la clave principal de la tabla Customers:
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Las cláusulas ON UPDATE CASCADE y ON DELETE CASCADE están definidas en la clave externa. La cláusula ON UPDATE CASCADE significa que si se actualiza el identificador de un cliente (CustId) en la tabla Customers, la actualización se propagará en cascada en la tabla Orders. Cada pedido que contenga un valor de identificador de cliente correspondiente se actualizará automáticamente con el nuevo valor. La cláusula ON DELETE CASCADE significa que si se elimina un cliente de la tabla Customers, todas las filas de la tabla Orders que contengan el mismo valor de identificador de cliente también se eliminarán. Considere la siguiente definición diferente de la tabla Orders, en la que se usa la acción SET NULL en lugar de la acción CASCADE:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  La cláusula ON UPDATE SET NULL significa que si se actualiza el identificador de un cliente (CustId) en la tabla Customers, los valores de clave externa correspondientes en la tabla Orders se establecerán automáticamente en NULL. Igualmente, la cláusula ON DELETE SET NULL significa que si se elimina un cliente de la tabla Customers, todas las claves externas correspondientes en la tabla Orders se establecerán automáticamente en NULL.

Para impedir la creación automática de índices para claves externas, se puede usar el modificador NO INDEX. Esta forma de definición de clave externa sólo debe usarse en casos en que los valores de índice resultantes se duplicarían con frecuencia. Si los valores de un índice de clave externa se duplican con frecuencia, el uso de un índice puede ser menos eficaz que simplemente realizar un recorrido de la tabla. El mantenimiento de este tipo de índice, con inserción y eliminación de filas en la tabla, disminuye el rendimiento y no aporta ninguna ventaja.

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

