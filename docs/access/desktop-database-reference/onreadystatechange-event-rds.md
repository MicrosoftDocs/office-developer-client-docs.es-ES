---
title: Evento onReadyStateChange (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288493"
---
# <a name="onreadystatechange-event-rds"></a>Evento onReadyStateChange (RDS)

**Se aplica a:** Access 2013, Office 2013

El evento **onReadyStateChange** recibe una llamada cuando el valor de la propiedad [ReadyState](readystate-property-rds.md) cambia.

## <a name="syntax"></a>Sintaxis

onReadyStateChange

## <a name="parameters"></a>Parámetros

Ninguno.

## <a name="remarks"></a>Comentarios

La propiedad **ReadyState** refleja el progreso de un objeto [RDS.DataControl](datacontrol-object-rds.md) a medida que recupera asincrónicamente datos en su objeto [Recordset](recordset-object-ado.md). Use el evento **onReadyStateChange** para supervisar los cambios que se produzcan en la propiedad **ReadyState**. Este método resulta más eficiente que comprobar periódicamente el valor de la propiedad.

