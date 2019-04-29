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
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418641"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene el estado asociado a un mensaje en una carpeta determinada (por ejemplo, si el mensaje está marcado para su eliminación).
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del mensaje cuyo estado se obtiene.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulMessageStatus_
  
> contempla Un puntero a un puntero a una máscara de máscara de marcas que indica el estado del mensaje. Los bits del 0 al 15 están reservados y deben ser cero; los bits 16 a 31 están disponibles para uso específico de la implementación. Se pueden establecer los siguientes indicadores:
    
MSGSTATUS_DELMARKED 
  
> El mensaje se ha marcado para su eliminación.
    
MSGSTATUS_HIDDEN 
  
> El mensaje no se va a mostrar. 
    
MSGSTATUS_HIGHLIGHTED 
  
> El mensaje se mostrará resaltado.
    
MSGSTATUS_REMOTE_DELETE 
  
> El mensaje se marcó para ser eliminado en el almacén de mensajes remoto sin descargarse al cliente local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> El mensaje se marcó para descargar del almacén de mensajes remoto en el cliente local.
    
MSGSTATUS_TAGGED 
  
> El mensaje se ha etiquetado para un propósito definido por el cliente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del mensaje se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: GetMessageStatus** devuelve el estado de un mensaje. El estado del mensaje se almacena en la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La forma en que los bits de estado del mensaje se establecen, borran y usan dependen por completo de la implementación, excepto que los bits del 0 al 15 están reservados y deben ser cero. Si almacena mensajes en el subárbol IPM, MAPI reserva los bits 16 a 31 para que los usen los clientes IPM. Si almacena mensajes en otros subárboles, puede usar bits 16 a 31 para sus propios fines.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetNextMessage  <br/> |MFCMAPI usa el método **IMAPIFolder:: GetMessageStatus** para obtener el estado del siguiente mensaje que se va a mostrar.  <br/> |
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal y OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPIFolder:: GetMessageStatus** para obtener el estado del mensaje que se mostrará para pasar al visor de formularios, que es CMyMAPIFormViewer o [IMAPISession:: ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

