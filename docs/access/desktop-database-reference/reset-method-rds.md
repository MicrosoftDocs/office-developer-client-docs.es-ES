---
title: 'Método Reset (RDS: referencia de base de datos de escritorio de Access)'
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306646"
---
# <a name="reset-method-rds"></a>Método Reset (RDS)

**Se aplica a:** Access 2013, Office 2013

Ordena o filtra un objeto **Recordset** de cliente según las propiedades de ordenación y filtro especificadas.

## <a name="syntax"></a>Sintaxis

*DataControl*. Reset(*value*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*value* |Es opcional. Valor de tipo **Boolean** que es **True** (valor predeterminado) si se desea filtrar el conjunto de filas "filtrado" actual. El valor **False** indica que se va a filtrar el conjunto de filas original y que se quitan todas las opciones de filtro anteriores.|

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtro en la caché de cliente. La funcionalidad de ordenación permite ordenar los registros por los valores de una columna. La funcionalidad de filtro permite mostrar un subconjunto de registros basándose en criterios de búsqueda, si bien el objeto [Recordset](recordset-object-ado.md) completo se mantiene en la caché. El método **Reset** ejecutará los criterios y reemplazará el actual objeto **Recordset** con un objeto **Recordset** actualizable.

Si se realizaron cambios en los datos originales que aún no se enviaron, el método **Reset** genera un error. Use primero el método [SubmitChanges](submitchanges-method-rds.md) para guardar los cambios en un objeto **Recordset** de lectura y escritura y, a continuación, use el método **Reset** para ordenar o filtrar los registros.

Si desea aplicar más de un filtro a un conjunto de filas, puede utilizar el argumento *booleano* opcional con el método **Reset**. En el ejemplo siguiente se muestra cómo hacerlo:

