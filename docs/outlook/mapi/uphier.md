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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359426"
---
# <a name="uphier"></a>UPHIER
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para sincronizar una jerarquía de carpetas durante el [Estado de carga](upload-hierarchy-state.md)de la jerarquía.
  
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
  
> a Marcas para modificar el comportamiento al sincronizar la jerarquía de carpetas.
    
  - UPH_OK
    
    - a La carga se realizó correctamente. El cliente lo establece después de cargar correctamente la información en el servidor. Una vez que se ve esta marca, Outlook borra la información interna de contabilidad que indicó que era necesario actualizar la jerarquía de carpetas. 
    
    - El cliente pasa el HRESULT si la carga no se realizó correctamente.
    
_pstmReserved_
  
> contempla Este miembro está reservado para uso interno de Outlook y no es compatible.
    
_iEnt_
  
> contempla Índice para realizar un seguimiento de la sincronización del número de carpetas especificado en *cEnt* . 
    
_Ciento_
  
> contempla Número de carpetas que no están sincronizadas.
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

