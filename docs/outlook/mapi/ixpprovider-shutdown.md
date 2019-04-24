---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357200"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierra un proveedor de transporte de manera ordenada.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente al apagar el proveedor de transporte.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPProvider:: Shutdown** justo antes de liberar un objeto de proveedor de transporte. Antes de llamar a **Shutdown**, MAPI libera todos los objetos de inicio de sesión de un proveedor.
  
## <a name="see-also"></a>Vea también



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

