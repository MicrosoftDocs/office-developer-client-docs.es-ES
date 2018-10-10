---
title: s ConnectComplete y Disconnect (evento, ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 731879abf181f64c24b1012e45ea23435f965574
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485980"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>s ConnectComplete y Disconnect (evento, ADO)


**Se aplica a**: Access 2013 | Office 2013

Al evento **ConnectComplete** se le llama después de que un conexión se *inicia*. Al evento **Disconnect** se le llama después de que una conexión *finaliza*.

## <a name="syntax"></a>Sintaxis

ConnectComplete*pError*, *adStatus*, *pConnection*

Desconectar*adStatus*, *pConnection*

## <a name="parameters"></a>Parámetros

  - *pError*

  - Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Cuando se llama a **ConnectComplete**, este parámetro se establece en **adStatusCancel** si un evento **WillConnect** ha solicitado la cancelación de la conexión pendiente.
    
    Antes de que cualquiera evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores. Sin embargo, si se cierra y se vuelve a abrir el objeto [Connection](connection-object-ado.md), estos eventos vuelven a ocurrir.

  - *pConnection*

  - Objeto **Connection** al que se aplica este evento.

