---
title: Instrucción UPDATE (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6a0404c21b308f6e389ee5577cc212763e660774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306247"
---
# <a name="update-statement-microsoft-access-sql"></a>Instrucción UPDATE (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crea una consulta de actualización que cambia los valores de los campos de una tabla especificada a partir de los criterios especificados.

## <a name="syntax"></a>Sintaxis

UPDATE *tabla* SET *valor nuevo* WHERE *criterios*;

La instrucción UPDATE consta de las siguientes partes:

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
<td><p><em>table</em></p></td>
<td><p>El nombre de la tabla que contiene los datos que quiere modificar.</p></td>
</tr>
<tr class="even">
<td><p><em>nuevoValor</em></p></td>
<td><p>Expresión que determina el valor que se debe insertar en un campo determinado en los registros actualizados.</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>Expresión que determina qué registros serán actualizados. Solo se actualizarán los registros que cumplan la expresión.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

UPDATE es especialmente útil cuando quiere modificar muchos registros o cuando los registros que quiere modificar están en varias tablas.

Puede cambiar varios campos al mismo tiempo. En el siguiente ejemplo, se incrementan los valores de Cantidad del pedido en un 10 por ciento y los valores de Carga en un 3 por ciento para los transportistas del Reino Unido:

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- UPDATE no genera un conjunto de resultados. Además, después de actualizar registros con una consulta de actualización, no se puede deshacer la operación. Si quiere saber qué registros se actualizaron, en primer lugar, examine los resultados de una consulta de selección que use los mismos criterios y, luego, ejecute la consulta de actualización.
- Mantenga copias de seguridad de los datos en todo momento. Si actualiza los registros incorrectos, podrá recuperarlos de las copias de seguridad.



## <a name="example"></a>Ejemplo

En este ejemplo, se cambian los valores del campo ReportsTo a 5 en todos los registros de empleados que tengan actualmente valores de 2 en el campo ReportsTo.

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
