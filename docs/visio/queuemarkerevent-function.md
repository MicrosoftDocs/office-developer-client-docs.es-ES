---
title: QUEUEMARKEREVENT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Hace que la aplicación desaprenda un evento de marcador en el complemento, el código de Microsoft Visual Basic para Aplicaciones (VBA) o el complemento COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418809"
---
# <a name="queuemarkerevent-function"></a>Función QUEUEMARKEREVENT

Hace que la aplicación desaprenda un evento de marcador en el complemento, el código de Microsoft Visual Basic para Aplicaciones (VBA) o el complemento COM. 
  
## <a name="syntax"></a>Sintaxis

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Obligatorio  <br/> |**String** <br/> | La cadena que se pasará al controlador de eventos.  <br/> |
   
## <a name="remarks"></a>Comentarios

La función QUEUEMARKEREVENT ofrece a los programadores un método para notificar al código desde una celda de ShapeSheet y pasar información específica de la solución. Cuando se evalúa la celda que contiene la fórmula con la función QUEUEMARKEREVENT, la aplicación activa un evento de marcador y pasa _event_string_ a todos los controladores de eventos que escuchan el evento **MarkerEvent.** 
  
Para obtener más información acerca de los eventos de marcador, vea los temas del método **QueueMarkerEvent** y del evento **MarkerEvent** en la Referencia de automatización de Microsoft Visio. 
  
## <a name="example"></a>Ejemplo

QUEUEMARKEREVENT ("MiNotificaciónPersonalizada") 
  
Hace que la aplicación desencadene un evento de marcador y pasa la cadena "MiNotificaciónPersonalizada" a los controladores de eventos que estén atentos al evento **MarkerEvent**. 
  

