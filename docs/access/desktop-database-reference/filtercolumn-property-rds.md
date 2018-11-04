---
title: FilterColumn (propiedad, RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1af06abc634d0ef1984d325722aac814214b28d
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949465"
---
# <a name="filtercolumn-property-rds"></a>FilterColumn (propiedad, RDS)

**Se aplica a**: Access 2013, Office 2013

Indica la columna en la que evaluar los criterios de filtro.

## <a name="syntax"></a>Sintaxis

*DataControl*. FilterColumn = *cadena*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Un valor de tipo **String** que especifica la columna en la que evaluar los criterios de filtro. Los criterios de filtro se especifican en la propiedad [FilterCriterion](filtercriterion-property-rds.md).|

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y **FilterColumn** proporcionan funciones de ordenación y filtro en la caché de cliente. 

La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. 

El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.

