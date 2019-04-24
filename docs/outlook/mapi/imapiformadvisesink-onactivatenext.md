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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329438"
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

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> a Un puntero a la clase de mensaje del siguiente mensaje.
    
 _ulMessageStatus_
  
> a Una máscara de bits de indicadores definidos por el cliente o definidos por el proveedor, copiado de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del siguiente mensaje que se va a mostrar, que proporciona información de estado relativa a la tabla de contenido en la que se incluye el mensaje. a.
    
 _ulMessageFlags_
  
> a Un puntero a una máscara de máscara de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del siguiente mensaje para mostrar que indica el estado actual del mensaje.
    
 _ppPersistMessage_
  
> contempla Un puntero a un puntero a la implementación de [IPersistMessage](ipersistmessageiunknown.md) para el objeto de formulario usado para el nuevo formulario, si se requiere un nuevo formulario. Se puede devolver un puntero a NULL si el objeto Form actual puede usarse para mostrar y guardar el siguiente mensaje. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente y el formulario puede controlar el siguiente mensaje.
    
S_FALSE 
  
> El formulario no controla la clase de mensaje del siguiente mensaje.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormAdviseSink:: OnActivateNext** para ayudar a que el formulario determine si puede mostrar el siguiente mensaje en una carpeta. El siguiente mensaje puede ser un mensaje de cualquier clase, pero suele ser de la misma clase o de una clase relacionada. Esto hace que el proceso de lectura de varios mensajes de la misma clase sea más eficaz al permitir a las aplicaciones cliente volver a usar objetos de formulario siempre que sea posible. 
  
La mayoría de los objetos de formulario usarán la clase de mensaje señalada por el parámetro _lpszMessageClass_ para determinar si pueden controlar el siguiente mensaje. Normalmente, un formulario puede controlar mensajes que pertenecen a clases de las que la clase predeterminada del formulario es una subclase, además de los mensajes que pertenecen a la clase predeterminada. Sin embargo, un formulario puede usar otros factores para determinar sin duda si se puede controlar un mensaje, como el estado enviado o no enviado del siguiente mensaje. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Devuelve S_OK y NULL en el parámetro _ppPersistMessage_ si el formulario puede controlar la clase de mensaje. Si el formulario puede crear un nuevo formulario que pueda controlar el mensaje que el formulario no puede controlar, siga estos pasos: 
  
1. Llame al generador de clases del formulario para crear una instancia de un nuevo objeto Form.
    
2. Almacene esa instancia en el contenido del parámetro de puntero _ppPersistMessage_ . 
    
3. Devuelve S_OK.
    
El visor del formulario cargará el mensaje mediante el método [IPersistMessage:: Load](ipersistmessage-load.md) que pertenece al objeto al que apunta _ppPersistMessage_.
  
Si ni el formulario ni el formulario que se pueden crear pueden controlar el siguiente mensaje, se devuelve S_FALSE. Sin embargo, en general, los formularios no deben devolver este valor porque provoca un rendimiento reducido en el visor de formularios.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CMyMAPIFormViewer:: ActivateNext  <br/> |MFCMAPI usa el método **IMAPIFormAdviseSink:: OnActivateNext** para implementar el método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

