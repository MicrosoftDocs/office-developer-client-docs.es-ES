---
title: Propiedad Relation.PartialReplica (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fef48902b806f13947ae4b81728af4c5704c2b8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307017"
---
# <a name="relationpartialreplica-property-dao"></a>Propiedad Relation.PartialReplica (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor en un objeto **Relation** que indica si esa relación se debería tener en cuenta al rellenar una réplica parcial desde una réplica completa. (Sólo para base de datos del motor de base de datos Microsoft Access). **Boolean** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . PartialReplica

*expresión* Expresión que devuelve un **objeto Relation** .

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un tipo de datos Boolean que es **True** cuando se debe obligar la relación durante la sincronización.

Esta propiedad le permite replicar datos desde una réplica completa a una réplica parcial a partir de relaciones entre tablas. Puede utilizar la propiedad **PartialReplica** cuando al establecer únicamente la propiedad **ReplicaFilter** no se puedan especificar adecuadamente los datos que deben replicarse para la parcial. Por ejemplo, suponga que tiene una base de datos en la que la tabla Clientes presenta una relación de uno a varios con la tabla Pedidos, y desea configurar una réplica parcial que sólo replique los pedidos de los clientes de la región de California (en vez de todos los pedidos). No será posible establecer la propiedad **ReplicaFilter** en la tabla Pedidos en Region = 'CA' porque el campo Región se encuentra en la tabla Clientes y no en la tabla Pedidos.

Para replicar todos los pedidos desde la región de California, debe indicar que la relación entre las tablas Pedidos y Clientes se activará durante la replicación. Una vez que haya creado una réplica parcial, los siguientes pasos la rellenarán con todos los pedidos realizados desde la región de California:

1.  Establezca la **propiedad ReplicaFilter** en el **objeto TableDef** customers en "Region = 'CA'".

2.  Establezca el valor de la propiedad **PartialReplica** en **True** en el objeto **Relation** que corresponde a la relación entre Pedidos y Clientes.

3.  Llame al método **PopulatePartial**.
    

> [!NOTE]
> [!NOTA] Al establecer un filtro de réplica o una relación de réplica, tenga en cuenta que los registros de la réplica parcial que no cumplen los criterios de restricción se quitarán de la réplica parcial, pero no de la réplica completa. Por ejemplo, suponga que establece la propiedad **ReplicaFilter** en el objeto Clientes **TableDef** en la réplica parcial en "Region = 'CA'" y que después vuelve a rellenar la base de datos. Esto insertará o actualizará todos los registros de los clientes de California. 
> 
> Si después restablece la propiedad **ReplicaFilter** en "Region = 'FL'" y vuelve a rellenar la base de datos, todos los registros de la región California en la réplica parcial se quitarán y todos los registros de los clientes de Florida se insertarán desde la réplica completa. No se eliminarán los registros en la réplica completa. 
>
> Antes de establecer la propiedad **ReplicaFilter** o la propiedad **PartialReplica**, se recomienda sincronizar la réplica parcial en la que está estableciendo estas propiedades con la réplica completa. Con ello, se asegurará de que los cambios pendientes en la réplica parcial se combinarán en la replica completa antes de quitar cualquier registro de la réplica parcial.


