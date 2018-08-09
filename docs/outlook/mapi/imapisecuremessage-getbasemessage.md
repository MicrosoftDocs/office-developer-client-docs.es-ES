---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817420"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Hace referencia a**: Outlook 
  
Recupera el subyacentes [IMessage: IMAPIProp](imessageimapiprop.md) esta [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) se encapsula. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parámetros

 _ppmsg_
  
> [out] Un objeto de mensaje seguro.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="see-also"></a>Vea también



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

