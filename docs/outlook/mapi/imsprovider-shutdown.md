---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817806"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Hace referencia a**: Outlook 
  
Cierra un proveedor de almacén de mensajes de una forma ordenada.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada] Reservado; debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

MAPI, llama al método **IMSProvider::Shutdown** justo antes de liberar el objeto de proveedor de almacén de mensajes. MAPI libera todos los objetos de inicio de sesión para un proveedor antes de llamar a **apagado** de ese proveedor. 
  
## <a name="see-also"></a>Vea también



[IMSProvider : IUnknown](imsprovideriunknown.md)

