---
title: onError (evento, RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486451"
---
# <a name="onerror-event-rds"></a>onError (evento, RDS)


**Se aplica a**: Access 2013 | Office 2013

El evento **onError** recibe una llamada siempre que se produce un error durante una operación.

## <a name="syntax"></a>Sintaxis

onError*SCode*, *Descripción*, *origen*, *CancelDisplay*

## <a name="parameters"></a>Parámetros

  - *SCode*

  - Un entero que indica el código de estado del error.

  - *Description*

  - Un objeto **String** que indica una descripción del error.

  - *Origen*

  - Un objeto **String** que indica la consulta o el comando que produjo el error.

  - *CancelDisplay*

  - Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.

