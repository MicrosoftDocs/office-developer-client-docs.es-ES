---
title: Método Database. Synchronize (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294711"
---
# <a name="databasesynchronize-method-dao"></a>Método Database. Synchronize (DAO)


**Se aplica a:** Access 2013, Office 2013

Sincroniza dos réplicas (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Synchronize (***DbPathName***, ***ExchangeType***)

*expresión* Variable que representa un objeto **Database** .

## <a name="parameters"></a>Parameters

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
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ruta de acceso a la réplica de destino con la que la base de datos estará sincronizada.</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="synchronizetypeenum-enumeration-dao.md">synchronizetypeenum (</a></strong> que indica la dirección en la que se van a sincronizar los cambios entre las dos bases de datos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Utilice **Synchronize** para intercambiar datos y cambios de diseño entre dos bases de datos. Los cambios de diseño siempre se ejecutan primero. Ambas bases de datos deben estar en el mismo nivel de diseño antes de que puedan intercambiar datos. Por ejemplo, un intercambio de tipo **dbRepExportChanges** podría causar cambios de diseño en una réplica, aunque los cambios de datos fluyen solo desde la base de datos a DbPathName.

La réplica identificada en DbPathName debe formar parte del mismo conjunto de réplicas. Si ambas réplicas tienen el mismo valor de la propiedad **ReplicaID** o son Diseños principales para dos conjuntos de réplicas distintos, la sincronización produce un error.

Al sincronizar dos réplicas a través de Internet, debe utilizar la constante **dbRepSyncInternet**. En este caso, especifique una dirección URL (Uniform Resource Locator) para el argumento DbPathName en lugar de especificar una ruta de acceso a la red de área local.


> [!NOTE]
> [!NOTA] No puede sincronizar réplicas parciales con otras réplicas parciales. Vea el método [PopulatePartial](database-populatepartial-method-dao.md) para obtener más información.


