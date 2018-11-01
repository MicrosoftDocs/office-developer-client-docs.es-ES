---
title: WillChangeRecordset y RecordsetChangeComplete (evento, ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a7bf9a69fd5a648efc86f698e82ca0ba9413a30
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886315"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>WillChangeRecordset y RecordsetChangeComplete (evento, ADO)


**Se aplica a**: Access 2013, Office 2013


Al evento **WillChangeRecordset** se le llama antes de que una operación pendiente cambie el [Recordset](recordset-object-ado.md). Al evento **RecordsetChangeComplete** se le llama después de que el objeto **Recordset** haya cambiado.

## <a name="syntax"></a>Sintaxis

WillChangeRecordset*adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

  - *adReason*

  - Valor [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnRequery**, **adRsnResynch**, **adRsnClose** o ** adRsnOpen**.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Cuando se llama a **WillChangeRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente.
    
    Cuando se llama a **RecordsetChangeComplete**, este parámetro se establece en ** adStatusOK** si la operación que provocó el evento se realizó correctamente, en **adStatusErrorsOccurred** si se produjo un error en la operación o en **adStatusCancel** si se ha cancelado la operación asociada al evento **WillChangeRecordset** anteriormente aceptado.
    
    Antes de que **WillChangeRecordset** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores.
    
    Antes de que **WillChangeRecordset** o **RecordsetChangeComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.

  - *pError*

  - Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.

  - *Connection*

  - Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.

## <a name="remarks"></a>Comentarios

Un **WillChangeRecordset** o **RecordsetChangeComplete** evento puede producirse debido a los métodos de **Recordset** [Requery](requery-method-ado.md) u [Open](open-method-ado-recordset.md) .

Si el proveedor no admite marcadores, se produce una notificación de evento **RecordsetChange** cada vez de que se recuperan filas nuevas del proveedor. La frecuencia de este evento depende de la propiedad **RecordsetCacheSize**.

Debe establecer el parámetro **adStatus** en **adStatusUnwantedEvent** para cada valor posible de **adReason** con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro **adReason** .

