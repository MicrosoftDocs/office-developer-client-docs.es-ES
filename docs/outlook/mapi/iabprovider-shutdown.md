---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409786"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela una conexión a una sesión activa.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> A Reserve debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La conexión se canceló correctamente.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

En la implementación del método **Shutdown** , realice las tareas que considere necesarias. MAPI llama al método **Shutdown** sólo después de haber lanzado todos los objetos de inicio de sesión. 
  
## <a name="see-also"></a>Ver también



[IABProvider : IUnknown](iabprovideriunknown.md)

