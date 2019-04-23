---
title: OnError (evento, RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288479"
---
# <a name="onerror-event-rds"></a>OnError (evento, RDS)

**Se aplica a:** Access 2013, Office 2013

El evento **onError** recibe una llamada siempre que se produce un error durante una operación.

## <a name="syntax"></a>Sintaxis

OnError*SCode*, *Descripción*, *origen*, *CancelDisplay*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*SCode* |Un entero que indica el código de estado del error.|
|*Description* |Un objeto **String** que indica una descripción del error.|
|*Origen* |Un objeto **String** que indica la consulta o el comando que produjo el error.|
|*CancelDisplay* |Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.|

