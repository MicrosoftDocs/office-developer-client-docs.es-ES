---
title: Type (propiedad, Stream de ADO)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306254"
---
# <a name="type-property-ado-stream"></a>Type (propiedad, Stream de ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el tipo de tipo de datos incluidos en el objeto [Stream](stream-object-ado.md) (binarios o texto).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor [StreamTypeEnum](streamtypeenum.md) que especifica el tipo de datos incluidos en el objeto **Stream**. El valor predeterminado es **adTypeText**. No obstante, si se escriben datos binarios en un nuevo objeto **Stream** vacío, la propiedad **Type** cambiará a **adTypeBinary**.

## <a name="remarks"></a>Comentarios

La propiedad **Type** es de lectura y escritura únicamente cuando la posición actual se encuentra al inicio del objeto **Stream** ([Position](position-property-ado.md) es 0) y de sólo lectura en todas las demás posiciones.

La propiedad **Type** determina los métodos que se deben utilizar para leer y escribir el objeto **Stream**. En los objetos **Stream** de texto, utilice [ReadText](readtext-method-ado.md) y [WriteText](writetext-method-ado.md). En los objetos **Stream** binarios, utilice [Read](read-method-ado.md) y [Write](write-method-ado.md).

