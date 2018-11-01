---
title: EndOfRecordset (evento, ADO)
TOCTitle: EndOfRecordset Event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a95ae75eb71ea50e08952418058f87bf54a40e45
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888128"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset (evento, ADO)


**Se aplica a**: Access 2013, Office 2013



Al evento **EndOfRecordset** se le llama cuando se intenta pasar a una fila más allá del final del objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

  - *fMoreData*

  - A **VARIANT\_BOOL** valor que, si se establece en VARIANT\_TRUE, indica que se han agregado más filas para el **conjunto de registros**.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Al llamar a **EndOfRecordset**, este parámetro se establece en **adStatusOK** si la operación que provocó el evento se realizó correctamente. Se establece en **adStatusCantDeny** si este evento no puede solicitar la cancelación de la operación que provocó este evento.
    
    Antes de que **EndOfRecordset** vuelva, establezca este parámetro en **adStatusUnwantedEvent** para evitar notificaciones posteriores.

  - *Connection*

  - Objeto **Recordset**. El objeto **Recordset** para el que se produjo este evento.

## <a name="remarks"></a>Comentarios

Un evento **EndOfRecordset** puede ocurrir si se produce un error en la operación [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

El controlador del evento recibe una llamada cuando se realiza un intento de avanzar más allá del final del objeto **Recordset**, quizá debido a una llamada a **MoveNext**. Sin embargo, mientras ocurre este evento, todavía se podrían recuperar más registros de una base de datos y agregarlos al final del objeto **Recordset**. En ese caso, establezca *fMoreData* en VARIANT\_es TRUE y devolución de **EndOfRecordset**. A continuación, llame de nuevo a **MoveNext** para obtener acceso a los registros recién recuperados.

