---
title: Notificaciones de formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e9c10f78af6dff2e0d0c59d0bfe59be07dccd4b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418613"
---
# <a name="mapi-forms-notifications"></a>Notificaciones de formularios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El registro y el control de notificaciones desde objetos de formulario es un proceso diferente al de otros objetos MAPI. Aconseja a los receptores de notificaciones de formulario implementar la interfaz **IMAPIViewAdviseSink** o **IMAPIFormAdviseSink** en lugar de **IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) e [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) cada uno tiene varios métodos, uno para cada uno de los eventos posibles que el origen de asesoramiento correspondiente es capaz de generar. Por ejemplo, **IMAPIFormAdviseSink** tiene dos métodos: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) para controlar un cambio en el estado del visor de formularios y [IMAPIFormAdviseSink::OnActivateNext para](imapiformadvisesink-onactivatenext.md) mostrar un nuevo mensaje con el formulario correcto. 
  
La estrategia de control de eventos para formularios es similar a la estrategia de control de eventos implementada en OLE. Los clientes no se registran para tipos de eventos específicos como lo hacen para la mayoría de los objetos MAPI. Se supone que el registro para la notificación les permite recibir cualquier tipo de evento que pueda generar el origen de notificación en particular. Dado **que IMAPIAdviseSink::OnNotify** debe escribirse para controlar todos los eventos registrados, implementarlo puede ser complejo para los clientes que se registran para muchos eventos diferentes. Dado que los métodos del formulario aconsejan a los objetos receptores dirigirse a un único evento, la implementación de estos métodos es más sencilla. 
  

