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
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587134"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que los visores de formulario trabajar con contextos de vista de formulario y notificación de formulario, para llevar a cabo los verbos de formulario y cerrar formularios.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Objetos de formulario  <br/> |
|Se implementa mediante:  <br/> |Servidores de formulario  <br/> |
|Llamado por:  <br/> |Visores de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIForm  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Establece un contexto de vista para el formulario.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Devuelve el contexto de la vista actual para el formulario.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Cierra el formulario.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Las solicitudes que el formulario realiza tareas con independencia de se asocia a un verbo específico.  <br/> |
|[Aviso](imapiform-advise.md) <br/> |Registra un visor de formulario para las notificaciones sobre los eventos que afectan a la forma.  <br/> |
|[Desaconsejar](imapiform-unadvise.md) <br/> |Cancela un registro para las notificaciones con un visor de formulario establecido previamente mediante una llamada a **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen al objeto form.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

