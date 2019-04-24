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
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350851"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba si Microsoft Outlook 2010 o Microsoft Outlook 2013 han bloqueado los datos adjuntos especificados para la visualización y la indización.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parameters

 _pwszFileName_
  
> a Puntero al nombre del archivo de datos adjuntos.
    
 _pfBlocked_
  
> contempla Puntero a un valor que indica **true** si se bloquean los datos adjuntos especificados; de lo contrario, **false**.
    
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)
  
[Comprobar que los datos adJuntos están bloqueados](how-to-verify-an-attachment-is-blocked.md)

