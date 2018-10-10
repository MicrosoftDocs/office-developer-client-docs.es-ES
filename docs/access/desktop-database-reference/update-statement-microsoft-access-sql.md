---
title: Instrucción UPDATE (Microsoft Access SQL)
TOCTitle: UPDATE Statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3affce9346e9e322bc588ca1c3be24867a1469d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484558"
---
# <a name="update-statement-microsoft-access-sql"></a>Instrucción UPDATE (Microsoft Access SQL)


**Se aplica a**: Access 2013 | Office 2013

Crea una consulta de actualización que cambia los valores de los campos de una tabla especificada a partir de los criterios especificados.

## <a name="syntax"></a>Sintaxis

UPDATE *tabla* SET *nuevoValor* WHERE *criterios*;

La instrucción UPDATE tiene estas partes:

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
<td><p>El nombre de la tabla que contiene los datos que quiere modificar.</p></td>
</tr>
<tr class="even">
<td><p><em>nuevoValor</em></p></td>
<td><p>Una expresión que determina el valor que se debe insertar en un campo concreto de los registros actualizados.</p></td>
</tr>
<tr class="odd">
<td><p><em>criterios</em></p></td>
<td><p>Una expresión que determina los registros que se actualizarán. Solo se actualizarán los registros que cumplan la expresión.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

UPDATE resulta especialmente útil cuando quiere cambiar muchos registros o cuando los registros que quiere cambiar están en varias tablas.

Puede cambiar varios campos a la vez. En el ejemplo siguiente, los valores de Importe del pedido (Order Amount) se aumentan un 10 % y los valores de Flete (Freight) se incrementan un 3 % para los remitentes que están en el Reino Unido:

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
> <UL>
> <LI>
> <P>UPDATE no genera un conjunto de resultados. Además, después de actualizar registros con una consulta de actualización, no se puede deshacer la operación. Si quiere saber qué registros se actualizaron, en primer lugar, examine los resultados de una consulta de selección que use los mismos criterios y, luego, ejecute la consulta de actualización.</P>
> <LI>
> <P>Mantenga copias de seguridad de los datos en todo momento. Si actualiza los registros equivocados, puede recuperarlos a partir de las copias de seguridad.</P></LI></UL>



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
