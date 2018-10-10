---
title: InfoMessage (evento, ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6cc3b69eb3310d8e717605edd3d6fae32d635806
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486724"
---
# <a name="infomessage-event-ado"></a>InfoMessage (evento, ADO)


**Se aplica a**: Access 2013 | Office 2013

Al evento **InfoMessage** se le llama siempre que se produce una advertencia durante una operación **ConnectionEvent**.

## <a name="syntax"></a>Sintaxis

InfoMessage*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parámetros

  - *pError*

  - Objeto [Error](error-object-ado.md). Este parámetro contiene cualquier error devuelto. Si se devuelven varios errores, enumere la colección **Errors** para encontrarlos.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.

  - *pConnection*

  - Objeto [Connection](connection-object-ado.md). La conexión para la que se produjo la advertencia. Por ejemplo, las advertencias pueden ocurrir al abrir un objeto **Connection** o ejecutar un objeto [Command](command-object-ado.md) sobre un objeto **Connection**.

