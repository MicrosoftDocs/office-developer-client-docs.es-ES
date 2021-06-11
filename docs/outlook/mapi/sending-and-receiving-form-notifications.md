---
title: Enviar y recibir notificaciones de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431858"
---
# <a name="sending-and-receiving-form-notifications"></a>Enviar y recibir notificaciones de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las notificaciones de formulario se usan en MAPI para facilitar la comunicación tanto del formulario al visor como del visor al formulario.
  
Los formularios envían notificaciones al visor cuando se produce uno de los siguientes eventos:
  
- El formulario está cerrado.
    
- Se carga un nuevo mensaje en el formulario.
    
- Se ha completado una operación de guardado.
    
- Se envía un mensaje.
    
Cada uno de estos tipos de eventos corresponden a un método determinado en [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), una de las interfaces que debe implementar el visor de formularios. Cuando se produce un evento, el formulario llama al método **IMAPIViewAdviseSink** correspondiente en el receptor de avisos del visor. Por ejemplo, cuando llega un nuevo mensaje que el visor debe incluir en su presentación, el formulario llama al método [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) 
  
Implementar el receptor de avisos de vista de una manera que tenga sentido para el visor; no hay ninguna implementación estándar. Por ejemplo, en **OnNewMessage** puede actualizar la vista de la tabla de contenido de la carpeta actual para incluir el mensaje recién llegado. En [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), el método al que se llama cuando recibe un evento de mensaje enviado, puede copiar el mensaje enviado en una carpeta Elementos enviados.
  
Los formularios reciben una notificación del visor cuando se produce un cambio que afecta al formulario y cuando se carga un mensaje nuevo. Para notificar a un formulario, llame a uno de los métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) o [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Llame **a OnChange** para comunicar el estado. Por ejemplo, si el formulario muestra el último elemento de una carpeta cuando llega un mensaje nuevo, llame a **OnChange** con la marca VCSTATUS_NEXT establecida para decir al formulario que ahora hay un elemento siguiente. 
  
Llama **a OnActivateNext para** avisar al formulario de la llegada de un nuevo mensaje que puede o no poder mostrar. Pase la clase de mensaje del mensaje a **OnActivateNext**. 
  
Las notificaciones de un objeto de formulario a la aplicación cliente se controlan mediante la interfaz **IMAPIViewAdviseSink** de la aplicación cliente. Para obtener más información, [vea IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

