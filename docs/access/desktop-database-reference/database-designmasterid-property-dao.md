---
title: Propiedad Database.DesignMasterID (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1d15cc036b33e2b64f54b89f4f8ed5c69d9fdcbe
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930493"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="f102d-102">Propiedad Database.DesignMasterID (DAO)</span><span class="sxs-lookup"><span data-stu-id="f102d-102">Database.DesignMasterID property (DAO)</span></span>

<span data-ttu-id="f102d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f102d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f102d-104">Establece o devuelve un valor de 16 bytes que identifica de forma única el Diseño principal de un conjunto de réplicas (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f102d-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f102d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f102d-105">Syntax</span></span>

<span data-ttu-id="f102d-106">*expresión* . DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="f102d-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="f102d-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="f102d-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f102d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f102d-108">Remarks</span></span>

<span data-ttu-id="f102d-p101">La propiedad **DesignMasterID** sólo se debe establecer si es necesario mover el Diseño principal actual. Al establecer esta propiedad, una réplica específica del conjunto de réplicas se convierte en el Diseño principal.</span><span class="sxs-lookup"><span data-stu-id="f102d-p101">You should set the **DesignMasterID** property only if you need to move the current Design Master. Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="f102d-p102">[!NOTA] No cree nunca un segundo Diseño principal en un conjunto de réplicas. La existencia de un segundo Diseño principal puede provocar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="f102d-p102">Never create a second Design Master in a replica set. The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="f102d-p103">En circunstancias extremas (por ejemplo, si se borra o daña el Diseño principal), puede establecer esta propiedad en la réplica actual. Sin embargo, al establecer esta propiedad en una réplica cuando ya hay otro Diseño principal en el conjunto se puede dividir el conjunto de réplicas en dos conjuntos irreconciliables e impedir la sincronización de los datos.</span><span class="sxs-lookup"><span data-stu-id="f102d-p103">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica. However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="f102d-p104">Si decide convertir una réplica en el nuevo Diseño principal del conjunto, sincronícela con todas las réplicas del conjunto de réplicas antes de establecer la propiedad **DesignMasterID** en la réplica. Para poder convertirla en el Diseño principal, la réplica debe estar abierta en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f102d-p104">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica. The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="f102d-117">Si convierte una réplica designada como sólo lectura en el Diseño principal, se crea una réplica de destino de lectura y escritura; el antiguo Diseño principal sigue siendo también de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f102d-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="f102d-118">El valor de la propiedad **DesignMasterID** se almacena en la tabla del sistema MSysRepInfo.</span><span class="sxs-lookup"><span data-stu-id="f102d-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="f102d-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f102d-119">Example</span></span>

<span data-ttu-id="f102d-p105">En este ejemplo, se establece la propiedad **DesignMasterID** en el valor de la propiedad **ReplicaID** de otra base de datos, convirtiendo dicha base de datos en el Diseño principal del conjunto de réplicas. Los diseños principales nuevo y antiguo se sincronizan para actualizar el cambio de diseño. Para que este código funcione, debe crear un Diseño principal y una réplica, incluir sus nombres y rutas de acceso según corresponda y ejecutar el código desde una base de datos distinta del Diseño principal nuevo o antiguo.</span><span class="sxs-lookup"><span data-stu-id="f102d-p105">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set. The old and new Design Masters are synchronized to update the design change. For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

