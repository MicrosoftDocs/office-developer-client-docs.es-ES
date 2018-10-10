---
title: onReadyStateChange (evento, RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dec783aaa76745b73bd031b00f1b8587a58eb165
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485514"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange (evento, RDS)


**Se aplica a**: Access 2013 | Office 2013


El evento **onReadyStateChange** recibe una llamada cuando el valor de la propiedad [ReadyState](readystate-property-rds.md) cambia.

## <a name="syntax"></a>Sintaxis

onReadyStateChange

## <a name="parameters"></a>Parámetros

Ninguno.

## <a name="remarks"></a>Comentarios

La propiedad **ReadyState** refleja el progreso de un objeto [RDS.DataControl](datacontrol-object-rds.md) a medida que recupera asincrónicamente datos en su objeto [Recordset](recordset-object-ado.md). Use el evento **onReadyStateChange** para supervisar los cambios que se produzcan en la propiedad **ReadyState**. Este método resulta más eficiente que comprobar periódicamente el valor de la propiedad.

