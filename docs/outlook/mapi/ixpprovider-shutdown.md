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
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592608"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="see-also"></a>Recursos adicionales



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

