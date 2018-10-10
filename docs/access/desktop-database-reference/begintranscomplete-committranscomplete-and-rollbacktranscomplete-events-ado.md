---
title: Eventos de RollbackTransComplete BeginTransComplete, CommitTransComplete, (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 216f5a92ea4095d78b8df2b196a1607e40ae58d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486672"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>s BeginTransComplete, CommitTransComplete y RollbackTransComplete (evento, ADO)


**Se aplica a**: Access 2013 | Office 2013


A estos eventos se les llama después de que la operación asociada sobre el objeto [Connection](connection-object-ado.md) haya terminado de ejecutarse.

  - A **BeginTransComplete** se le llama después de la operación [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

  - A **CommitTransComplete** se le llama después de la operación [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

  - A **RollbackTransComplete** se le llama después de la operación [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

## <a name="syntax"></a>Sintaxis

De BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*

CommitTransComplete*pError*, *adStatus*, *pConnection*

A RollbackTransComplete*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parámetros

  - *TransactionLevel*

  - Valor **Long** que contiene el nuevo nivel de transacción de la operación **BeginTrans** que causó este evento.

  - *pError*

  - Objeto [Error](error-object-ado.md). Describe el error si el valor de EventStatusEnum es ** adStatusErrorsOccurred**; de lo contrario, no se establece un valor para él.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Estos eventos pueden impedir notificaciones posteriores si se establece este parámetro en **adStatusUnwantedEvent** antes de que el evento vuelva.

  - *pConnection*

  - El objeto **Recordset** para el que se produjo este evento.

## <a name="remarks"></a>Comentarios

En Visual C++, varios objetos **Connection** pueden compartir el mismo método de control de evento. El método utiliza el objeto ** Connection** devuelto para determinar qué objeto causó el evento.

Si la propiedad [Attributes](attributes-property-ado.md) se establece en **adXactCommitRetaining** o **adXactAbortRetaining**, se iniciará una transacción nueva después de confirmar o deshacer una transacción. Utilice el evento **BeginTransComplete** para omitir todo excepto el primer evento de inicio de transacción.

