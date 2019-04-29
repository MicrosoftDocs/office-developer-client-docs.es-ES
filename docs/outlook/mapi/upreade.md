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
  
Información extendida para cargar el estado de lectura de un elemento durante el [Estado de lectura](upload-read-status-state.md)de la carga.
  
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
  
>  [salida]/[in] indicadores para determinar el comportamiento adecuado durante la carga. 
    
  - UPR_ASSOC
    
    - contempla El elemento está oculto.
    
  - UPR_READ
    
    - contempla Se ha cambiado el estado de lectura del elemento.
    
  - UPR_OK
    
    - a La carga se realizó correctamente. El cliente lo establece después de cargar la información en el servidor.
    
  - UPR_COMMIT
    
    - a Cargue ahora el estado de lectura del elemento, en lugar de esperar hasta el final del [Estado de carga](upload-table-state.md) de la tabla, para procesar por lotes más de un elemento. 
    
_skey_
  
> contempla Clave de origen del elemento.
    
## <a name="see-also"></a>Ver también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)

