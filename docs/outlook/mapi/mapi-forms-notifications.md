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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351481"
---
# <a name="mapi-forms-notifications"></a>Notificaciones de formularios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El registro y la administración de notificaciones desde objetos de formulario es un proceso diferente que para otros objetos de MAPI. Informar a los receptores de las notificaciones de formulario implemente la interfaz **IMAPIViewAdviseSink** o **IMAPIFormAdviseSink** en lugar de **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) y [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) tiene varios métodos, uno para cada uno de los eventos posibles que el origen de la notificación correspondiente puede generar. Por ejemplo, **IMAPIFormAdviseSink** tiene dos métodos: [IMAPIFormAdviseSink:: onchange](imapiformadvisesink-onchange.md) para controlar un cambio en el estado del visor de formularios y [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md) para mostrar un nuevo mensaje con el formato correcto. 
  
La estrategia de control de eventos para formularios es similar a la estrategia de control de eventos implementada en OLE. Los clientes no se registran para tipos específicos de eventos de la misma manera que en la mayoría de los objetos MAPI. Se supone que el registro para la notificación les permite recibir cualquier tipo de evento que el origen de notificaciones puede generar. Dado que **IMAPIAdviseSink:: Notify** se debe escribir para controlar todos los eventos registrados, implementarlo puede ser complejo para los clientes que se registran para muchos eventos diferentes. Debido a que los métodos de la forma informar a los objetos receptores tienen como objetivo un solo evento, la implementación de estos métodos es más sencilla. 
  

