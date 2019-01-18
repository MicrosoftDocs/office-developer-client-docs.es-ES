---
title: FilterCriterion (propiedad, RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707951"
---
# <a name="filtercriterion-property-rds"></a>FilterCriterion (propiedad, RDS)

**Se aplica a**: Access 2013, Office 2013

Indica el operador de evaluación que se utilizará en el valor de filtro.

## <a name="syntax"></a>Sintaxis

*DataControl*. FilterCriterion = *cadena*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Un valor de tipo **String** que especifica el operador de evaluación de [FilterValue](filtervalue-property-rds.md) a los registros. Puede ser uno de los siguientes: \<, \<=, \>, \>=, =, o \< \>.|

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un objeto **Recordset** actualizable.

La "\!=" operador no es válido para **FilterCriterion**; en su lugar, use "\<\>".

Si se establecen las propiedades de filtrado y ordenación y se llama al método **Reset**, el conjunto de filas primero se filtra y luego se ordena. En un orden ascendente, los valores nulos se encuentran en la parte superior, mientras que en un orden descendente están en la parte inferior (el orden ascendente es el comportamiento predeterminado).

