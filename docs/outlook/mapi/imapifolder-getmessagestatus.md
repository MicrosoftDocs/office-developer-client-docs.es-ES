---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e5ccadbd6df664b6650487f340508ae4548a1c2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583270"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Obtiene el estado asociado a un mensaje de una carpeta determinada (por ejemplo, si ese mensaje está marcado para su eliminación).
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero a para el mensaje cuyo estado se obtiene el identificador de entrada.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulMessageStatus_
  
> [out] Un puntero a un puntero a una máscara de bits de marcadores que indican el estado del mensaje. De 0 a 15 bits están reservados y deben ser cero; 16 a través de 31 bits están disponibles para su uso específico de la implementación. Se pueden establecer los siguientes indicadores:
    
MSGSTATUS_DELMARKED 
  
> El mensaje se ha marcado para su eliminación.
    
MSGSTATUS_HIDDEN 
  
> El mensaje no es se muestre. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Es el mensaje que se mostrará resaltado.
    
MSGSTATUS_REMOTE_DELETE 
  
> El mensaje se ha marcado para su eliminación en el almacén de mensajes remoto sin descargar en el cliente local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> El mensaje se ha marcado para la descarga desde el almacén de mensajes remoto para el cliente local.
    
MSGSTATUS_TAGGED 
  
> El mensaje se ha etiquetado con un fin definidas por el cliente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del mensaje se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::GetMessageStatus** devuelve el estado de un mensaje. Estado del mensaje se almacena en la propiedad del mensaje **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cómo los bits de estado del mensaje se establece, desactivados y usa depende completamente de la implementación, excepto que los bits 0 a 15 están reservados y deben ser cero. Si almacena los mensajes en el subárbol IPM, MAPI reserva bits 16 a través de 31 para su uso por los clientes IPM. Si almacena los mensajes en otros subárboles, puede utilizar bits 16 a través de 31 para sus propios fines.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI usa el método **IMAPIFolder::GetMessageStatus** para obtener el estado del siguiente mensaje que se mostrará.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal y OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPIFolder::GetMessageStatus** para obtener el estado del mensaje que se mostrará para pasar al Visor de formulario, que es CMyMAPIFormViewer o [IMAPISession:: ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propiedad canónico PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

