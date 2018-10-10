---
title: Database.DesignMasterID Property (DAO)
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
ms.openlocfilehash: 0bb2e369f886ba60fb425b9f1f2d10fdea0c1463
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485062"
---
# <a name="databasedesignmasterid-property-dao"></a>Database.DesignMasterID Property (DAO)

**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor de 16 bytes que identifica de forma única el Diseño principal de un conjunto de réplicas (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . DesignMasterID

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="remarks"></a>Observaciones

La propiedad **DesignMasterID** sólo se debe establecer si es necesario mover el Diseño principal actual. Al establecer esta propiedad, una réplica específica del conjunto de réplicas se convierte en el Diseño principal.

> [!NOTE]
> [!NOTA] No cree nunca un segundo Diseño principal en un conjunto de réplicas. La existencia de un segundo Diseño principal puede provocar la pérdida de datos.

En circunstancias extremas (por ejemplo, si se borra o daña el Diseño principal), puede establecer esta propiedad en la réplica actual. Sin embargo, al establecer esta propiedad en una réplica cuando ya hay otro Diseño principal en el conjunto se puede dividir el conjunto de réplicas en dos conjuntos irreconciliables e impedir la sincronización de los datos.

Si decide convertir una réplica en el nuevo Diseño principal del conjunto, sincronícela con todas las réplicas del conjunto de réplicas antes de establecer la propiedad **DesignMasterID** en la réplica. Para poder convertirla en el Diseño principal, la réplica debe estar abierta en modo exclusivo.

Si convierte una réplica designada como sólo lectura en el Diseño principal, se crea una réplica de destino de lectura y escritura; el antiguo Diseño principal sigue siendo también de lectura y escritura.

El valor de la propiedad **DesignMasterID** se almacena en la tabla del sistema MSysRepInfo.

## <a name="example"></a>Ejemplo

En este ejemplo, se establece la propiedad **DesignMasterID** en el valor de la propiedad **ReplicaID** de otra base de datos, convirtiendo dicha base de datos en el Diseño principal del conjunto de réplicas. Los diseños principales nuevo y antiguo se sincronizan para actualizar el cambio de diseño. Para que este código funcione, debe crear un Diseño principal y una réplica, incluir sus nombres y rutas de acceso según corresponda y ejecutar el código desde una base de datos distinta del Diseño principal nuevo o antiguo.

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

