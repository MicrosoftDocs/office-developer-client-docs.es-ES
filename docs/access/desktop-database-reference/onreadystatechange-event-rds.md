---
title: onReadyStateChange (evento, RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87e6e7718ef99f10dc185104f1f11959e6589c89
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949848"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange (evento, RDS)

**Se aplica a**: Access 2013, Office 2013

El evento **onReadyStateChange** recibe una llamada cuando el valor de la propiedad [ReadyState](readystate-property-rds.md) cambia.

## <a name="syntax"></a>Sintaxis

onReadyStateChange

## <a name="parameters"></a>Parámetros

Ninguno.

## <a name="remarks"></a>Comentarios

La propiedad **ReadyState** refleja el progreso de un objeto [RDS.DataControl](datacontrol-object-rds.md) a medida que recupera asincrónicamente datos en su objeto [Recordset](recordset-object-ado.md). Use el evento **onReadyStateChange** para supervisar los cambios que se produzcan en la propiedad **ReadyState**. Este método resulta más eficiente que comprobar periódicamente el valor de la propiedad.

