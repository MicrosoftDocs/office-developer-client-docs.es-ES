---
title: Database.PopulatePartial Method (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed8125d89691045a24ecc438d490146a8a3942b5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883018"
---
# <a name="databasepopulatepartial-method-dao"></a>Database.PopulatePartial Method (DAO)


**Se aplica a**: Access 2013, Office 2013


Sincroniza cualquier cambio en una réplica parcial con la réplica completa, desactiva todos los registros en la réplica parcial y, a continuación, vuelve a llenar la réplica parcial en función de los filtros de la réplica activa. (Solo bases de datos del motor de base de datos de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . PopulatePartial (***DbPathName***)

*expresión* Variable que representa un objeto de **base de datos** .

### <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DbPathName</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ruta y nombre de la réplica completa a partir de la cual se llenan los registros.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Al sincronizar una réplica parcial con una réplica completa, es posible crear registros "huérfanos" en la réplica parcial. Por ejemplo, suponga que tiene una tabla de clientes con **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** establecido en "región = 'CA'". Si un usuario cambia una región de cliente de CA a NY en la réplica parcial y luego se produce una sincronización a través del método **[Synchronize](database-synchronize-method-dao.md)**, el cambio se propaga a la réplica completa pero el registro que contiene NY en la réplica parcial está huérfano porque ya no cumple los criterios de filtro de la réplica.

Para resolver el problema de los registros huérfanos, puede utilizar el método **PopulatePartial**. El método **PopulatePartial** es similar al método **Synchronize** pero sincroniza cualquier cambio con la réplica completa, elimina todos los registros en la réplica parcial y luego rellena dicha réplica basándose en los filtros de la réplica activa. Incluso si los filtros de la réplica no han cambiado, **PopulatePartial** borrará siempre todos los registros de la réplica parcial y la rellenará basándose en los filtros activos.

En general, debe utilizar el método **PopulatePartial** cuando crea una réplica parcial y siempre que cambie los filtros de la réplica. Si la aplicación cambia los filtros de la réplica, debe seguir estos pasos:

1.  Sincronice la réplica completa con la réplica parcial en la que se están cambiando los filtros.

2.  Utilice las propiedades **ReplicaFilter** y **[PartialReplica](relation-partialreplica-property-dao.md)** para hacer los cambios que desee en el filtro de réplica.

3.  Llame al método **PopulatePartial** para eliminar todos los registros de la réplica parcial y transferir los registros desde la réplica completa que cumplen los criterios del nuevo filtro de réplica.

Si se cambia un filtro de réplica y se abre el método **Synchronize** sin abrir primero **PopulatePartial**, se produce un error capturable.

El método **PopulatePartial** sólo se puede abrir en una réplica parcial que se haya abierto para un acceso exclusivo. Además, no puede llamar al método **PopulatePartial** desde un código que se ejecuta en la misma réplica parcial. En su lugar, abra la réplica parcial de forma exclusiva desde la réplica completa u otra base de datos y llame luego a **PopulatePartial**.


> [!NOTE]
> [!NOTA] Aunque **PopulatePartial** realiza una sincronización de sentido único antes de borrar y rellenar la réplica parcial, resulta recomendable llamar a **Synchronize** antes de a **PopulatePartial**. Esto se debe a que si ocurre un error en la llamada a **Synchronize**, se produce un error capturable. Puede utilizar este error para decidir si prosigue o no con el método **PopulatePartial** (que elimina todos los registros de la réplica parcial). Si **PopulatePartial** se llama a sí mismo y se produce un error mientras se sincronizan los registros, se borrarán los registros de la réplica parcial, lo que quizá no sea el resultado esperado.



## <a name="example"></a>Ejemplo

En el ejemplo siguiente se utiliza el método **PopulatePartial** después de cambiar un filtro de réplica.

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

