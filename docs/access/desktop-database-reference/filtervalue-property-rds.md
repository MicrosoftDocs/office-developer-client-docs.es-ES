---
title: FilterValue (propiedad, RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de54097c7992583851bbbd7b04c40f10fbca76e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949484"
---
# <a name="filtervalue-property-rds"></a>FilterValue (propiedad, RDS)

**Se aplica a**: Access 2013, Office 2013

Indica el valor mediante el que se van a filtrar registros.

## <a name="syntax"></a>Sintaxis

*DataControl*. FilterValue = *cadena*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Un valor de **tipo String** que representa un valor de datos con el que se va a filtrar registros (por ejemplo, 'Programmer' o 125).|

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtro en la caché de cliente. 

La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.

Los valores nulos dan lugar a un error de falta de coincidencia de tipos.

