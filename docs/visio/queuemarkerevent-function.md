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
description: Hace que la aplicación desencadene un evento de marcador en el complemento, Microsoft Visual Basic para aplicaciones (VBA), o un complemento COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822888"
---
# <a name="queuemarkerevent-function"></a>Función QUEUEMARKEREVENT

Hace que la aplicación desencadene un evento de marcador en el complemento, Microsoft Visual Basic para aplicaciones (VBA), o un complemento COM. 
  
## <a name="syntax"></a>Sintaxis

QUEUEMARKEREVENT (** *cadena_evento* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cadena_evento_ <br/> |Obligatorio  <br/> |**String** <br/> | La cadena que se pase a su controlador de eventos.  <br/> |
   
## <a name="remarks"></a>Comentarios

La función QUEUEMARKEREVENT ofrece a los programadores una forma de notificar a su código de una celda de ShapeSheet y pasar información específica de la solución. Cuando la celda que contiene la fórmula con la función QUEUEMARKEREVENT se evalúa, la aplicación desencadena un evento de marcador y pasa _cadena_evento_ a todos los controladores de eventos que estén atentos al evento **MarkerEvent** . 
  
Para obtener más información acerca de los eventos de marcador, vea el método **QueueMarkerEvent** y temas de evento **MarkerEvent** en la referencia de automatización de Microsoft Visio. 
  
## <a name="example"></a>Ejemplo

QUEUEMARKEREVENT ("MiNotificaciónPersonalizada") 
  
Hace que la aplicación desencadene un evento de marcador y pasa la cadena "MiNotificaciónPersonalizada" a los controladores de eventos que estén atentos al evento **MarkerEvent**. 
  

