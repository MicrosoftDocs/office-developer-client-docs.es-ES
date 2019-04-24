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
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342780"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el estado asociado a un mensaje (por ejemplo, si el mensaje está marcado para su eliminación).
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada para el mensaje cuyo estado es establecido.
    
 _ulNewStatus_
  
> a Nuevo estado que se va a asignar. 
    
 _ulNewStatusMask_
  
> a Máscara de máscara de marcadores que se aplica al nuevo estado e indica las marcas que se van a establecer. Se pueden establecer los siguientes indicadores:
    
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
    
 _lpulOldStatus_
  
> contempla Un puntero al estado anterior del mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del mensaje se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: SetMessageStatus** establece el estado del mensaje en el valor que se almacena en su propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La forma en que los bits de estado del mensaje se establecen, borran y usan dependen por completo de la implementación, excepto que los bits del 0 al 15 están reservados y deben ser cero. 
  
La implementación de este método de un proveedor de transporte remoto debe seguir la semántica que se describe aquí. No hay ninguna consideración especial. Los clientes usan este método para establecer los bits MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE para indicar que un mensaje en particular debe descargarse o eliminarse del almacén de mensajes remoto. Un proveedor de transporte remoto no tiene que implementar el método [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) relacionado. Los clientes deben buscar en la tabla de contenido de la carpeta para determinar el estado de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la propiedad **PR_MSG_STATUS** de un mensaje para negociar una operación de bloqueo de mensajes con otros clientes. Designar un bit como bit de bloqueo. Para determinar si se estableció el bit de bloqueo, examine el valor anterior del estado del mensaje en el parámetro _lpulOldStatus_ . Use los otros bits del parámetro _ulNewStatus_ para realizar un seguimiento del estado del mensaje sin interferir con el bit de bloqueo. 
  
## <a name="see-also"></a>Vea también



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

