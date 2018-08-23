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
ms.openlocfilehash: 992d51526c45334f6db3738e36994f4bb9c07c6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572259"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el estado actual del Visor. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parámetros

 _lpulStatus_
  
> [out] Puntero a una máscara de bits de marcadores que indica el estado del Visor del. Se pueden establecer los siguientes indicadores:
    
VCSTATUS_CATEGORY 
  
> Hay un mensaje siguiente o anterior en otra categoría. 
    
VCSTATUS_DELETE 
  
> El formulario permite que los mensajes que se va a quitar. 
    
VCSTATUS_INTERACTIVE 
  
> El formulario debe mostrar una interfaz de usuario. Si no se establece este indicador, el formulario debe suprimir mostrar la interfaz de usuario incluso en respuesta a un verbo que normalmente hace que una interfaz de usuario que se mostrará. 
    
VCSTATUS_MODAL 
  
> El formulario es modal al Visor. 
    
VCSTATUS_NEXT 
  
> Hay un mensaje siguiente en la vista. 
    
VCSTATUS_PREV 
  
> Hay un mensaje anterior en la vista. 
    
VCSTATUS_READONLY 
  
> El mensaje es para abrirse en modo de sólo lectura. Eliminar, enviar y mover las operaciones deben deshabilitarse. 
    
VCSTATUS_UNREAD 
  
> Hay un mensaje no leído siguiente o anterior en la vista.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Estado del Visor se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario, llame al método **IMAPIViewContext::GetViewStatus** para determinar si hay más mensajes que se activará en una vista de formulario en cualquiera o ambas direcciones es decir, en la dirección en la que se activa un comando **a continuación** los mensajes, en el dirección en la que un comando **anterior** activa de los mensajes, o en ambas direcciones. El valor al que señala el parámetro _lpulStatus_ se usa para determinar si los indicadores VCSTATUS_NEXT y VCSTATUS_PREV son válidos para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Si el indicador VCSTATUS_DELETE es set, pero no la marca VCSTATUS_READONLY, a continuación, el mensaje se puede eliminar mediante el método [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) . 
  
Normalmente, formularios deshabilitación botones y comandos de menú si no son válidos para el contexto del Visor. Un visor puede un formulario a un cambio en el estado de alerta llamando a su método [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) . 
  
Se establece la marca VCSTATUS_MODAL si el formulario debe ser modal a la ventana cuyo controlador se pasa en la llamada de [IMAPIForm::DoVerb](imapiform-doverb.md) anterior. Si se establece VCSTATUS_MODAL, el formulario puede usar el subproceso en el que se realizó la llamada **DoVerb** hasta que se cierra el formulario. Si VCSTATUS_MODAL no está establecido, el formulario no debe ser modal a esta ventana y no debe usar el subproceso. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implementa el método **IMAPIViewContext::GetViewStatus** en esta función.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

