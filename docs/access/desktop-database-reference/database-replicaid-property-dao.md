---
title: Propiedad Database.ReplicaID (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3214f093b90576483df4d6f63cf1ad62b3530931
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918768"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="84041-102">Propiedad Database.ReplicaID (DAO)</span><span class="sxs-lookup"><span data-stu-id="84041-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="84041-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84041-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="84041-104">Devuelve un valor de 16 bytes que identifica de forma exclusiva una réplica de base de datos (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="84041-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="84041-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84041-105">Syntax</span></span>

<span data-ttu-id="84041-106">*expresión* . ReplicaID</span><span class="sxs-lookup"><span data-stu-id="84041-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="84041-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="84041-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="84041-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84041-108">Remarks</span></span>

<span data-ttu-id="84041-109">El valor devuelto es un valor **GUID** que identifica de forma exclusiva la réplica o el Diseño principal.</span><span class="sxs-lookup"><span data-stu-id="84041-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="84041-110">El motor de base de datos Microsoft Access genera de forma automática este valor cuando se crea una nueva réplica.</span><span class="sxs-lookup"><span data-stu-id="84041-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="84041-111">La propiedad **ReplicaID** de cada réplica, y del Diseño principal, se almacena en la tabla de sistema MSysReplicas.</span><span class="sxs-lookup"><span data-stu-id="84041-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="84041-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84041-112">Example</span></span>

<span data-ttu-id="84041-p101">En este ejemplo se crea un réplica desde el Diseño principal de Neptuno.mdb y después se devuelve la **ReplicaID** de la réplica, que crea automáticamente el motor de base de datos Microsoft Access. (Si todavía no ha creado un Diseño principal de Neptuno, vea la propiedad **Replicable** o cambie el nombre de la base de datos en el código de un Diseño principal existente).</span><span class="sxs-lookup"><span data-stu-id="84041-p101">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

