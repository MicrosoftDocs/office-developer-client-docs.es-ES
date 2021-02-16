---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436808"
---
# <a name="updel"></a>UPDEL

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información de los elementos que se han eliminado en un almacén local. Esta información se usa durante el estado [de eliminación de carga.](upload-delete-status-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Miembros

 _indeste_
  
>  [salida] Vector de [entradas UPDELE.](updele.md) 
    
 _cEnt_
  
> [salida] Número de entradas en  *el archivo*  . 
    
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

