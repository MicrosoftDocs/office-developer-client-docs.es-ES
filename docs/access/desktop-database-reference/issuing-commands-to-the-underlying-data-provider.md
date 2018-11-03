---
title: Emitir comandos al proveedor de datos subyacente
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944637"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Emitir comandos al proveedor de datos subyacente

**Se aplica a**: Access 2013, Office 2013

Cualquier comando que no empiece por SHAPE se pasa al proveedor de datos. Esto equivale a emitir un comando Shape de la forma "SHAPE {comando de proveedor}". Estos comandos *no* tienen que producir un **conjunto de registros**. Por ejemplo, "SHAPE {DROP TABLE MyTable} es un comando Shape perfectamente válido, suponiendo que el proveedor de datos admite DROP TABLE.

Esta característica permite que los comandos de proveedor normal y los comandos Shape compartan la misma conexión y la misma transacción.

