---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438774"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un nuevo mensaje.
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameters

 _fComposeInFolder_
  
> a Indica en qué carpeta debe componerse el mensaje. Si la variable es FALSE, se omite el parámetro _pFolderFocus_ y el visor del formulario puede redactar el mensaje en cualquier carpeta. Si la variable es TRUE y NULL se pasa en el parámetro _pFolderFocus_ , el mensaje se crea en la carpeta actual. Si la variable es TRUE y se pasa un valor no NULL en _pFolderFocus_, el mensaje se redacta en la carpeta a la que apunta _pFolderFocus_.
    
 _pFolderFocus_
  
> a Un puntero a la carpeta en la que se crea el nuevo mensaje.
    
 _pPersistMessage_
  
> a Un puntero al objeto de formulario para el nuevo formulario.
    
 _ppMessage_
  
> contempla Un puntero a un puntero al nuevo mensaje.
    
 _ppMessageSite_
  
> contempla Un puntero a un puntero a un objeto de sitio de mensaje para el nuevo mensaje.
    
 _ppViewContext_
  
> contempla Un puntero a un puntero a un contexto de vista que es apropiado para pasar a un nuevo formulario con el nuevo mensaje. Si el formulario implementa su propio contexto de vista, se puede pasar NULL en el parámetro _ppViewContext_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIMessageSite:: NewMessage** para crear un mensaje nuevo. El formulario usa **NewMessage** para obtener un nuevo mensaje y el sitio del mensaje asociado desde su vista. A continuación, puede modificar el nuevo mensaje. 
  
También puede obtener un contexto de vista asociado pasando un valor no nulo en el parámetro _ppViewContext_ . Este contexto de vista se puede usar directamente o se puede Agregar y pasar al nuevo mensaje. Si se requiere una implementación completa, pase NULL en _ppViewContext_.
  
Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: NewMessage  <br/> |MFCMAPI usa el método **IMAPIMessageSite:: NewMessage** para crear un nuevo mensaje, crear una instancia de un nuevo visor de formularios y llamar a **SetPersist** para establecer el mensaje en el visor de formularios. Por último, devuelve el visor del formulario como el sitio del mensaje.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

