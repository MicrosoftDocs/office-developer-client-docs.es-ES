---
title: Notificaciones de formularios de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38011c02791688ce5b1c291a1355ccaececd43fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574737"
---
# <a name="mapi-forms-notifications"></a>Notificaciones de formularios de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registrar para y controlar las notificaciones de objetos de formulario es un proceso diferente que para otros objetos MAPI. Receptores de notificaciones para implementar notificaciones de formulario ya sea el **IMAPIViewAdviseSink** o **IMAPIFormAdviseSink** interfaz en lugar de **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) y [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) cada uno de ellos tener varios métodos, uno para cada uno de los eventos posibles que el correspondiente aviso origen es capaz de generar. Por ejemplo, **IMAPIFormAdviseSink** tiene dos métodos: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) para controlar un cambio en el Visor de formulario estado y [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) para mostrar un nuevo mensaje con el formato correcto. 
  
El evento estrategia para los formularios de control es similar a la estrategia de implementada en OLE de control de eventos. Los clientes no se registra para determinados tipos de eventos como lo hacen para la mayoría de los objetos MAPI. La suposición es que registrarse para recibir notificaciones les permite recibir cualquier tipo de evento que se puede generar por el origen de advise determinado. Debido a que **IMAPIAdviseSink::OnNotify** debe escribirse con el fin de controlar todos los eventos registrados, su implementación puede ser complejo para los clientes que registrar para muchos eventos diferentes. Debido a que el destino de los objetos del receptor de aviso de los métodos en el formulario de un solo evento, implementación de estos métodos es más sencillo. 
  

