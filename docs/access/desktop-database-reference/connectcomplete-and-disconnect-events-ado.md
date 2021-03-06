---
title: Eventos ConnectComplete y Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295992"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>Eventos ConnectComplete y Disconnect (ADO)

**Se aplica a:** Access 2013, Office 2013

Al evento **ConnectComplete** se le llama después de que un conexión se *inicia*. Al evento **Disconnect** se le llama después de que una conexión *finaliza*.

## <a name="syntax"></a>Sintaxis

ConnectComplete *pError*, *adStatus*, *pConnection*

Desconectar *adStatus*, *pConnection*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Cuando se llama a **ConnectComplete**, este parámetro se establece en **adStatusCancel** si un evento **WillConnect** ha solicitado la cancelación de la conexión pendiente.<br/><br/>Antes de que cualquiera evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores. Sin embargo, si se cierra y se vuelve a abrir el objeto [Connection](connection-object-ado.md), estos eventos vuelven a ocurrir.|
|*pConnection* |Objeto **Connection** al que se aplica este evento.|

