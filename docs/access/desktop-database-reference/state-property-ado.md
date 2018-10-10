---
title: State (propiedad, ADO)
TOCTitle: State Property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2bde03f1d6c7619e8140248b2551002f0453fc9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486591"
---
# <a name="state-property-ado"></a>State (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

En todos los objetos aplicables indica si el estado del objeto es abierto o cerrado.

Indica para todos los objetos aplicables que ejecutan un método asincrónico si el objeto se encuentra actualmente en estado de conexión, ejecución o recuperación.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que puede ser un valor [ObjectStateEnum](objectstateenum.md). El valor predeterminado es **adStateClosed**.

## <a name="remarks"></a>Comentarios

Puede utilizar la propiedad **Estado (State)** para determinar el estado actual de un objeto dado en cualquier momento.

La propiedad **Estado (State)** del objeto puede tener una combinación de valores. Por ejemplo, si se está ejecutando una instrucción, esta propiedad tendrá un valor combinado de **adStateOpen** y **adStateExecuting**.

La propiedad **Estado (State)** es de sólo lectura.

