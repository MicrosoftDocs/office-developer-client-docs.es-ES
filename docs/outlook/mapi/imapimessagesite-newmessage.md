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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817355"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _fComposeInFolder_
  
> [entrada] Indica en qué carpeta se debe estar compuestas por el mensaje. Si la variable es FALSE, se omite el parámetro _pFolderFocus_ y el Visor de formulario puede redactar el mensaje en cualquier carpeta. Si la variable es TRUE y se pasa NULL en el parámetro _pFolderFocus_ , el mensaje se compone de la carpeta actual. Si la variable es TRUE y se pasa un valor no nulo en _pFolderFocus_, el mensaje se compone en la carpeta indicada por _pFolderFocus_.
    
 _pFolderFocus_
  
> [entrada] Un puntero a la carpeta donde se crea el nuevo mensaje.
    
 _pPersistMessage_
  
> [entrada] Un puntero al objeto de formulario para el nuevo formulario.
    
 _ppMessage_
  
> [out] Un puntero a un puntero al mensaje nuevo.
    
 _ppMessageSite_
  
> [out] Un puntero a un puntero a un objeto de sitio de mensaje para el mensaje nuevo.
    
 _ppViewContext_
  
> [out] Un puntero a un puntero a un contexto de vista que es adecuado para pasar a un nuevo formulario con el nuevo mensaje. Si el formulario implementa su propio contexto de vista, se puede pasar NULL en el parámetro _ppViewContext_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIMessageSite::NewMessage** para crear un nuevo mensaje. El formulario usa **NewMessage** para obtener un nuevo mensaje y el sitio de mensaje asociado desde su vista. A continuación, puede modificar el mensaje de nuevo. 
  
También puede obtener un contexto de la vista asociada al pasar un valor no nulo en el parámetro _ppViewContext_ . En este contexto de vista se puede utilizar directamente, o puede ser agregado y se pasan al mensaje nuevo. Si se requiere una implementación completa, pase NULL en _ppViewContext_.
  
Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI usa el método **IMAPIMessageSite::NewMessage** para crear un nuevo mensaje, crear una instancia de un nuevo Visor de formulario y llame a **SetPersist** para establecer el mensaje en el Visor del formulario. Por último, devuelve el Visor de formulario como el sitio de mensaje.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

