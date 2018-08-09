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
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818018"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Hace referencia a**: Outlook 
  
Se cierra un proveedor de transporte de una forma ordenada.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente en Apagar el proveedor de transporte.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPProvider::Shutdown** justo antes de la liberación de un objeto de proveedor de transporte. Antes de llamar a **apagado**, MAPI libera todos los objetos de inicio de sesión para un proveedor.
  
## <a name="see-also"></a>Vea también



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

