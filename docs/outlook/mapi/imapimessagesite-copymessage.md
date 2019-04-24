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
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321549"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia el mensaje actual en una carpeta.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parameters

 _pFolderDestination_
  
> a Puntero a la carpeta en la que se va a copiar el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> La operación no es compatible con este sitio de mensajes.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIMessageSite:: CopyMessage** para copiar el mensaje actual en una carpeta nueva. **CopyMessage** no cambia el mensaje que se está mostrando actualmente al usuario y no se devuelve al formulario ninguna interfaz para el mensaje recién creado. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Una implementación típica del método **CopyMessage** realiza las siguientes tareas: 
  
1. Crea un nuevo mensaje para el mensaje actual al que se va a copiar.
    
2. Llama al método [IPersistMessage:: Save](ipersistmessage-save.md) con un puntero al nuevo mensaje en el parámetro _pMessage_ y false en el parámetro _fSameAsLoad_ . 
    
3. Llama al método [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) , pasando null en el parámetro _pMessage_ . 
    
4. Llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) en el nuevo mensaje. 
    
Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: CopyMessage  <br/> |No implementado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

