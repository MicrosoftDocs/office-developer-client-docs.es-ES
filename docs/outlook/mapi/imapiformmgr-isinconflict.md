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
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321850"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina si un formulario puede controlar sus propios conflictos de mensajes. Un mensaje está en conflicto si ha sido editado simultáneamente por más de un usuario. Esto puede ocurrir con mensajes en carpetas públicas.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameters

 _ulMessageFlags_
  
> a Un puntero a una máscara de máscara de marcas copiada de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de un mensaje que indica el estado actual del mensaje.
    
 _ulMessageStatus_
  
> a Una máscara de bits de marcadores definidos por el cliente o definidos por el proveedor que se copian de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de un mensaje que proporciona información adicional sobre el estado del mensaje.
    
 _szMessageClass_
  
> a Una cadena que asigna un nombre A la clase de mensaje del mensaje.
    
 _pFolderFocus_
  
> a Un puntero a la carpeta que contiene el mensaje. El parámetro _pFolderFocus_ puede ser null si no existe una carpeta de este tipo (por ejemplo, si el mensaje está incrustado en otro mensaje). 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario no controla sus propios conflictos de mensajes.
    
S_FALSE 
  
> El formulario administra sus propios conflictos de mensajes o el mensaje para el que se pasó la información no está en conflicto.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: IsInConflict** para descubrir si un formulario en particular no controla sus propios conflictos de mensajes. **IsInConflict** comprueba la máscaras de de los parámetros _ulMessageFlags_ y _ulMessageStatus_ para la presencia de una marca de conflicto. Si se establece una marca de conflicto, **IsInConflict** resuelve la clase de mensaje pasada en el parámetro _SZMESSAGECLASS_ y Devuelve S_OK si el formulario no controla sus propios conflictos. **IsInConflict** devuelve S_FALSE si el formulario controla sus propios conflictos. 
  
Un formulario que no controla sus propios conflictos se debe abrir mediante el método [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) y no puede volver a usar un objeto Form existente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Las aplicaciones cliente suelen tener que enfrentarse a conflictos cuando las aplicaciones se mueven de un mensaje al mensaje siguiente o anterior de una carpeta. Si un mensaje está en conflicto, pero el servidor de formularios para ese mensaje puede controlar conflictos, la aplicación cliente debe ejecutar su código habitual para mostrar el mensaje siguiente o anterior. Si el servidor de formularios no puede controlar conflictos, la aplicación cliente debe continuar como si no hubiera constancia de la clase de mensaje del mensaje siguiente o anterior. 
  
## <a name="see-also"></a>Vea también



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

