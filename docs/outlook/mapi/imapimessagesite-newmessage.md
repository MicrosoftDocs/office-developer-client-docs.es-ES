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
  
Crea un mensaje nuevo.
  
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
  
> [in] Indica en qué carpeta se debe componer el mensaje. Si la variable es FALSE, se omite el  _parámetro pFolderFocus_ y el visor de formularios puede redactar el mensaje en cualquier carpeta. Si la variable es TRUE y NULL se pasa en el  _parámetro pFolderFocus,_ el mensaje se compone en la carpeta actual. Si la variable es TRUE y se pasa un valor que no es NULL en  _pFolderFocus_, el mensaje se compone en la carpeta señalada por  _pFolderFocus_.
    
 _pFolderFocus_
  
> [in] Puntero a la carpeta donde se crea el nuevo mensaje.
    
 _pPersistMessage_
  
> [in] Puntero al objeto de formulario del nuevo formulario.
    
 _ppMessage_
  
> [salida] Puntero a un puntero al nuevo mensaje.
    
 _ppMessageSite_
  
> [salida] Puntero a un puntero a un objeto de sitio de mensaje para el nuevo mensaje.
    
 _ppViewContext_
  
> [salida] Puntero a un puntero a un contexto de vista adecuado para pasar a un nuevo formulario con el nuevo mensaje. Si el formulario implementa su propio contexto de vista, se puede pasar NULL en el _parámetro ppViewContext._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los objetos Form llaman **al método IMAPIMessageSite::NewMessage** para crear un nuevo mensaje. El formulario usa **NewMessage** para obtener un nuevo mensaje y el sitio de mensaje asociado desde su vista. A continuación, puede modificar el nuevo mensaje. 
  
También puede obtener un contexto de vista asociado pasando un valor que no sea NULL en el _parámetro ppViewContext._ Este contexto de vista se puede usar directamente o puede agregarse y pasarse al nuevo mensaje. Si se requiere una implementación completa, pase NULL en  _ppViewContext_.
  
Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI usa el método **IMAPIMessageSite::NewMessage** para crear un nuevo mensaje, crear una instancia de un nuevo visor de formularios y llamar a **SetPersist** para establecer el mensaje en el visor de formularios. Por último, devuelve el visor de formularios como el sitio del mensaje.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

