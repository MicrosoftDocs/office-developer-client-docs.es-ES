---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 329771bf79e30f07c9de0a311aa2a836ca507c38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580036"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina si un formulario puede controlar sus propio conflictos de mensaje. Un mensaje está en conflicto si se ha editado simultáneamente por más de un usuario. Esto puede ocurrir a los mensajes en las carpetas públicas.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parámetros

 _ulMessageFlags_
  
> [entrada] Un puntero a una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de un mensaje que indica el estado actual del mensaje.
    
 _ulMessageStatus_
  
> [entrada] Una máscara de bits de definidas por el cliente o definidas por el proveedor de indicadores que se copió desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de un mensaje que proporciona información adicional sobre el estado del mensaje.
    
 _szMessageClass_
  
> [entrada] Una cadena que da nombre de clase de mensaje del mensaje.
    
 _pFolderFocus_
  
> [entrada] Un puntero a la carpeta que contiene el mensaje. El parámetro _pFolderFocus_ puede ser NULL si no existe como una carpeta (por ejemplo, si el mensaje está incrustado en otro mensaje). 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario no controla sus propia conflictos de mensaje.
    
S_FALSE 
  
> El formulario controla sus propio conflictos de mensaje o el mensaje para el que se pasó información no está en conflicto.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormMgr::IsInConflict** para detectar si un formulario en particular no controla sus propia conflictos de mensaje. **IsInConflict** comprueba la máscara de bits en los parámetros _ulMessageFlags_ y _ulMessageStatus_ para la presencia de un indicador de conflicto. Si se establece un indicador de conflicto, **IsInConflict** resuelve la clase de mensaje que se pasa en el parámetro _szMessageClass_ y devuelve S_OK si el formulario no controla su propia entra en conflicto. **IsInConflict** devuelve S_FALSE si el formulario controla su propia entra en conflicto. 
  
Un formulario que no administran sus propio conflictos se debe abrir con el método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) y no puede volver a usar un objeto de formulario existente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Las aplicaciones cliente suelen tengan que abordar los problemas con conflictos al mover las aplicaciones de un mensaje para el mensaje siguiente o anterior en una carpeta. Si un mensaje está en conflicto, pero el servidor de formulario para ese mensaje puede controlar conflictos, la aplicación cliente debe ejecutar su código habitual para mostrar el mensaje siguiente o anterior. Si el servidor de formulario no puede controlar conflictos, la aplicación cliente debe seguir como si era consciente de la clase de mensaje del mensaje siguiente o anterior. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

