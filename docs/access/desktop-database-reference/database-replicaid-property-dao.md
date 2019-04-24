---
title: Propiedad Database. ReplicaID (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294718"
---
# <a name="databasereplicaid-property-dao"></a>Propiedad Database. ReplicaID (DAO)


**Se aplica a:** Access 2013, Office 2013


Devuelve un valor de 16 bytes que identifica de forma exclusiva una réplica de base de datos (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . ReplicaID

*expresión* Variable que representa un objeto **Database** .

## <a name="remarks"></a>Comentarios

El valor devuelto es un valor **GUID** que identifica de forma exclusiva la réplica o el Diseño principal.

El motor de base de datos Microsoft Access genera de forma automática este valor cuando se crea una nueva réplica.

La propiedad **ReplicaID** de cada réplica, y del Diseño principal, se almacena en la tabla de sistema MSysReplicas.

## <a name="example"></a>Ejemplo

En este ejemplo se crea un réplica desde el Diseño principal de Neptuno.mdb y después se devuelve la **ReplicaID** de la réplica, que crea automáticamente el motor de base de datos Microsoft Access. (Si todavía no ha creado un Diseño principal de Neptuno, vea la propiedad **Replicable** o cambie el nombre de la base de datos en el código de un Diseño principal existente).

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

