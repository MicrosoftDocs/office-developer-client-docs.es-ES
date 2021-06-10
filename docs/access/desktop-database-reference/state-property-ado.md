---
title: Propiedad State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308536"
---
# <a name="state-property-ado"></a>Propiedad State (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica, para todos los objetos aplicables, si el estado del objeto es abierto o cerrado.

Indica para todos los objetos aplicables que ejecutan un método asincrónico si el objeto se encuentra actualmente en estado de conexión, ejecución o recuperación.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que puede ser un valor [ObjectStateEnum](objectstateenum.md). El valor predeterminado es **adStateClosed**.

## <a name="remarks"></a>Comentarios

Puede utilizar la propiedad **Estado (State)** para determinar el estado actual de un objeto dado en cualquier momento.

La propiedad **Estado (State)** del objeto puede tener una combinación de valores. Por ejemplo, si se está ejecutando una instrucción, esta propiedad tendrá un valor combinado de **adStateOpen** y **adStateExecuting**.

La propiedad **Estado (State)** es de sólo lectura.

