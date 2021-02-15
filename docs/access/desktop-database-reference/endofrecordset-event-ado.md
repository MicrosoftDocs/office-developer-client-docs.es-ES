---
title: Evento EndOfRecordset (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293563"
---
# <a name="endofrecordset-event-ado"></a>Evento EndOfRecordset (ADO)

**Se aplica a:** Access 2013, Office 2013

Al evento **EndOfRecordset** se le llama cuando se intenta pasar a una fila más allá del final del objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*fMoreData* |Valor **VARIANT \_ BOOL** que, si se establece en VARIANT TRUE, indica que se han agregado más filas \_ al conjunto de **registros**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Al llamar a **EndOfRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación que provocó este evento.<br/><br/>Antes de que **EndOfRecordset** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para evitar notificaciones posteriores.|
|*pRecordset* | Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.|

## <a name="remarks"></a>Comentarios

Un evento **EndOfRecordset** puede ocurrir si se produce un error en la operación [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

El controlador del evento recibe una llamada cuando se realiza un intento de avanzar más allá del final del objeto **Recordset**, quizá debido a una llamada a **MoveNext**. Sin embargo, mientras ocurre este evento, todavía se podrían recuperar más registros de una base de datos y agregarlos al final del objeto **Recordset**. En ese caso, establezca *fMoreData* en VARIANT \_ TRUE y devuelva desde **EndOfRecordset**. A continuación, llame de nuevo a **MoveNext** para obtener acceso a los registros recién recuperados.

