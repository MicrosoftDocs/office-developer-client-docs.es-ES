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
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434147"
---
# <a name="upreade"></a>UPREADE

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información ampliada para cargar el estado de lectura de un elemento durante el [estado de lectura de carga.](upload-read-status-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Miembros

_ulFlags_
  
>  [out]/[in] Marcas para determinar el comportamiento apropiado durante la carga. 
    
  - UPR_ASSOC
    
    - [salida] El elemento está oculto.
    
  - UPR_READ
    
    - [salida] Se ha cambiado el estado de lectura del elemento.
    
  - UPR_OK
    
    - [entrada] La carga se ha realizado correctamente. El cliente establece esto después de cargar información en el servidor.
    
  - UPR_COMMIT
    
    - [entrada] Cargue el estado de lectura del elemento ahora, [](upload-table-state.md) en lugar de esperar al final del estado de la tabla de carga para procesar por lotes más de un elemento. 
    
_skey_
  
> [salida] Clave de origen del elemento.
    
## <a name="see-also"></a>Consulte también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)

