---
title: onError (evento, RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712179"
---
# <a name="onerror-event-rds"></a>onError (evento, RDS)

**Se aplica a**: Access 2013, Office 2013

El evento **onError** recibe una llamada siempre que se produce un error durante una operación.

## <a name="syntax"></a>Sintaxis

onError*SCode*, *Descripción*, *origen*, *CancelDisplay*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*SCode* |Un entero que indica el código de estado del error.|
|*Description* |Un objeto **String** que indica una descripción del error.|
|*Origen* |Un objeto **String** que indica la consulta o el comando que produjo el error.|
|*CancelDisplay* |Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.|

