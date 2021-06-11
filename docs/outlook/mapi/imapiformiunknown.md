---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436387"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite a los visores de formulario trabajar con contextos de vista de formulario y notificación de formulario, realizar verbos de formulario y cerrar formularios.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
|Expuesto por:  <br/> |Objetos de formulario  <br/> |
|Implementado por:  <br/> |Servidores de formulario  <br/> |
|Llamado por:  <br/> |Visores de formularios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIForm  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Establece un contexto de vista para el formulario.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Devuelve el contexto de vista actual del formulario.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Cierra el formulario.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Solicita que el formulario realice las tareas que asocie con un verbo específico.  <br/> |
|[Aconsejar](imapiform-advise.md) <br/> |Registra un visor de formularios para notificaciones sobre eventos que afectan al formulario.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Cancela un registro para las notificaciones con un visor de formulario establecido anteriormente llamando a **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

