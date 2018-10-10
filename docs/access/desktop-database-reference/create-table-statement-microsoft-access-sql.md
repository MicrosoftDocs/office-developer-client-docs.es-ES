---
title: Instrucción CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE Statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 749d593a0c9ed32290ee91aec20c79a141a83f56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484977"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Instrucción CREATE TABLE (Microsoft Access SQL)

**Se aplica a**: Access 2013 | Office 2013

Crea una tabla nueva.

> [!NOTE]
> [!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE TABLE, o ninguna de las instrucciones DDL, con bases de datos cuyo motor no sea de Microsoft Access. En su lugar, use los métodos DAO Create.

## <a name="syntax"></a>Sintaxis

CREAR \[temporal\] tabla *tabla* (*campo1 tipo* \[(*tamaño*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[ *índice1* \] \[, *campo2* *tipo* \[(*tamaño*)\] \[NOT NULL\] \[ *índice2* \] \[,... \] \] \[, CONSTRAINT *índicedevarioscampos* \[,... \]\])

La instrucción CREATE TABLE tiene estas partes:

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
<td><p><em>table</em></p></td>
<td><p>Nombre de la tabla que se va a eliminar.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>El nombre del campo o de los campos que se crearán en la tabla nueva. Debe crear al menos un campo.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>El tipo de datos del <em>campo</em> en la nueva tabla.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Tamaño del campo en caracteres (sólo los campos de tipo texto y binario).</p></td>
</tr>
<tr class="odd">
<td><p><em>index1</em>, <em>index2</em></p></td>
<td><p>Cláusula CONSTRAINT que define un índice de un solo campo. Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>Cláusula CONSTRAINT que define un índice de varios campos. Para obtener más información sobre cómo crear este índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use la instrucción CREATE TABLE para definir una nueva tabla y sus campos y restricciones de campos. Si se especifica NOT NULL para un campo, los nuevos registros deben tener datos válidos en ese campo.

Cláusula CONSTRAINT que establece varias restricciones en un campo y que se puede usar para establecer la clave primaria. También puede usar la instrucción [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para crear una clave primaria o índices adicionales en tablas existentes.

Puede usar NOT NULL en un solo campo o en una cláusula llamada CONSTRAINT que se aplica a un solo campo o a varios campos llamados CONSTRAINT. Sin embargo, puede aplicar la restricción NOT NULL una sola vez en un campo. Al intentar aplicar esta restricción más de una sola vez, se genera un error en tiempo de ejecución

Cuando se crea una tabla TEMPORARY, queda visible solamente en la sesión en que fue creada. Se elimina automáticamente cuando la sesión finaliza. Más de un usuario puede tener acceso a las tablas temporales.

El atributo WITH COMPRESSION puede usarse solo con los tipos de datos CHARACTER y MEMO (también conocidos como TEXT) y sus sinónimos.

El atributo WITH COMPRESSION se añadió para las columnas CHARACTER debido al cambio a formato de representación de caracteres Unicode. Los caracteres Unicode requieren uniformemente dos bytes para cada carácter. Para bases de datos existentes de Microsoft® Jet que contienen datos de caracteres principalmente, esto podría significar que el archivo de la base de datos tendría casi el doble de tamaño al convertirse a formato de motor de base de datos de Microsoft Access. Sin embargo, se puede comprimir fácilmente en un byte simple la representación Unicode de muchos conjuntos de caracteres, aquellos antes denominados como Single-Byte Character Sets (SBCS). Si define una columna CHARACTER con este atributo, los datos se comprimirán automáticamente mientras se almacenan y se descomprimirán al recuperarse de la columna.

Las columnas MEMO también pueden definirse para almacenar datos en un formato comprimido. Sin embargo, existe una limitación. Solamente se comprimirán las instancias de columnas MEMO que, al comprimirse, tengan 4096 bytes o menos. Todas las demás instancias de columnas MEMO permanecerán sin comprimir. Esto significa que en una tabla determinada, para una columna MEMO determinada, algunos datos pueden comprimirse y algunos datos pueden no comprimirse.

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
