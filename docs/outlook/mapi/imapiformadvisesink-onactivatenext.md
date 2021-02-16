---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411767"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si el formulario puede controlar la clase de mensaje del siguiente mensaje que se va a mostrar.
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Parámetros

 _lpszMessageClass_
  
> [entrada] Puntero a la clase de mensaje del siguiente mensaje.
    
 _ulMessageStatus_
  
> [entrada] Máscara de bits de marcas definidas por el cliente o definidas por el proveedor, copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del siguiente mensaje que se va a mostrar, que proporciona información de estado sobre la tabla de contenido en la que se incluye el mensaje.
    
 _ulMessageFlags_
  
> [entrada] Puntero a una máscara de bits de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del siguiente mensaje para mostrar que indica el estado actual del mensaje.
    
 _ppPersistMessage_
  
> [salida] Puntero a un puntero a la implementación [de IPersistMessage](ipersistmessageiunknown.md) para el objeto de formulario usado para el nuevo formulario, si es necesario un nuevo formulario. Se puede devolver un puntero a NULL si se puede usar el objeto de formulario actual para mostrar y guardar el siguiente mensaje. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente y el formulario puede controlar el siguiente mensaje.
    
S_FALSE 
  
> El formulario no controla la clase de mensaje del siguiente mensaje.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormAdviseSink::OnActivateNext** para ayudar al formulario a determinar si puede mostrar el siguiente mensaje en una carpeta. El siguiente mensaje podría ser un mensaje de cualquier clase, pero normalmente es de la misma clase o una clase relacionada. Esto hace que el proceso de lectura de varios mensajes de la misma clase sea más eficaz al permitir que las aplicaciones cliente reutilicen objetos de formulario siempre que sea posible. 
  
La mayoría de los objetos de formulario usarán la clase de mensaje a la que apunta el parámetro  _lpszMessageClass_ para determinar si pueden controlar el siguiente mensaje. Normalmente, un formulario puede controlar mensajes que pertenecen a clases de las que la clase predeterminada del formulario es una subclase, además de los mensajes que pertenecen a la clase predeterminada. Sin embargo, un formulario puede usar otros factores para determinar sin duda si se puede controlar un mensaje, como el estado enviado o no enviado del siguiente mensaje. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Devuelve S_OK y NULL en el  _parámetro ppPersistMessage_ si el formulario puede controlar la clase de mensaje. Si el formulario puede crear un formulario nuevo que pueda controlar el mensaje que el formulario no puede controlar, siga estos pasos: 
  
1. Llame a la fábrica de clases del formulario para crear una instancia de un nuevo objeto de formulario.
    
2. Almacene esa instancia en el contenido del parámetro de puntero _ppPersistMessage._ 
    
3. Devuelve S_OK.
    
El visor de formularios cargará el mensaje mediante el método [IPersistMessage::Load](ipersistmessage-load.md) que pertenece al objeto al que apunta  _ppPersistMessage_.
  
Si ni el formulario ni el formulario que puede crear pueden controlar el siguiente mensaje, S_FALSE. Sin embargo, en general, los formularios no deben devolver este valor porque provoca una disminución del rendimiento en el visor de formularios.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI usa el método **IMAPIFormAdviseSink::OnActivateNext** para implementar el método [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

