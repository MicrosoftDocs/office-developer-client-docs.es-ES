---
title: s WillChangeRecord y RecordChangeComplete (evento, ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 895a80cf4810088b5f18f4a9416e7eadc54a004f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878132"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>s WillChangeRecord y RecordChangeComplete (evento, ADO)


**Se aplica a**: Access 2013, Office 2013


El evento **WillChangeRecord** se usa (recibe una llamada) antes de cualquier cambio en uno o más registros (filas) del objeto [Recordset](recordset-object-ado.md). El evento **RecordChangeComplete** recibe una llamada después de cualquier cambio en uno o más registros.

## <a name="syntax"></a>Sintaxis

WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*

RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

  - *adReason*

  - Valor [EventReasonEnum](eventreasonenum.md) que especifica el motivo para este evento. El valor puede ser **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, ** adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** o **adRsnFirstChange**.

  - *cRecords*

  - Valor **Long** que indica el número de registros cambiados (afectados).

  - *pError*

  - Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Cuando se realiza una llamada a **WillChangeRecord**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar cancelación de la operación pendiente.
    
    Cuando se llama a **RecordChangeComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación.
    
    Antes de que **WillChangeRecord** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación que causó este evento, o en adStatusUnwantedEvent para impedir notificaciones posteriores.
    
    Antes de que **RecordChangeComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.

  - *Connection*

  - Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.

## <a name="remarks"></a>Comentarios

Un evento **WillChangeRecord** o **RecordChangeComplete** se puede producir para el primer campo cambiados de una fila debido a las operaciones del objeto **Recordset** siguientes: [ Update ](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) y [CancelBatch](cancelbatch-method-ado.md). El valor de [CursorType](cursortype-property-ado.md) del **Recordset** determina qué operaciones hacen que se producen los eventos.

Durante el evento **WillChangeRecord** , la propiedad de [filtro](filter-property-ado.md) de **conjunto de registros** se establece en **adFilterAffectedRecords**. No es posible cambiar esta propiedad mientras se procesa el evento.

Deberá establecer el parámetro adStatus en adStatusUnwantedEvent para cada valor posible de adReason con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro adReason.

