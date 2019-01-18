---
title: Database.Synchronize (método) (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709890"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize (método) (DAO)


**Se aplica a**: Access 2013, Office 2013

Sincroniza dos réplicas (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Sincronizar (***DbPathName***, ***ExchangeType***)

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="parameters"></a>Parámetros

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
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>Ruta de acceso a la réplica de destino con la que la base de datos estará sincronizada.</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> que indica la dirección para sincronizar los cambios entre las dos bases de datos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Utilice **Synchronize** para intercambiar datos y cambios de diseño entre dos bases de datos. Los cambios de diseño siempre se ejecutan primero. Ambas bases de datos deben estar en el mismo nivel de diseño antes de que puedan intercambiar datos. Por ejemplo, un intercambio de tipo **dbRepExportChanges** puede provocar cambios de diseño en una réplica incluso aunque los cambios de datos flujo sólo desde la base de datos a DbPathName.

La réplica identificada en DbPathName debe formar parte del mismo conjunto de réplicas. Si ambas réplicas tienen el mismo valor de la propiedad **ReplicaID** o son Diseños principales para dos conjuntos de réplicas distintos, la sincronización produce un error.

Al sincronizar dos réplicas a través de Internet, debe utilizar la constante **dbRepSyncInternet**. En este caso, especifique una dirección de localizador de recursos uniforme (URL) para el argumento DbPathName en lugar de especificar una ruta de acceso de red de área local.


> [!NOTE]
> [!NOTA] No puede sincronizar réplicas parciales con otras réplicas parciales. Vea el método [PopulatePartial](database-populatepartial-method-dao.md) para obtener más información.


