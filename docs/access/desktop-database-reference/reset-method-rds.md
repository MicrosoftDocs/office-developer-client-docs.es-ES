---
title: Método Reset (RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cebb2f464b63106545ff5b27b1722b6417b9dbe1
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949946"
---
# <a name="reset-method-rds"></a>Reset (método, RDS)

**Se aplica a**: Access 2013, Office 2013

Ordena o filtra un objeto **Recordset** de cliente según las propiedades de ordenación y filtro especificadas.

## <a name="syntax"></a>Sintaxis

*DataControl*. Reset (*valor*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*value* |Es opcional. Valor de tipo **Boolean** que es **True** (valor predeterminado) si se desea filtrar el conjunto de filas "filtrado" actual. El valor **False** indica que se va a filtrar el conjunto de filas original y que se quitan todas las opciones de filtro anteriores.|

## <a name="remarks"></a>Comentarios

Las propiedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtro en la caché de cliente. La funcionalidad de ordenación permite ordenar los registros por los valores de una columna. La funcionalidad de filtro permite mostrar un subconjunto de registros basándose en criterios de búsqueda, si bien el objeto [Recordset](recordset-object-ado.md) completo se mantiene en la caché. El método **Reset** ejecutará los criterios y reemplazará el actual objeto **Recordset** con un objeto **Recordset** actualizable.

Si se realizaron cambios en los datos originales que aún no se enviaron, el método **Reset** genera un error. Use primero el método [SubmitChanges](submitchanges-method-rds.md) para guardar los cambios en un objeto **Recordset** de lectura y escritura y, a continuación, use el método **Reset** para ordenar o filtrar los registros.

Si desea realizar más de un filtro en el conjunto de filas, puede utilizar el opcional argumento *booleano* con el método **Reset** . En el ejemplo siguiente se muestra cómo hacerlo:

