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
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="53c0b-102">Propiedad Relation.PartialReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="53c0b-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="53c0b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53c0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53c0b-p101">Establece o devuelve un valor en un objeto **Relation** que indica si esa relación se debería tener en cuenta al rellenar una réplica parcial desde una réplica completa. (Sólo para base de datos del motor de base de datos Microsoft Access). **Boolean** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="53c0b-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c0b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53c0b-107">Syntax</span></span>

<span data-ttu-id="53c0b-108">*expresión* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="53c0b-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="53c0b-109">*expresión* Expresión que devuelve un **objeto Relation** .</span><span class="sxs-lookup"><span data-stu-id="53c0b-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c0b-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53c0b-110">Remarks</span></span>

<span data-ttu-id="53c0b-111">La configuración o el valor devuelto es un tipo de datos Boolean que es **True** cuando se debe obligar la relación durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="53c0b-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="53c0b-112">Esta propiedad le permite replicar datos desde una réplica completa a una réplica parcial a partir de relaciones entre tablas.</span><span class="sxs-lookup"><span data-stu-id="53c0b-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="53c0b-113">Puede utilizar la propiedad **PartialReplica** cuando al establecer únicamente la propiedad **ReplicaFilter** no se puedan especificar adecuadamente los datos que deben replicarse para la parcial.</span><span class="sxs-lookup"><span data-stu-id="53c0b-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="53c0b-114">Por ejemplo, suponga que tiene una base de datos en la que la tabla Clientes presenta una relación de uno a varios con la tabla Pedidos, y desea configurar una réplica parcial que sólo replique los pedidos de los clientes de la región de California (en vez de todos los pedidos).</span><span class="sxs-lookup"><span data-stu-id="53c0b-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="53c0b-115">No será posible establecer la propiedad **ReplicaFilter** en la tabla Pedidos en Region = 'CA' porque el campo Región se encuentra en la tabla Clientes y no en la tabla Pedidos.</span><span class="sxs-lookup"><span data-stu-id="53c0b-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="53c0b-p103">Para replicar todos los pedidos desde la región de California, debe indicar que la relación entre las tablas Pedidos y Clientes se activará durante la replicación. Una vez que haya creado una réplica parcial, los siguientes pasos la rellenarán con todos los pedidos realizados desde la región de California:</span><span class="sxs-lookup"><span data-stu-id="53c0b-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="53c0b-118">Establezca la **propiedad ReplicaFilter** en el **objeto TableDef** customers en "Region = 'CA'".</span><span class="sxs-lookup"><span data-stu-id="53c0b-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="53c0b-119">Establezca el valor de la propiedad **PartialReplica** en **True** en el objeto **Relation** que corresponde a la relación entre Pedidos y Clientes.</span><span class="sxs-lookup"><span data-stu-id="53c0b-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="53c0b-120">Llame al método **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="53c0b-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="53c0b-121">[!NOTA] Al establecer un filtro de réplica o una relación de réplica, tenga en cuenta que los registros de la réplica parcial que no cumplen los criterios de restricción se quitarán de la réplica parcial, pero no de la réplica completa.</span><span class="sxs-lookup"><span data-stu-id="53c0b-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="53c0b-122">Por ejemplo, suponga que establece la propiedad **ReplicaFilter** en el objeto Clientes **TableDef** en la réplica parcial en "Region = 'CA'" y que después vuelve a rellenar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="53c0b-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="53c0b-123">Esto insertará o actualizará todos los registros de los clientes de California.</span><span class="sxs-lookup"><span data-stu-id="53c0b-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="53c0b-124">Si después restablece la propiedad **ReplicaFilter** en "Region = 'FL'" y vuelve a rellenar la base de datos, todos los registros de la región California en la réplica parcial se quitarán y todos los registros de los clientes de Florida se insertarán desde la réplica completa.</span><span class="sxs-lookup"><span data-stu-id="53c0b-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="53c0b-125">No se eliminarán los registros en la réplica completa.</span><span class="sxs-lookup"><span data-stu-id="53c0b-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="53c0b-126">Antes de establecer la propiedad **ReplicaFilter** o la propiedad **PartialReplica**, se recomienda sincronizar la réplica parcial en la que está estableciendo estas propiedades con la réplica completa.</span><span class="sxs-lookup"><span data-stu-id="53c0b-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="53c0b-127">Con ello, se asegurará de que los cambios pendientes en la réplica parcial se combinarán en la replica completa antes de quitar cualquier registro de la réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="53c0b-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>


