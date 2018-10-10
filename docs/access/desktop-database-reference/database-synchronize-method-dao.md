---
title: Database.Synchronize Method (DAO)
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
ms.openlocfilehash: c55eab611cae8431a3ff3f2220cdfa8b1923d891
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485018"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Sincroniza dos réplicas (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Sincronizar (***DbPathName***, ***ExchangeType***)

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
<td><p>Ruta de acceso a la réplica de destino con la que la base de datos estará sincronizada.</p></td>
</tr>
<tr class="even">
<td><p>ExchangeType</p></td>
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
> <P>[!NOTA] No puede sincronizar réplicas parciales con otras réplicas parciales. Vea el método <STRONG><A href="database-populatepartial-method-dao.md">PopulatePartial</A></STRONG> para obtener más información.</P>


