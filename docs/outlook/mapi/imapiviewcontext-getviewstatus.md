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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351180"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el estado actual del visor. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> contempla Puntero a una máscara de máscara de indicadores que proporciona el estado del visor. Se pueden establecer los siguientes indicadores:
    
VCSTATUS_CATEGORY 
  
> Hay un mensaje siguiente o anterior en otra categoría. 
    
VCSTATUS_DELETE 
  
> El formulario permite quitar los mensajes. 
    
VCSTATUS_INTERACTIVE 
  
> El formulario debe mostrar una interfaz de usuario. Si no se establece esta marca, el formulario debe suprimir la visualización de una interfaz de usuario incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario. 
    
VCSTATUS_MODAL 
  
> El formulario es modal para el visor. 
    
VCSTATUS_NEXT 
  
> Hay un mensaje siguiente en la vista. 
    
VCSTATUS_PREV 
  
> Hay un mensaje anterior en la vista. 
    
VCSTATUS_READONLY 
  
> El mensaje debe abrirse en modo de solo lectura. Las operaciones de eliminar, enviar y mover deben estar deshabilitadas. 
    
VCSTATUS_UNREAD 
  
> Hay un mensaje no leído siguiente o anterior en la vista.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del visor se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewContext:: GetViewStatus** para determinar si hay más mensajes que se van a activar en una vista de formulario en una o ambas direcciones, es decir, en la dirección en la que un comando **siguiente** activa los mensajes, en el Dirección en la que un comando **anterior** activa los mensajes o en ambas direcciones. El valor al que señala el parámetro _lpulStatus_ se usa para determinar si las marcas VCSTATUS_NEXT y VCSTATUS_PREV son válidas para [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md). Si se establece la marca VCSTATUS_DELETE, pero no la marca VCSTATUS_READONLY, el mensaje se puede eliminar mediante el método [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) . 
  
Por lo general, los formularios deshabilitan botones y comandos de menú si no son válidos para el contexto del visor. Un visor puede enviar una alerta de un formulario a un cambio de estado llamando a su método [IMAPIFormAdviseSink:: onchange](imapiformadvisesink-onchange.md) . 
  
La marca VCSTATUS_MODAL se establece si el formulario tiene que ser modal a la ventana cuyo controlador se pasa en la anterior [IMAPIForm::D llamada overb](imapiform-doverb.md) . Si se establece VCSTATUS_MODAL, el formulario puede usar el subproceso en el que se realizó la llamada a **doverb** hasta que se cierre el formulario. Si no se establece VCSTATUS_MODAL, el formulario no debe ser modal a esta ventana y no debe usar el subproceso. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetViewStatus  <br/> |MFCMAPI implementa el método **IMAPIViewContext:: GetViewStatus** en esta función.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

