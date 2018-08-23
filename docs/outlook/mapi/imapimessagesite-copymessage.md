---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 074a806a710ce8c11adba815951c93c25d8cae7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579259"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia el mensaje actual en una carpeta.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parámetros

 _pFolderDestination_
  
> [entrada] Un puntero a la carpeta donde el mensaje se va a copiar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> La operación no es compatible con este sitio de mensaje.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIMessageSite::CopyMessage** para copiar el mensaje actual en una nueva carpeta. **CopyMessage** no cambia el mensaje que se muestra actualmente al usuario y ninguna interfaz para el mensaje recién creada se devuelve al formulario. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Una implementación típica del método **CopyMessage** realiza las tareas siguientes: 
  
1. Crea un nuevo mensaje para el mensaje actual que se copiarán a.
    
2. Llama al método [IPersistMessage::Save](ipersistmessage-save.md) con un puntero al nuevo mensaje en el parámetro _pMessage_ y FALSE en el parámetro _fSameAsLoad_ . 
    
3. Llama al método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , pasando NULL en el parámetro _pMessage_ . 
    
4. Llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el nuevo mensaje. 
    
Para obtener una lista de las interfaces que están relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |No se ha implementado.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

