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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317265"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierra un proveedor de almacenamiento de mensajes de manera ordenada.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> a Reserve debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

MAPI llama al método **IMSProvider:: Shutdown** justo antes de liberar el objeto de proveedor de almacén de mensajes. MAPI libera todos los objetos de inicio de sesión de un proveedor antes de llamar a **Shutdown** para ese proveedor. 
  
## <a name="see-also"></a>Vea también



[IMSProvider : IUnknown](imsprovideriunknown.md)

