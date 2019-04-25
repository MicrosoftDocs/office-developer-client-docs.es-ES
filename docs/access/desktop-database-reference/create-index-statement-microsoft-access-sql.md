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
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295432"
---
# <a name="create-index-statement-microsoft-access-sql"></a>Instrucción CREATE INDEX (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crea un índice en una tabla existente.

> [!NOTE]
> Para las bases de datos que no son del motor de base de datos de Microsoft Access, el motor de base de datos de Microsoft Access no admite el uso de CREATE INDEX (excepto para crear un pseudoíndice en una tabla vinculada ODBC) ni las instrucciones de lenguaje de definición de datos (DDL). En su lugar, use los métodos **Create** de DAO. Para más información, vea la sección Observaciones.

## <a name="syntax"></a>Sintaxis

CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]

La instrucción CREATE INDEX consta de las siguientes partes:

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
<td><p><em>index</em></p></td>
<td><p>El nombre del índice que se va a crear.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>El nombre de la tabla existente que contendrá el índice.</p></td>
</tr>
<tr class="odd">
<td><p><em>field</em></p></td>
<td><p>Nombre del campo o los campos que se van a indizar. Para crear un índice de campo único, enumere el nombre del campo entre paréntesis a continuación del nombre de la tabla. Para crear un índice de varios campos, enumere el nombre de cada campo que se incluirá en el índice. Para crear índices descendentes, use la palabra reservada DESC; de lo contrario, se supone que el orden de los índices es ascendente.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Para prohibir valores duplicados en el campo o campos indexados de registros diferentes, use la palabra reservada UNIQUE.

En la cláusula WITH opcional, puede aplicar reglas de validación de datos. Podrá:

- Impedir entradas Null en el campo o campos indexados de los registros nuevos mediante la opción DISALLOW NULL.

- Impedir que los registros con valores **Null** en el campo o campos indexados se incluyan en el índice mediante la opción IGNORE NULL.

- Designar el campo o campos indizados como la clave principal mediante la palabra reservada PRIMARY. Esto implica que la clave es única, por lo que se puede omitir la palabra reservada UNIQUE.

Puede usar CREATE INDEX para crear un pseudoíndice en una tabla vinculada de un origen de datos ODBC, como Microsoft SQL Server, que no tenga un índice. No es necesario permiso ni acceso al servidor remoto para crear un seudoíndice, y la base de datos remota no es consciente ni se ve afectada por el seudoíndice. Se usa la misma sintaxis para las tablas vinculadas y nativas. La creación de un seudoíndice en una tabla que normalmente sería de solo lectura puede ser especialmente útil.

También puede usar la instrucción [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para agregar un índice de campo único o de varios campos a una tabla y puede usar la instrucción ALTER TABLE o la instrucción [DROP](drop-statement-microsoft-access-sql.md) para eliminar un índice creado con ALTER TABLE o CREATE INDEX.

> [!NOTE]
> No use la palabra reservada PRIMARY al crear un índice en una tabla que ya tiene una clave principal; si lo hace, se produce un error.

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
