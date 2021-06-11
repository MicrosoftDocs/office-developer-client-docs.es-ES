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
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438627"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierra un proveedor de almacén de mensajes de forma ordenada.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in] Reservado; debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

MAPI llama al **método IMSProvider::Shutdown** justo antes de liberar el objeto de proveedor del almacén de mensajes. MAPI libera todos los objetos de inicio de sesión de un proveedor antes de llamar a **Shutdown** para ese proveedor. 
  
## <a name="see-also"></a>Vea también



[IMSProvider : IUnknown](imsprovideriunknown.md)

