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
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567891"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela una conexión a una sesión activa.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [Entrada] Reservado; debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La conexión se canceló correctamente.
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

En la implementación del método **apagado** , lleve a cabo cualquier tarea de tener en cuenta es necesario. MAPI llama a su método **Shutdown** sólo después de que se han lanzado todos los objetos de inicio de sesión. 
  
## <a name="see-also"></a>Recursos adicionales



[IABProvider : IUnknown](iabprovideriunknown.md)

