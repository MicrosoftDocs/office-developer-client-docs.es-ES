---
title: Emisión de comandos al proveedor de datos subyacente
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291091"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Emisión de comandos al proveedor de datos subyacente

**Se aplica a:** Access 2013, Office 2013

Cualquier comando que no empiece por SHAPE se pasa al proveedor de datos. Esto equivale a emitir un comando Shape de la forma "SHAPE {comando de proveedor}". Estos comandos *no* tienen que producir un **conjunto de registros**. Por ejemplo, "SHAPE {DROP TABLE MyTable} es un comando Shape perfectamente válido, suponiendo que el proveedor de datos admite DROP TABLE.

Esta característica permite que los comandos de proveedor normal y los comandos Shape compartan la misma conexión y la misma transacción.

