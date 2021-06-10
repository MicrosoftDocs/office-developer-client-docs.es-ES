---
title: Eventos WillMove y MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306058"
---
# <a name="willmove-and-movecomplete-events-ado"></a>Eventos WillMove y MoveComplete (ADO)

**Se aplica a:** Access 2013, Office 2013

El evento **WillMove** recibe una llamada antes de que una operación pendiente cambie la posición actual en el objeto [Recordset](recordset-object-ado.md). El evento **MoveComplete** recibe una llamada después de que la posición actual del objeto **Recordset** cambie.

## <a name="syntax"></a>Sintaxis

WillMove *adReason*, *adStatus*, *pRecordset*

MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*adReason* |Valor de [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** o **adRsnRequery**.|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Cuando **se llama a WillMove,** este parámetro se establece en **adStatusOK** si la operación que provocó el evento se ha realizado correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente. <br/><br/>Cuando se llama a **MoveComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación. <br/><br/>Antes de que **WillMove** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores. <br/><br/>Antes de que **MoveComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*pRecordset* |Objeto [Recordset](recordset-object-ado.md). El objeto **Recordset** para el que se produjo este evento.|

## <a name="remarks"></a>Comentarios

Puede producirse un evento **WillMove** **o MoveComplete** debido a las siguientes **operaciones recordset:**

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

Estos eventos pueden producirse debido a las siguientes propiedades:

- [Filter](filter-property-ado.md)
- [Índice](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Estos eventos también se producen si un objeto **Recordset** secundario tiene eventos de **Recordset** conectados y se mueve su **Recordset** principal.

Deberá establecer el parámetro *adStatus* como **adStatusUnwantedEvent** para cada valor posible de *adReason* con el fin de detener completamente la notificación de eventos para cualquier suceso que incluya un parámetro *adReason*.

