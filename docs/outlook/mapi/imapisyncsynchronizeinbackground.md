---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Última modificación: 26 de junio de 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426859"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 Inicia una sincronización. Este método es llamado por Microsoft Outlook 2010 y Microsoft Outlook 2013 e implementado por los proveedores de almacén de mensajes. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Parameters

 _psibpb_
  
> Informa al proveedor de lo que se sincronizará y proporciona acceso a las interfaces que se pueden usar durante la sincronización. Es una [estructura MAPISIB.](mapisib.md) 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="see-also"></a>Vea también



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

