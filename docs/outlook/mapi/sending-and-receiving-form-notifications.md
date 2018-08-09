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
ms.openlocfilehash: 4730fb04d530fce516fe1ca4fd572c58fc1f1ffa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820614"
---
# <a name="sending-and-receiving-form-notifications"></a>Enviar y recibir notificaciones de formulario

  
  
**Hace referencia a**: Outlook 
  
Notificaciones de formulario se usan en MAPI para facilitar la comunicación tanto desde el formulario a su visor, así como desde el visor al formulario.
  
Formularios de envían notificaciones a su visor cuando se producen uno de los siguientes eventos:
  
- Se cierra el formulario.
    
- Se carga un nuevo mensaje en el formulario.
    
- Se completa una operación de guardar.
    
- Se envía un mensaje.
    
Cada uno de estos tipos de evento corresponden a un método concreto en [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), una de las interfaces que debe implementar el Visor de formulario. Cuando se produce un evento, las llamadas de formulario **IMAPIViewAdviseSink** del método correspondiente en el Visor del aviso receptor. Por ejemplo, cuando llega un nuevo mensaje que debe incluir el Visor en su presentación, el formulario llama al método [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Implementar la vista de aviso receptor en una forma que tiene sentido para su Visor; No hay ninguna implementación estándar. Por ejemplo, puede actualizar la vista de tabla de contenido de la carpeta actual para incluir el mensaje recién llegado en **OnNewMessage** . En [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), el método que se llama cuando se recibe un evento de mensaje enviado, puede copiar el mensaje enviado a una carpeta de elementos enviados.
  
Formularios de reciben una notificación de su visor cuando se produce un cambio que influye en el formulario y cuando se carga un nuevo mensaje. Para notificar a un formulario, llame a uno de los métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) o [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Llamada **OnChange** para comunicar el estado. Por ejemplo, si el formulario muestra el último elemento en una carpeta cuando llegue un nuevo mensaje, llamada **OnChange** con el indicador VCSTATUS_NEXT establecido para indicar que el formulario que ahora es un elemento siguiente. 
  
Llame a **OnActivateNext** para el formulario a la llegada de un nuevo mensaje de alerta que pueden o no pueden ser capaz de mostrar. Pase la clase de mensaje del mensaje a **OnActivateNext**. 
  
Las notificaciones por un objeto de formulario a la aplicación cliente se controlan mediante la interfaz de **IMAPIViewAdviseSink** de la aplicación cliente. Para obtener más información, vea [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).
  

