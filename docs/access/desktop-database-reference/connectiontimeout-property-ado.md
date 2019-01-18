---
title: ConnectionTimeout (propiedad, ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700937"
---
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el tiempo que se va a esperar durante el establecimiento de una conexión para que finalice el intento y se genere un error.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que indica, en segundos, el tiempo que se va a esperar a que se abra la conexión. El valor predeterminado es 15.

## <a name="remarks"></a>Comentarios

Use la propiedad **ConnectionTimeout** en un objeto [Connection](connection-object-ado.md) si, debido a demoras en el tráfico de red o la sobrecarga del servidor, es preciso abandonar un intento de establecer conexión. Si transcurre el tiempo especificado por la propiedad **ConnectionTimeout** antes de que se abra la conexión, se genera un error y ADO cancela el intento. Si la propiedad tiene el valor cero, ADO esperará indefinidamente a que se abra la conexión. Asegúrese de que el proveedor en el que está escribiendo código admite la funcionalidad **ConnectionTimeout**.

La propiedad **ConnectionTimeout** es de lectura y escritura cuando está cerrada la conexión, y es de sólo lectura cuando la conexión está abierta.

