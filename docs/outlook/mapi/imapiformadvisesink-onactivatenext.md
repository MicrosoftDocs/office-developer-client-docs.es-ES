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
ms.openlocfilehash: 7e8fb69e7d25420186d7269943c5d957311e813d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581760"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Indica si el formulario puede controlar la clase de mensaje del mensaje siguiente para mostrar.
  
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
  
> [entrada] Un puntero a la clase de mensaje del mensaje siguiente.
    
 _ulMessageStatus_
  
> [entrada] Una máscara de bits de indicadores definidas por el cliente o definidas por el proveedor, copiada desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje siguiente para mostrar, que proporciona información de estado con respecto a la tabla de contenido que se incluye el mensaje en.
    
 _ulMessageFlags_
  
> [entrada] Un puntero a una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje siguiente para mostrar indica el estado actual del mensaje.
    
 _ppPersistMessage_
  
> [out] Un puntero a un puntero a la implementación de [IPersistMessage](ipersistmessageiunknown.md) para el objeto de formulario utilizado para el nuevo formulario, si es necesario un nuevo formulario. Puede ser devuelve un puntero en NULL si el objeto de formulario actual se puede usar para mostrar y guardar el mensaje siguiente. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se realizó correctamente y el formulario puede administrar el mensaje siguiente.
    
S_FALSE 
  
> El formulario no controla la clase de mensaje del mensaje siguiente.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormAdviseSink::OnActivateNext** para determinar el formulario si puede mostrar el siguiente mensaje en una carpeta. El siguiente mensaje podría ser un mensaje de cualquier clase, pero normalmente es de la misma clase o una clase relacionada. Esto hace que el proceso de lectura de varios mensajes de la misma clase más eficaz mediante la habilitación de las aplicaciones de cliente volver a usar los objetos de formulario siempre que sea posible. 
  
La mayoría de los objetos de formulario usará la clase de mensaje que apunta el parámetro _lpszMessageClass_ para determinar si pueden procesar el mensaje siguiente. Normalmente, un formulario puede administrar los mensajes que pertenecen a las clases de que la clase del formulario de forma predeterminada es una subclase, además de los mensajes que pertenecen a la clase predeterminada. Sin embargo, un formulario puede usar otros factores para determinar sin pregunta si un mensaje puede ser controlado, como el estado enviado y no enviado del mensaje siguiente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Devolver S_OK y NULL en el parámetro _ppPersistMessage_ si el formulario puede controlar la clase de mensaje. Si el formulario puede crear un nuevo formulario que puede administrar el mensaje que el formulario no puede controlar, siga estos pasos: 
  
1. Llamar a fábrica de clase del formulario para crear una instancia de un nuevo objeto de formulario.
    
2. Almacenar esa instancia en el contenido del parámetro de puntero _ppPersistMessage_ . 
    
3. Devuelve S_OK.
    
El Visor de formulario cargará el mensaje mediante el método [IPersistMessage::Load](ipersistmessage-load.md) que pertenece el objeto al que señala por _ppPersistMessage_.
  
Si ni el formulario ni en un formulario que se puede crear puede controlar el mensaje siguiente, devuelve S_FALSE. Sin embargo, en general, formularios no deben devolver que este valor porque hace disminución del rendimiento en el Visor de formulario.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI utiliza el método **IMAPIFormAdviseSink::OnActivateNext** para implementar el método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propiedad canónico PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónico PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

