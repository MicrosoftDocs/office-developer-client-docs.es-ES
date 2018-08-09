---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820950"
---
# <a name="upreade"></a>UPREADE

**Hace referencia a**: Outlook 
  
Información ampliada para cargar el estado de un elemento durante la [carga lee el estado de estado](upload-read-status-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
>  [out] o [in] indicadores para determinar el comportamiento adecuado durante la carga. 
    
  - UPR_ASSOC
    
    - [out] Elemento está oculto.
    
  - UPR_READ
    
    - [out] Se cambió el estado de lectura del elemento.
    
  - UPR_OK
    
    - [entrada] Carga fue correcta. El cliente establece esto después de cargar información en el servidor.
    
  - UPR_COMMIT
    
    - [entrada] Cargar el estado de lectura del elemento ahora, en lugar de esperar hasta el final de la [carga de estado de la tabla](upload-table-state.md) a proceso por lotes más de un elemento. 
    
_SKEY_
  
> [out] Clave de origen del elemento.
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)

