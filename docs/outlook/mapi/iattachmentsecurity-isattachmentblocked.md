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
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817165"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Hace referencia a**: Outlook 
  
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
  
[Comprobar si los datos adjuntos están bloqueados](how-to-verify-an-attachment-is-blocked.md)

