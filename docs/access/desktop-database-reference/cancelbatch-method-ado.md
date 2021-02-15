---
title: Método CancelBatch (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 832b367824fd8043486ff85f63739c3288696774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296643"
---
# <a name="cancelbatch-method-ado"></a>Método CancelBatch (ADO)

**Se aplica a:** Access 2013, Office 2013

Cancela una actualización por lotes que está pendiente.

## <a name="syntax"></a>Sintaxis

*recordset*. CancelBatch *AffectRecords*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*AffectRecords* |Es opcional. Valor de [AffectEnum](affectenum.md) que indica el número de registros afectados por el método **CancelBatch**. |

## <a name="remarks"></a>Comentarios

Use el método **CancelBatch** para cancelar cualquier actualización pendiente en un objeto [Recordset](recordset-object-ado.md) en modo de actualización por lotes. Si el objeto **Recordset** está en modo de actualización inmediata y se llama a **CancelBatch** sin **adAffectCurrent**, se generará un error.

Si está modificando el registro actual o agregando un registro nuevo cuando llama a **CancelBatch**, ADO llamará primero al método [CancelUpdate](cancelupdate-method-ado.md) para cancelar los cambios almacenados en caché. A continuación, se cancelarán todos los cambios pendientes en el objeto **Recordset**.

Es posible que el registro actual sea indeterminable después de llamar a **CancelBatch**, sobre todo si se estaba agregando un registro nuevo. Por este motivo, se recomienda establecer la posición del registro actual en una ubicación conocida en el objeto **Recordset** después de la llamada a **CancelBatch**, llamando, por ejemplo al método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

Si un intento de cancelar las actualizaciones pendientes genera un error debido a un conflicto con los datos subyacentes (por ejemplo, otro usuario ha eliminado un registro), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) pero no detiene la ejecución del programa. Se produce un error en tiempo de ejecución sólo si hay conflictos en todos los registros solicitados. Utilice la propiedad [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) y la propiedad [Status](status-property-ado-recordset.md) para localizar los registros con conflictos.

