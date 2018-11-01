---
title: s WillMove y MoveComplete (evento, ADO)
TOCTitle: WillMove and MoveComplete Events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b1a0e119d857947b78eb6adcfc9a5b1ba87e055
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868836"
---
# <a name="willmove-and-movecomplete-events-ado"></a>s WillMove y MoveComplete (evento, ADO)


**Se aplica a**: Access 2013, Office 2013

El evento **WillMove** recibe una llamada antes de que una operación pendiente cambie la posición actual en el objeto [Recordset](recordset-object-ado.md). El evento **MoveComplete** recibe una llamada después de que la posición actual del objeto **Recordset** cambie.

## <a name="syntax"></a>Sintaxis

WillMove*adReason*, *adStatus*, *pRecordset*

MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

  - *adReason*

  - Valor de [EventReasonEnum](eventreasonenum.md) que especifica el motivo de este evento. Su valor puede ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** o **adRsnRequery**.

  - *pError*

  - Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Cuando se realiza una llamada a **WillMove**, este parámetro se establece a **adStatusOK** si la operación que provocó el evento se realizó correctamente.Se establece en **adStatusCantDeny** si este evento no puede solicitar cancelación de la operación pendiente.
    
    Cuando se llama a **MoveComplete**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente, o en **adStatusErrorsOccurred** si se produjo un error en la operación.
    
    Antes de que **WillMove** vuelva, establezca este parámetro en **adStatusCancel** para solicitar la cancelación de la operación pendiente, o en adStatusUnwantedEvent para impedir notificaciones posteriores.
    
    Antes de que **MoveComplete** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.

  - *Connection*

  - Objeto [Recordset](recordset-object-ado.md). El objeto **Recordset** para el que se produjo este evento.

## <a name="remarks"></a>Comentarios

Un evento **WillMove** o **MoveComplete** se puede producir debido a las siguientes operaciones con **Recordsets**: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) y [Requery](requery-method-ado.md). Estos eventos se pueden producir a causa de las propiedades siguientes: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) y [AbsolutePosition](absoluteposition-property-ado.md). Estos eventos también se producen si un objeto **Recordset** secundario tiene eventos de **Recordset** conectados y se mueve su **Recordset** principal.

Deberá establecer el parámetro **adStatus** en **adStatusUnwantedEvent** para cada valor adReason posible con el fin de detener completamente la notificación de eventos para cualquier evento que incluya un parámetro adReason.

