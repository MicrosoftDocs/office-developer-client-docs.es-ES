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
ms.openlocfilehash: 4e7f27cb696b085b5c4536477ee3454df09cfabe
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881289"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="28c41-102">Instrucción UPDATE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="28c41-102">UPDATE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="28c41-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28c41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28c41-104">Crea una consulta de actualización que cambia los valores de los campos de una tabla especificada a partir de los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="28c41-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28c41-105">Syntax</span></span>

<span data-ttu-id="28c41-106">UPDATE *tabla* SET *nuevoValor* WHERE *criterios*;</span><span class="sxs-lookup"><span data-stu-id="28c41-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span></span>

<span data-ttu-id="28c41-107">La instrucción UPDATE tiene estas partes:</span><span class="sxs-lookup"><span data-stu-id="28c41-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28c41-108">Parte</span><span class="sxs-lookup"><span data-stu-id="28c41-108">Part</span></span></p></th>
<th><p><span data-ttu-id="28c41-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="28c41-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28c41-110"><em>tabla</em></span><span class="sxs-lookup"><span data-stu-id="28c41-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="28c41-111">El nombre de la tabla que contiene los datos que quiere modificar.</span><span class="sxs-lookup"><span data-stu-id="28c41-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28c41-112"><em>nuevoValor</em></span><span class="sxs-lookup"><span data-stu-id="28c41-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="28c41-113">Una expresión que determina el valor que se debe insertar en un campo concreto de los registros actualizados.</span><span class="sxs-lookup"><span data-stu-id="28c41-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28c41-114"><em>criterios</em></span><span class="sxs-lookup"><span data-stu-id="28c41-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="28c41-p101">Una expresión que determina los registros que se actualizarán. Solo se actualizarán los registros que cumplan la expresión.</span><span class="sxs-lookup"><span data-stu-id="28c41-p101">An expression that determines which records will be updated. Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="28c41-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28c41-117">Remarks</span></span>

<span data-ttu-id="28c41-118">UPDATE resulta especialmente útil cuando quiere cambiar muchos registros o cuando los registros que quiere cambiar están en varias tablas.</span><span class="sxs-lookup"><span data-stu-id="28c41-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="28c41-p102">Puede cambiar varios campos a la vez. En el ejemplo siguiente, los valores de Importe del pedido (Order Amount) se aumentan un 10 % y los valores de Flete (Freight) se incrementan un 3 % para los remitentes que están en el Reino Unido:</span><span class="sxs-lookup"><span data-stu-id="28c41-p102">You can change several fields at the same time. The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- <span data-ttu-id="28c41-p103">UPDATE no genera un conjunto de resultados. Además, después de actualizar registros con una consulta de actualización, no se puede deshacer la operación. Si quiere saber qué registros se actualizaron, en primer lugar, examine los resultados de una consulta de selección que use los mismos criterios y, luego, ejecute la consulta de actualización.</span><span class="sxs-lookup"><span data-stu-id="28c41-p103">UPDATE does not generate a result set. Also, after you update records using an update query, you cannot undo the operation. If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span>
- <span data-ttu-id="28c41-p104">Mantenga copias de seguridad de los datos en todo momento. Si actualiza los registros equivocados, puede recuperarlos a partir de las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="28c41-p104">Maintain backup copies of your data at all times. If you update the wrong records, you can retrieve them from your backup copies.</span></span>



## <a name="example"></a><span data-ttu-id="28c41-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28c41-126">Example</span></span>

<span data-ttu-id="28c41-127">En este ejemplo, se cambian los valores del campo ReportsTo a 5 en todos los registros de empleados que tengan actualmente valores de 2 en el campo ReportsTo.</span><span class="sxs-lookup"><span data-stu-id="28c41-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

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
