---
title: Propiedad TableDef.ReplicaFilter (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ba296701faebb32696741a742b7fe01660b74c46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302789"
---
# <a name="tabledefreplicafilter-property-dao"></a>Propiedad TableDef.ReplicaFilter (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor en un objeto **[TableDef](tabledef-object-dao.md)** dentro de una réplica parcial que indica el subconjunto de registros que se replica a esa tabla desde una réplica completa. (Sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . ReplicaFilter

*expression* Variable que representa un objeto **TableDef**.

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un **String** o **Boolean** que indica el subconjunto de registros que se replica, como se especifica en la siguiente tabla:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Una cadena</p></td>
<td><p>Criterios que un registro de la réplica parcial debe satisfacer para replicarse desde una réplica completa.</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>Replica todos los registros.</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(Valor predeterminado) no replica ningún registro.</p></td>
</tr>
</tbody>
</table>


Esta propiedad es similar a una cláusula SQL WHERE (sin la palabra WHERE), pero no se pueden especificar subconsultas, funciones de agregado (como **Count**) o funciones definidas por el usuarios dentro del criterio.

Solo se pueden sincronizar datos entre una réplica completa y una réplica parcial. No se pueden sincronizar datos entre dos réplicas parciales. Además, con la réplica parcial se pueden establecer restricciones que indiquen los registros que se replican, pero no se pueden indicar los campos replicados.

Generalmente, se restablece un filtro de réplica cuando se desea replicar un conjunto de registros distinto. Por ejemplo, cuando un representante de ventas se hace cargo temporalmente de la región de otro representante de ventas, la aplicación de la base de datos puede replicar temporalmente datos de ambas regiones y, a continuación, volver al filtro anterior. En este caso, la aplicación restablece la propiedad **ReplicaFilter** y después vuelve a llenar la réplica parcial.

Si su aplicación cambia los filtros de réplica, debería seguir los pasos que se indican a continuación:

1.  Utilice el método **[Synchronize](database-synchronize-method-dao.md)** para sincronizar su réplica completa con la réplica parcial en la que se han cambiado los filtros.

2.  Utilice la propiedad **ReplicaFilter** para realizar los cambios que desee en el filtro de réplica.

3.  Utilice el método **[PopulatePartial](database-populatepartial-method-dao.md)** para quitar todos los registros de la réplica parcial y transferir todos los registros desde la réplica completa que cumplen los nuevos criterios de filtro de réplica.

Para quitar un filtro, establezca la propiedad **ReplicaFilter** en **False**. Si quita todos los filtros y llama al método **PopulatePartial**, no aparecerá ningún registro en ninguna tabla replicada de la réplica parcial.

> [!NOTE]
> [!NOTA] Si un filtro de réplica cambia y se llama al método **Synchronize** sin haber llamado primero a **PopulatePartial**, se producirá un error capturable.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo se utiliza la propiedad **ReplicaFilter** para replicar sólo los registros de los clientes de la región de California.

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

