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
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317139"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica al formulario que se ha completado una operación de guardado. 
  
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
  
> La notificación se ha realizado correctamente.
    
E_INVALIDARG 
  
> El _parámetro pMessage_ es NULL y el formulario está en el estado [HandsOffFromNormal](handsofffromnormal-state.md) o [HandsOffAfterSave.](handsoffaftersave-state.md) 
    
E_UNEXPECTED 
  
> El formulario no está en uno de los siguientes estados:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Comentarios

Un visor de formulario llama al método **IPersistMessage::SaveCompleted** para notificar al formulario que se han guardado todos los cambios pendientes. Solo se debe llamar a **SaveCompleted** cuando el formulario se encuentra en uno de los siguientes estados: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Hay varias acciones posibles que puede realizar el método **SaveCompleted,** en función de lo que contenga el parámetro de puntero del mensaje y del estado en que se encuentra el mensaje. Sin embargo, cuando una acción se realiza correctamente, guarde siempre el estado actual del mensaje al que apunta el parámetro _pMessage_ y haga la transición del formulario a [su estado Normal.](normal-state.md) 
  
En la tabla siguiente se describen las condiciones que afectan a las acciones que debe realizar en la implementación de **SaveCompleted**.
  
|**Condición**|**Acción**|
|:-----|:-----|
|El  _parámetro pMessage_ es NULL y el parámetro  _fSameAsLoad_ del [método IPersistMessage::Save](ipersistmessage-save.md) se establece en TRUE.  <br/> |Llame al [método IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.  <br/> |
|El  _parámetro pMessage_ es NULL y el parámetro  _fSameAsLoad_ del **método IPersistMessage::Save** se establece en FALSE.  <br/> |Devuelve S_OK.  <br/> |
|El formulario está en estado HandsOffFromNormal.  <br/> |Libere el mensaje actual y reemplácela por el mensaje al que apunta el _parámetro pMessage._ Llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del mensaje de reemplazo y devuelva S_OK.  <br/> |
|El formulario está en estado HandsOffAfterSave.  <br/> |Llame al **método IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.  <br/> |
|El formulario está en estado [NoScribable.](noscribble-state.md)  <br/> |Libere el mensaje actual y reemplácela por el mensaje que apunta  _pMessage_. Llame al método **IUnknown::AddRef** del mensaje de reemplazo. Llame al **método IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.  <br/> |
|El formulario se encuentra en uno de los estados HandsOff y el  _parámetro pMessage_ se establece en NULL.  <br/> |Devuelve E_INVALIDARG.  <br/> |
|El formulario está en un estado distinto de uno de los estados HandsOff o NoScribble.  <br/> |Devuelve E_UNEXPECTED.  <br/> |
   
Para obtener más información acerca de cómo guardar objetos de almacenamiento, vea la documentación de los [métodos IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) o [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) 
  
## <a name="see-also"></a>Consulte también

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Estados de formulario](form-states.md)
