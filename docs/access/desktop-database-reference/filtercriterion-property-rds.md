---
title: Propiedad FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292429"
---
# <a name="filtercriterion-property-rds"></a>Propiedad FilterCriterion (RDS)

**Se aplica a:** Access 2013, Office 2013

Indica el operador de evaluación que se utilizará en el valor de filtro.

## <a name="syntax"></a>Sintaxis

*DataControl*. FilterCriterion = *String*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Un valor de tipo **String** que especifica el operador de evaluación de [FilterValue](filtervalue-property-rds.md) a los registros. Puede ser cualquiera de los siguientes: \< , \< =, \> , \> =, =, o \< \> .|

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un **Recordset** actualizable.

El operador " \! =" no es válido para **FilterCriterion;** en su lugar, use " \< \> ".

Si se establecen las propiedades de filtrado y ordenación y se llama al método **Reset**, el conjunto de filas primero se filtra y luego se ordena. En un orden ascendente, los valores nulos se encuentran en la parte superior, mientras que en un orden descendente están en la parte inferior (el orden ascendente es el comportamiento predeterminado).

