---
title: Tipos de eventos (referencia de base de datos de escritorio de Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314157"
---
# <a name="types-of-events"></a>Tipos de eventos


**Se aplica a:** Access 2013, Office 2013



Hay dos tipos básicos de eventos. Los "eventos Will", a los que se llama antes de iniciarse una operación, normalmente incluyen "Will" en su nombre; por ejemplo, **WillChangeRecordset** o **WillConnect**. Los eventos a los que se llama después de finalizar un evento suelen incluir "Complete" en su nombre; por ejemplo, **RecordChangeComplete** o **ConnectComplete**. Hay excepciones, como **InfoMessage**, pero éstas se producen después de finalizar la operación asociada.

## <a name="will-events"></a>Eventos Will

Los controladores de eventos a los que se llama antes de iniciarse la operación permiten examinar o modificar los parámetros de la operación y, a continuación, cancelar la operación o permitir que finalice. Estas rutinas de controladores de eventos normalmente tienen nombres con el formato*** Events * * *.

## <a name="complete-events"></a>Eventos Complete

Los controladores de eventos a los que se llama después de finalizar una operación pueden notificar a la aplicación la finalización de la operación. Estos controladores de eventos también reciben una notificación cuando un controlador de eventos Will cancela una operación pendiente. Normalmente, estas rutinas de controladores de eventos tienen nombres con el formato ***Event * complete**.

Los eventos Will y Complete suelen utilizarse emparejados.

## <a name="other-events"></a>Otros eventos

Los demás controladores de eventos, es decir, los eventos cuyos nombres no se encuentran en el formulario **, * evento*** o ***evento * completo,** solo se llaman después de que se complete una operación. Estos eventos son **Disconnect**, **EndOfRecordset** e **InfoMessage**.

