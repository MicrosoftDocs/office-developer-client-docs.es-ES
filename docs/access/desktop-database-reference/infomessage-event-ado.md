---
title: InfoMessage (evento, ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1db793ec99dd0248eacc527bd76068ceec025a58
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949435"
---
# <a name="infomessage-event-ado"></a>InfoMessage (evento, ADO)

**Se aplica a**: Access 2013, Office 2013

Al evento **InfoMessage** se le llama siempre que se produce una advertencia durante una operación **ConnectionEvent**.

## <a name="syntax"></a>Sintaxis

InfoMessage*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*pError* |Objeto [Error](error-object-ado.md). Este parámetro contiene cualquier error devuelto. Si se devuelven varios errores, enumere la colección **Errors** para encontrarlos.|
|*valor de adStatus* |[EventStatusEnum](eventstatusenum.md). Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*pConnection* |Objeto [Connection](connection-object-ado.md). La conexión para la que se produjo la advertencia. Por ejemplo, las advertencias pueden ocurrir al abrir un objeto **Connection** o ejecutar un objeto [Command](command-object-ado.md) sobre un objeto **Connection**.|

