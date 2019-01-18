---
title: WillMove y MoveComplete (eventos, ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705963"
---
# <a name="willmove-and-movecomplete-events-ado"></a>WillMove y MoveComplete (eventos, ADO)

**Se aplica a**: Access 2013, Office 2013

El evento **WillMove** recibe una llamada antes de que una operación pendiente cambie la posición actual en el objeto [Recordset](recordset-object-ado.md). El evento **MoveComplete** recibe una llamada después de que la posición actual del objeto **Recordset** cambie.

## <a name="syntax"></a>Sintaxis

WillMove*adReason*, *adStatus*, *pRecordset*

MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*adReason* |Valor de [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** o **adRsnRequery**.|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*valor de adStatus* |[EventStatusEnum](eventstatusenum.md). Cuando se llama a **WillMove** , este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación pendiente. <br/><br/>Cuando se llama a **MoveComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación. <br/><br/>Antes de que **WillMove** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores. <br/><br/>Antes de que **MoveComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*Connection* |Objeto [Recordset](recordset-object-ado.md). El objeto **Recordset** para el que se produjo este evento.|

## <a name="remarks"></a>Comentarios

Un evento **WillMove** o **MoveComplete** puede producir debido a las siguientes operaciones de **conjunto de registros** :

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [Métodos MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

Es posible que se produzcan estos eventos debido a las siguientes propiedades:

- [Filtro](filter-property-ado.md)
- [Índice](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Estos eventos también se producen si un objeto **Recordset** secundario tiene eventos de **Recordset** conectados y se mueve su **Recordset** principal.

Debe establecer el parámetro *adStatus* en **adStatusUnwantedEvent** para cada valor posible de *adReason* con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro *adReason* .

