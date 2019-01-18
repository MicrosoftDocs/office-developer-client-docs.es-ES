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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722434"
---
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="61fd8-102">Propiedad TableDef.ReplicaFilter (DAO)</span><span class="sxs-lookup"><span data-stu-id="61fd8-102">TableDef.ReplicaFilter property (DAO)</span></span>

<span data-ttu-id="61fd8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61fd8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61fd8-p101">Establece o devuelve un valor en un objeto **[TableDef](tabledef-object-dao.md)** dentro de una réplica parcial que indica el subconjunto de registros que se replica a esa tabla desde una réplica completa. (Sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="61fd8-p101">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="61fd8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61fd8-106">Syntax</span></span>

<span data-ttu-id="61fd8-107">*expresión* . ReplicaFilter</span><span class="sxs-lookup"><span data-stu-id="61fd8-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="61fd8-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="61fd8-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61fd8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61fd8-109">Remarks</span></span>

<span data-ttu-id="61fd8-110">La configuración o el valor devuelto es un **String** o **Boolean** que indica el subconjunto de registros que se replica, como se especifica en la siguiente tabla:</span><span class="sxs-lookup"><span data-stu-id="61fd8-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61fd8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="61fd8-111">Value</span></span></p></th>
<th><p><span data-ttu-id="61fd8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="61fd8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61fd8-113">Una cadena</span><span class="sxs-lookup"><span data-stu-id="61fd8-113">A string</span></span></p></td>
<td><p><span data-ttu-id="61fd8-114">Criterios que un registro de la réplica parcial debe satisfacer para replicarse desde una réplica completa.</span><span class="sxs-lookup"><span data-stu-id="61fd8-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61fd8-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="61fd8-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="61fd8-116">Replica todos los registros.</span><span class="sxs-lookup"><span data-stu-id="61fd8-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61fd8-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="61fd8-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="61fd8-118">(Valor predeterminado) no replica ningún registro.</span><span class="sxs-lookup"><span data-stu-id="61fd8-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61fd8-119">Esta propiedad es similar a una cláusula SQL WHERE (sin la palabra WHERE), pero no se pueden especificar subconsultas, funciones de agregado (como **Count**) o funciones definidas por el usuarios dentro del criterio.</span><span class="sxs-lookup"><span data-stu-id="61fd8-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="61fd8-p102">Solo se pueden sincronizar datos entre una réplica completa y una réplica parcial. No se pueden sincronizar datos entre dos réplicas parciales. Además, con la réplica parcial se pueden establecer restricciones que indiquen los registros que se replican, pero no se pueden indicar los campos replicados.</span><span class="sxs-lookup"><span data-stu-id="61fd8-p102">You can only synchronize data between a full replica and a partial replica. You can't synchronize data between two partial replicas. Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="61fd8-p103">Generalmente, se restablece un filtro de réplica cuando se desea replicar un conjunto de registros distinto. Por ejemplo, cuando un representante de ventas se hace cargo temporalmente de la región de otro representante de ventas, la aplicación de la base de datos puede replicar temporalmente datos de ambas regiones y, a continuación, volver al filtro anterior. En este caso, la aplicación restablece la propiedad **ReplicaFilter** y después vuelve a llenar la réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="61fd8-p103">Usually, you reset a replica filter when you want to replicate a different set of records. For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter. In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="61fd8-126">Si su aplicación cambia los filtros de réplica, debería seguir los pasos que se indican a continuación:</span><span class="sxs-lookup"><span data-stu-id="61fd8-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="61fd8-127">Utilice el método **[Synchronize](database-synchronize-method-dao.md)** para sincronizar su réplica completa con la réplica parcial en la que se han cambiado los filtros.</span><span class="sxs-lookup"><span data-stu-id="61fd8-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="61fd8-128">Utilice la propiedad **ReplicaFilter** para realizar los cambios que desee en el filtro de réplica.</span><span class="sxs-lookup"><span data-stu-id="61fd8-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="61fd8-129">Utilice el método **[PopulatePartial](database-populatepartial-method-dao.md)** para quitar todos los registros de la réplica parcial y transferir todos los registros desde la réplica completa que cumplen los nuevos criterios de filtro de réplica.</span><span class="sxs-lookup"><span data-stu-id="61fd8-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="61fd8-p104">Para quitar un filtro, establezca la propiedad **ReplicaFilter** en **False**. Si quita todos los filtros y llama al método **PopulatePartial**, no aparecerá ningún registro en ninguna tabla replicada de la réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="61fd8-p104">To remove a filter, set the **ReplicaFilter** property to **False**. If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>

> [!NOTE]
> <span data-ttu-id="61fd8-132">[!NOTA] Si un filtro de réplica cambia y se llama al método **Synchronize** sin haber llamado primero a **PopulatePartial**, se producirá un error capturable.</span><span class="sxs-lookup"><span data-stu-id="61fd8-132">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="61fd8-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61fd8-133">Example</span></span>

<span data-ttu-id="61fd8-134">En el siguiente ejemplo se utiliza la propiedad **ReplicaFilter** para replicar sólo los registros de los clientes de la región de California.</span><span class="sxs-lookup"><span data-stu-id="61fd8-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

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

