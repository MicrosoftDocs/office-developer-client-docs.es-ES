---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429022"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el estado del visor actual. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parámetros

 _lpulStatus_
  
> [salida] Puntero a una máscara de bits de indicadores que proporciona el estado del visor. Se pueden establecer las siguientes marcas:
    
VCSTATUS_CATEGORY 
  
> Hay un mensaje siguiente o anterior en otra categoría. 
    
VCSTATUS_DELETE 
  
> El formulario permite quitar mensajes. 
    
VCSTATUS_INTERACTIVE 
  
> El formulario debe mostrar una interfaz de usuario. Si no se establece esta marca, el formulario debería suprimir la visualización de una interfaz de usuario incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario. 
    
VCSTATUS_MODAL 
  
> El formulario es modal para el visor. 
    
VCSTATUS_NEXT 
  
> Hay un siguiente mensaje en la vista. 
    
VCSTATUS_PREV 
  
> Hay un mensaje anterior en la vista. 
    
VCSTATUS_READONLY 
  
> El mensaje se debe abrir en modo de solo lectura. Las operaciones de eliminación, envío y movimiento deben deshabilitarse. 
    
VCSTATUS_UNREAD 
  
> Hay un mensaje no leído siguiente o anterior en la vista.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del visor se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewContext::GetViewStatus** para determinar si hay más mensajes para activar en una  vista de formulario en una o  ambas direcciones, es decir, en la dirección en la que un comando Next activa los mensajes, en la dirección en que un comando Anterior activa los mensajes o en ambas direcciones. El valor al que apunta el parámetro  _lpulStatus_ se usa para determinar si las marcas VCSTATUS_NEXT y VCSTATUS_PREV son válidas para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Si se VCSTATUS_DELETE marca, pero no la marca VCSTATUS_READONLY, el mensaje se puede eliminar mediante el método [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md) 
  
Normalmente, los formularios deshabilitan los comandos de menú y los botones si no son válidos para el contexto del visor. Un visor puede alertar a un formulario sobre un cambio de estado llamando a su [método IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md) 
  
La VCSTATUS_MODAL se establece si el formulario debe ser modal para la ventana cuyo identificador se pasa en la llamada [imapiform::D oVerb](imapiform-doverb.md) anterior. Si VCSTATUS_MODAL se establece, el formulario puede usar el subproceso en el que se realizó la llamada **a DoVerb** hasta que se cierre el formulario. Si VCSTATUS_MODAL no se establece, el formulario no debe ser modal para esta ventana y no debe usar el subproceso. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implementa el **método IMAPIViewContext::GetViewStatus** en esta función.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

