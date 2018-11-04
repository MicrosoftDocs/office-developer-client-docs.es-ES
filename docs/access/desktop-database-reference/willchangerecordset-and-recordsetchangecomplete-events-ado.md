---
title: WillChangeRecordset y RecordsetChangeComplete (eventos, ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 47d2c4a870151e8c917e7d00eca3e3d152bbfb8b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950205"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>WillChangeRecordset y RecordsetChangeComplete (eventos, ADO)

**Se aplica a**: Access 2013, Office 2013

Al evento **WillChangeRecordset** se le llama antes de que una operación pendiente cambie el [Recordset](recordset-object-ado.md). Al evento **RecordsetChangeComplete** se le llama después de que el objeto **Recordset** haya cambiado.

## <a name="syntax"></a>Sintaxis

WillChangeRecordset*adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*adReason* |Valor [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnRequery**, **adRsnResynch**, **adRsnClose** o ** adRsnOpen**.|
|*valor de adStatus* |[EventStatusEnum](eventstatusenum.md). Cuando se llama a **WillChangeRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente. <br/><br/>Cuando se llama a **RecordsetChangeComplete**, este parámetro se establece en ** adStatusOK** si la operación que provocó el evento se realizó correctamente, en **adStatusErrorsOccurred** si se produjo un error en la operación o en **adStatusCancel** si se ha cancelado la operación asociada al evento **WillChangeRecordset** anteriormente aceptado. <br/><br/>Antes de que **WillChangeRecordset** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores. <br/><br/>Antes de que **WillChangeRecordset** o **RecordsetChangeComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*Connection* |Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.|

## <a name="remarks"></a>Comentarios

Un **WillChangeRecordset** o **RecordsetChangeComplete** evento puede producirse debido a los métodos de **Recordset** [Requery](requery-method-ado.md) u [Open](open-method-ado-recordset.md) .

Si el proveedor no admite marcadores, se produce una notificación de evento **RecordsetChange** cada vez de que se recuperan filas nuevas del proveedor. La frecuencia de este evento depende de la propiedad **RecordsetCacheSize**.

Debe establecer el parámetro **adStatus** en **adStatusUnwantedEvent** para cada valor posible de **adReason** con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro **adReason** .

