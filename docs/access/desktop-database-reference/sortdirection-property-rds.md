---
title: SortDirection (propiedad, RDS)
TOCTitle: SortDirection Property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 256e6a878e9c3f382bcd65b9138df7a440bf118c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486083"
---
# <a name="sortdirection-property-rds"></a>SortDirection (propiedad, RDS)


**Se aplica a**: Access 2013 | Office 2013


Indica si un criterio de ordenación es ascendente o descendente.

## <a name="syntax"></a>Sintaxis

*DataControl*. SortDirection = *valor*

## <a name="parameters"></a>Parámetros

  - *DataControl*

  - Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *Valor*

  - Un valor de tipo **Boolean** que, si está establecido en **True**, indica que el orden es ascendente. **False** indica un orden descendente.

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método **Reset** ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.

