---
title: Propiedad SortColumn (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306891"
---
# <a name="sortcolumn-property-rds"></a>Propiedad SortColumn (RDS)

**Se aplica a:** Access 2013, Office 2013

Indica la columna por la que se van a ordenar los registros.

## <a name="syntax"></a>Sintaxis

*DataControl*. SortColumn = *String*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Un valor de tipo **String** que representa el nombre o el alias de la columna mediante la que se ordenan los registros.|

## <a name="remarks"></a>Comentarios

Las propiedades **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) y [FilterColumn](filtercolumn-property-rds.md) proporcionan funciones de ordenación y filtrado en la memoria caché del cliente. La función de ordenación ordena los registros por los valores de una columna. La función de filtrado muestra un subconjunto de registros basado en criterios de búsqueda, mientras que se conserva el objeto completo [Recordset](recordset-object-ado.md) en la memoria caché. El método [Reset](reset-method-rds.md) ejecutará los criterios y sustituirá al objeto **Recordset** actual por un **Recordset** actualizable.

Para ordenar un objeto **Recordset**, en primer lugar se deben guardar los cambios pendientes. Si se usa **RDS.DataControl**, se puede usar el método [SubmitChanges](submitchanges-method-rds.md). Por ejemplo, si su **RDS. DataControl** se denomina ADC1, el código sería ADC1. SubmitChanges . Si se usa un objeto **Recordset** ADO, es posible usar su método [UpdateBatch](updatebatch-method-ado.md). **UpdateBatch** es el método recomendado para los objetos **Recordset** creados con el método [CreateRecordset](createrecordset-method-rds.md). Por ejemplo, el código puede ser myRS.UpdateBatch o . Si se usa un objeto **Recordset** ADO, es posible usar su método [UpdateBatch](updatebatch-method-ado.md). **UpdateBatch** es el método recomendado para los objetos **Recordset** creados con el método [CreateRecordset](createrecordset-method-rds.md). Por ejemplo, el código podría ser myRS.UpdateBatch o ADC1. Recordset.UpdateBatch .

