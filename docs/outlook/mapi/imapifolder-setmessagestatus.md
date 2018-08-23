---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d06523625a20760faec7a6c73a6beaef757818b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575080"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el estado asociado a un mensaje (por ejemplo, si ese mensaje está marcado para su eliminación).
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada para el mensaje cuyo estado está establecido.
    
 _ulNewStatus_
  
> [entrada] El nuevo estado que se asignará. 
    
 _ulNewStatusMask_
  
> [entrada] Una máscara de bits de indicadores que se aplica al nuevo estado e indica los indicadores que se va a establecer. Se pueden establecer los siguientes indicadores:
    
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
    
 _lpulOldStatus_
  
> [out] Un puntero al estado anterior del mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del mensaje se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::SetMessageStatus** establece el estado del mensaje en el valor que se almacena en su propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cómo los bits de estado del mensaje se establece, desactivados y usa depende completamente de la implementación, excepto que los bits 0 a 15 están reservados y deben ser cero. 
  
Implementación del proveedor de transporte remoto de este método debe seguir la semántica que se describen aquí. No hay ninguna consideración especial. Los clientes de utilizar este método para configurar los bits MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE para indicar que un mensaje determinado se va a descargar o eliminar desde el almacén de mensajes remoto. Un proveedor de transporte remoto no tiene que implementar el método [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) relacionado. Los clientes deben buscar en la tabla de contenido de la carpeta para determinar el estado de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la propiedad **PR_MSG_STATUS** de un mensaje para la negociación de una operación de bloqueo de mensajes con otros clientes. Designar un poco como el bit de bloqueo. Para determinar si se ha establecido el bit de bloqueo, examine el valor anterior de estado del mensaje en el parámetro _lpulOldStatus_ . Use el resto de los bits en el parámetro _ulNewStatus_ para realizar un seguimiento del estado del mensaje sin interferir con el bit de bloqueo. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

