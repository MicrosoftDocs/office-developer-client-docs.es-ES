---
title: Instrucción DROP (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293654"
---
# <a name="drop-statement-microsoft-access-sql"></a>Instrucción DROP (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Elimina una tabla, procedimiento o vista existente de una base de datos o elimina un índice existente de una tabla.

> [!NOTE]
> El motor de base de datos de Microsoft Access no admite el uso de DROP, ni las instrucciones DDL, con bases de datos que no sean del motor de base de datos de Microsoft Access. En su lugar, use el método **Delete** de DAO.

## <a name="syntax"></a>Sintaxis

DROP {TABLE *tabla* | INDEX *índice* ON *tabla* | PROCEDURE *procedimiento* | VIEW *vista*}

La instrucción DROP consta de las siguientes partes:

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
<td><p><em>tabla</em></p></td>
<td><p>El nombre de la tabla que se va a eliminar o la tabla desde la que se va a eliminar un índice.</p></td>
</tr>
<tr class="even">
<td><p><em>procedimiento</em></p></td>
<td><p>El nombre del procedimiento que se va a eliminar.</p></td>
</tr>
<tr class="odd">
<td><p><em>ver</em></p></td>
<td><p>El nombre de la vista que se va a eliminar.</p></td>
</tr>
<tr class="even">
<td><p><em>índice</em></p></td>
<td><p>El nombre del índice que se va a eliminar de <em>tabla.</em></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Debe cerrar la tabla antes de poder eliminar o quitar un índice de ella.

También puede usar [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para eliminar un índice en la tabla.

Puede usar [CREATE TABLE](create-table-statement-microsoft-access-sql.md)para crear una tabla y [CREATE INDEX](create-index-statement-microsoft-access-sql.md) o ALTER TABLE para crear un índice. Para modificar una tabla, use ALTER TABLE.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se supone la existencia de un índice hipotético NewIndex en la tabla Employees de la base de datos Neptuno.

En este ejemplo, se elimina el índice MyIndex de la tabla Employees.

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

En este ejemplo se elimina la tabla Employees de la base de datos.

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
