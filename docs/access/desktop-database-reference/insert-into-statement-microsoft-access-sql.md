---
title: Instrucción INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291336"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>Instrucción INSERT INTO (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Agrega uno o varios registros a una tabla. A esto se le denomina consulta anexada.

## <a name="syntax"></a>Sintaxis

### <a name="multiple-record-append-query"></a>Consulta anexada de varios registros:

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*

### <a name="single-record-append-query"></a>Consulta anexada de un solo registro:

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])

La instrucción INSERT INTO tiene estas partes:

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
<td><p><em>target</em></p></td>
<td><p>El nombre de la tabla o consulta en la cual se anexarán los registros.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Nombres de los campos en los que se van a anexar los datos, si siguen un argumento <em>target</em>, o los nombres de los campos desde los cuales obtener datos, si siguen un argumento <em>source</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>La ruta de acceso a una base de datos externa. Para obtener una descripción de la ruta de acceso, consulte la cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>El nombre de la tabla o consulta desde la cual se copiarán los registros.</p></td>
</tr>
<tr class="odd">
<td><p><em>table1xpression</em></p></td>
<td><p>El nombre de la tabla o de las tablas desde las cuales se insertarán los registros. Este argumento puede ser un único nombre de tabla o compuesto como resultado de una operación <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> o <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> o una consulta guardada.</p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>, <em>value2</em></p></td>
<td><p>Los valores que se insertarán en los campos específicos del nuevo registro. Cada valor se inserta en el campo que corresponde a la posición del valor en la lista: <em>value1</em> se inserta en <em>field1</em> del nuevo registro, <em>value2</em> en <em>field2</em>, y así sucesivamente. Debe separar los valores con una coma y escribir los campos de texto entre comillas (' ').</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar la instrucción INSERT INTO para añadir un solo registro a una tabla con la sintaxis de consulta anexada de un solo registro, tal como se muestra arriba. En este caso, el código especifica el nombre y el valor para cada campo del registro. Debe especificar cada uno de los campos del registro al cual se asignará un valor, y debe especificar un valor para ese campo. Cuando no especifica cada campo, el valor predeterminado o **Null** se inserta para las columnas que faltan. Los registros se añaden al final de la tabla.

También puede usar INSERT INTO para anexar un conjunto de registros desde otra tabla o consulta con la cláusula SELECT … FROM, tal como se muestra más arriba en la consulta anexada de varios registros. En este caso, la cláusula SELECT especifica los campos a los que anexar la tabla *target* especificada.

La tabla *source* o *target* puede especificar una tabla o una consulta. Si se especifica una consulta, el motor de base de datos de Microsoft Access anexa los registros a cualquier tabla especificada por la consulta.

INSERT INTO es opcional pero, cuando se incluye, antecede a la instrucción [SELECT](select-statement-microsoft-access-sql.md).

Si la tabla de destino contiene una clave primaria, asegúrese de anexar valores únicos que no sean **Null** al campo o a los campos de claves primarias. Si no lo hace, el motor de base de datos de Microsoft Access no anexará registros.

Si anexa registros a una tabla con un campo AutoNumber y desea reenumerar los registros anexados, no incluya el campo AutoNumber en la consulta. Incluya el campo AutoNumber en la consulta si desea conservar los valores originales del campo.

Use la cláusula IN para anexar registros a una tabla en otra base de datos.

Para crear una nueva tabla, use la instrucción [SELECT… INTO](select-into-statement-microsoft-access-sql.md) para crear una consulta de creación de tabla.

Para averiguar qué registros se anexarán antes de la ejecución de la consulta anexada, primero ejecute y vea los resultados de una consulta seleccionada que use los mismos criterios de selección.

Una consulta anexada copia registros de una o más tablas a otra. Las tablas que contienen los registros que anexa no se ven afectadas por la consulta anexada.

En vez de anexar registros existentes de otra tabla, puede especificar el valor para cada campo en un solo registro nuevo con la cláusula VALUES. Si omite la lista de campos, la cláusula VALUES debe incluir un valor para cada campo en la tabla; de lo contrario, la operación INSERT fallará. Use una instrucción INSERT INTO adicional con una cláusula VALUES para cada registro adicional que desee crear.

**Vínculos proporcionados por** la comunidad de [UtterAccess](https://www.utteraccess.com). UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.

- [Generación de números secuenciales para instrucciones INSERT/UPDATE](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [Herramienta de formato de SQL a VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>Ejemplo

Este ejemplo selecciona todos los registros en una tabla hipotética New Customers y los añade a la tabla Customers. Cuando no se designan columnas individuales, los nombres de columna de tabla SELECT deben coincidir exactamente con los nombres en la tabla INSERT INTO.

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

Este ejemplo muestra un nuevo registro en la tabla Employees.

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

