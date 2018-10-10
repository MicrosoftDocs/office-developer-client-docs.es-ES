---
title: ConnectionTimeout (propiedad, ADO)
TOCTitle: ConnectionTimeout Property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 375af7f4dc84d1a630c290df1c38e77ee6580b5d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484590"
---
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el tiempo que se va a esperar durante el establecimiento de una conexión para que finalice el intento y se genere un error.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que indica, en segundos, el tiempo que se va a esperar a que se abra la conexión. El valor predeterminado es 15.

## <a name="remarks"></a>Comentarios

Use la propiedad **ConnectionTimeout** en un objeto [Connection](connection-object-ado.md) si, debido a demoras en el tráfico de red o la sobrecarga del servidor, es preciso abandonar un intento de establecer conexión. Si transcurre el tiempo especificado por la propiedad **ConnectionTimeout** antes de que se abra la conexión, se genera un error y ADO cancela el intento. Si la propiedad tiene el valor cero, ADO esperará indefinidamente a que se abra la conexión. Asegúrese de que el proveedor en el que está escribiendo código admite la funcionalidad **ConnectionTimeout**.

La propiedad **ConnectionTimeout** es de lectura y escritura cuando está cerrada la conexión, y es de sólo lectura cuando la conexión está abierta.

