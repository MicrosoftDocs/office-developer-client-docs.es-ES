---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414924"
---
# <a name="uphier"></a>UPHIER
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para sincronizar una jerarquía de carpetas durante el estado [de la jerarquía de carga.](upload-hierarchy-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Miembros

_ulFlags_
  
> [entrada] Marcas para modificar el comportamiento al sincronizar la jerarquía de carpetas.
    
  - UPH_OK
    
    - [entrada] La carga se ha realizado correctamente. El cliente establece esto después de cargar correctamente la información en el servidor. Al ver esta marca, Outlook borra la información de contabilidad interna que indicaba la jerarquía de carpetas necesaria para la actualización. 
    
    - El cliente pasa el HRESULT si la carga no se ha realizado correctamente.
    
_pstmReserved_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible.
    
_iEnt_
  
> [salida] Índice para realizar un seguimiento de la sincronización del número de carpetas especificadas por  *cEnt*  . 
    
_cEnt_
  
> [salida] Número de carpetas que no están sincronizadas.
    
## <a name="see-also"></a>Consulte también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

