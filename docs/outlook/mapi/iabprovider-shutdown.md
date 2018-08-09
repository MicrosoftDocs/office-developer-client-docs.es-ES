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
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817121"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[IABProvider : IUnknown](iabprovideriunknown.md)

