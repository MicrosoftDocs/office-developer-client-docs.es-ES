---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565049"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Comprueba si los datos adjuntos especificados está bloqueado por Microsoft Outlook 2010 o Microsoft Outlook 2013 para su visualización e indización.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parámetros

 _pwszFileName_
  
> [entrada] Puntero al nombre del archivo de datos adjuntos.
    
 _pfBlocked_
  
> [out] Puntero a un valor que indica **true** si está bloqueado el archivo adjunto especificado; en caso contrario, **false**.
    
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)
  
[Compruebe que se bloquea un dato adjunto](how-to-verify-an-attachment-is-blocked.md)

