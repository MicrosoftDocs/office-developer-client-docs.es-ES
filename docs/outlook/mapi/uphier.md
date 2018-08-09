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
ms.openlocfilehash: 041ae867ff3a9cc9636ff1d93f9360576e455420
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820932"
---
# <a name="uphier"></a>UPHIER
 
**Hace referencia a**: Outlook 
  
Información para la sincronización de una jerarquía de carpetas durante la [carga de estado de la jerarquía](upload-hierarchy-state.md).
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [entrada] Marcas para modificar el comportamiento cuando se sincroniza la jerarquía de carpetas.
    
  - UPH_OK
    
    - [entrada] Carga fue correcta. El cliente establece esto después de cargar correctamente la información en el servidor. Al ver esta marca, Outlook borra cualquier información de contabilidad interna que indica que la jerarquía de carpetas sea necesario actualizar. 
    
    - El cliente pasa el HRESULT si la carga no se realizó correctamente.
    
_pstmReserved_
  
> [out] Este miembro está reservado para uso interno de Outlook y no se admite.
    
_iEnt_
  
> [out] Índice que se va a realizar un seguimiento de sincronizar el número de las carpetas especificadas por *ciento* . 
    
_cEnt_
  
> [out] Número de carpetas que no están sincronizados.
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

