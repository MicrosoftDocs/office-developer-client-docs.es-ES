---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7813636abc1c4d6ad756c7cf670e21d4acb7f540
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592748"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se notifica el formulario que guarda una operación se ha completado. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parámetros

_pMessage_
  
> [entrada] Un puntero al mensaje recién guardado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación fue correcta.
    
E_INVALIDARG 
  
> El parámetro _pMessage_ es NULL y el formulario está en el estado [HandsOffFromNormal](handsofffromnormal-state.md) o [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> El formulario no está en uno de los siguientes estados:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Comentarios

Se llama al método de **IPersistMessage::SaveCompleted** por un visor de formulario para notificar el formulario que se han guardado todos los cambios pendientes. **SaveCompleted** debe llamarse sólo cuando el formulario está en uno de los siguientes estados: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

Existen varias acciones posibles que puede realizar el método **SaveCompleted** , dependiendo de qué el mensaje contiene el parámetro de puntero y estado en que el mensaje está en. Sin embargo, cuando una acción es correcta, siempre guarde el estado actual del mensaje que señala el parámetro _pMessage_ y transición el formulario a su estado [Normal](normal-state.md) . 
  
En la siguiente tabla se describe las condiciones que afectan a las acciones que debe realizar en su implementación de **SaveCompleted**.
  
|**Condición**|**Acción**|
|:-----|:-----|
|El parámetro _pMessage_ es NULL y el parámetro _fSameAsLoad_ del método [IPersistMessage::Save](ipersistmessage-save.md) se establece en TRUE.  <br/> |Llame al método [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.  <br/> |
|El parámetro _pMessage_ es NULL y el parámetro _fSameAsLoad_ del método **IPersistMessage::Save** se establece en FALSE.  <br/> |Devuelve S_OK.  <br/> |
|El formulario está en el estado de HandsOffFromNormal.  <br/> |Liberar el mensaje actual y reemplácelo con el mensaje que apunta el parámetro _pMessage_ . Llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del mensaje de reemplazo y devolver S_OK.  <br/> |
|El formulario está en el estado de HandsOffAfterSave.  <br/> |Llame al método **IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.  <br/> |
|El formulario está en el estado de [NoScribble](noscribble-state.md) .  <br/> |Liberar el mensaje actual y reemplácelo con el mensaje que apunta _pMessage_. Llamar al método **IUnknown:: AddRef** del mensaje de reemplazo. Llame al método **IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.  <br/> |
|El formulario está en uno de los Estados de HandsOff y el parámetro _pMessage_ se establece en NULL.  <br/> |Devolver E_INVALIDARG.  <br/> |
|El formulario está en un estado que no sea uno de los Estados de HandsOff o el estado de NoScribble.  <br/> |Devolver E_UNEXPECTED.  <br/> |
   
Para obtener más información acerca de cómo guardar objetos de almacenamiento, vea la documentación de los métodos [IPersistStorage::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) o [:: SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Recursos adicionales

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Estados de formulario](form-states.md)
