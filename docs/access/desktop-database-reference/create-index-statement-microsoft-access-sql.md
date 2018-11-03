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
ms.openlocfilehash: 1b12fcf4d92bbe0949065557973efe94688a7a30
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937207"
---
# <a name="create-index-statement-microsoft-access-sql"></a>Instrucción CREATE INDEX (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Crea un índice nuevo en una tabla existente.

> [!NOTE]
> Para las bases de datos del motor de base de datos de no sean de Microsoft Access, el motor de base de datos de Microsoft Access no admite el uso de CREATE INDEX (excepto para crear un pseudoíndice en una tabla vinculada ODBC) o cualquiera de las instrucciones de lenguaje (DDL) de definición de datos. Utilice los métodos DAO **crear** en su lugar. Si desea más información, vea la sección Comentarios.

## <a name="syntax"></a>Sintaxis

CREAR \[ UNIQUE \] INDEX *índice* ON *tabla* (*campo* \[ASC | DESC\]\[, *campo* \[ASC | DESC\],... \]) \[WITH {principal | DISALLOW NULL | IGNORE NULL}\]

La instrucción CREATE INDEX consta de los siguientes elementos:

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
<td><p><em>índice</em></p></td>
<td><p>Nombre del índice que se va a crear.</p></td>
</tr>
<tr class="even">
<td><p><em>tabla</em></p></td>
<td><p>Nombre de la tabla existente que contendrá el índice.</p></td>
</tr>
<tr class="odd">
<td><p><em>campo</em></p></td>
<td><p>Nombre del campo o los campos que se van a indizar. Para crear un índice de campo único, enumere el nombre del campo entre paréntesis a continuación del nombre de la tabla. Para crear un índice de varios campos, enumere el nombre de cada campo que se incluirá en el índice. Para crear índices descendentes, use la palabra reservada DESC; de lo contrario, se supone que el orden de los índices es ascendente.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Para prohibir valores duplicados en el campo o campos indizados de diferentes registros, use la palabra reservada UNIQUE.

En la cláusula opcional WITH, puede aplicar las reglas de validación de datos. Se puede:

- Prohibir entradas Null en el campo o campos indizados de nuevos registros mediante la opción DISALLOW NULL.

- Impedir que los registros con valores **Null** en el campo o campos indizados se incluyan en el índice mediante la opción IGNORE NULL.

- Designar el campo o campos indizados como la clave principal mediante la palabra reservada PRIMARY. Esto implica que la clave es única, por lo que se puede omitir la palabra reservada UNIQUE.

Puede utilizar CREATE INDEX para crear un pseudoíndice en una tabla vinculada en un origen de datos ODBC, como Microsoft SQL Server, que ya no tiene un índice. No es necesario permiso o acceso al servidor remoto para crear un pseudoíndice y éste no es conocido por la base de datos remota ni le afecta. Se usa la misma sintaxis para las tablas vinculadas y nativas. Puede ser especialmente útil la creación de un pseudoíndice en una tabla que normalmente será de sólo lectura.

También puede usar la instrucción [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para agregar un índice de campo único o de varios campos a una tabla y puede usar la instrucción ALTER TABLE o la instrucción [DROP](drop-statement-microsoft-access-sql.md) para eliminar un índice creado con ALTER TABLE o CREATE INDEX.

> [!NOTE]
> [!NOTA] No use la palabra reservada PRIMARY al crear un nuevo índice en una tabla que ya tenga una clave principal; si lo hace, se producirá un error.

## <a name="example"></a>Ejemplo

En este ejemplo, se crea un índice formado por los campos Home Phone (Teléfono particular) y Extension (Extensión) de la tabla Employees (Empleados).

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

En este ejemplo, se crea un índice en la tabla Customers (Clientes) con el campo CustomerID (IDCliente). No puede haber dos registros que tengan los mismos datos en el campo CustomerID y no se permiten valores Null.

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
