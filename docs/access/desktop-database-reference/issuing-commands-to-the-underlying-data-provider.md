---
title: Emitir comandos al proveedor de datos subyacente
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484411"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Emitir comandos al proveedor de datos subyacente


**Se aplica a**: Access 2013 | Office 2013

Cualquier comando que no empiece por SHAPE se pasa al proveedor de datos. Esto equivale a emitir un comando Shape de la forma "SHAPE {comando de proveedor}". Estos comandos *no* tienen que producir un **conjunto de registros**. Por ejemplo, "SHAPE {DROP TABLE MyTable} es un comando Shape perfectamente válido, suponiendo que el proveedor de datos admite DROP TABLE.

Esta característica permite que los comandos de proveedor normal y los comandos Shape compartan la misma conexión y la misma transacción.

