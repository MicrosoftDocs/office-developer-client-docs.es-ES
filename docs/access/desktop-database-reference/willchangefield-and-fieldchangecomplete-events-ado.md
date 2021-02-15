---
title: Eventos WillChangeField y FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302488"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>Eventos WillChangeField y FieldChangeComplete (ADO)

**Se aplica a:** Access 2013, Office 2013

Al evento **WillChangeField** se le llama antes de que una operación pendiente cambie el valor de uno o varios objetos [Field](field-object-ado.md) en el objeto [Recordset](recordset-object-ado.md). Al evento **FieldChangeComplete** se le llama después de que el valor de uno o varios objetos **Field** haya cambiado.

## <a name="syntax"></a>Sintaxis

WillChangeField *cFields*, *Fields*, *adStatus*, *pRecordset*

FieldChangeComplete *cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*cFields* |Valor **Long** que indica el número de objetos **Field** en *Fields*.|
|*Fields* |Para **WillChangeField**, el parámetro *Fields* es una matriz de **Variants** que contiene objetos **Field** con los valores originales. <br/><br/>Para **FieldChangeComplete**, el parámetro *Fields* es una matriz de **Variants** que contiene objetos **Field** con los valores modificados.|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Cuando se llama a **WillChangeField**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente. <br/><br/>Cuando se llama a **FieldChangeComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación. <br/><br/>Antes de que **WillChangeField** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente. <br/><br/>Antes de que **FieldChangeComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*pRecordset* |Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.|

## <a name="remarks"></a>Comentarios

Un evento **WillChangeField** o **FieldChangeComplete** se puede producir al establecer la propiedad [Value](value-property-ado.md) y llamar al método [Update](update-method-ado.md) con parámetros de tipo array (matriz) para field (campo) y value (valor).

