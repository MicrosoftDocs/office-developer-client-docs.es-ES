---
title: Propiedad InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291244"
---
# <a name="internettimeout-property-rds"></a>Propiedad InternetTimeout (RDS)


**Se aplica a:** Access 2013, Office 2013

Indica el número de milisegundos que se debe esperar antes de que una solicitud exceda el tiempo de espera.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que representa el número de milisegundos antes de que una solicitud exceda el tiempo de espera.

## <a name="remarks"></a>Comentarios

Esta propiedad se aplica sólo a solicitudes enviadas mediante los protocolos HTTP o HTTPS.

Las solicitudes de un entorno de tres niveles pueden tardar varios minutos en ejecutarse. Use esta propiedad para especificar tiempo adicional para aquellas solicitudes de ejecución larga.

