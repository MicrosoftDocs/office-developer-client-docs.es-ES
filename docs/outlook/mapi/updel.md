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
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820925"
---
# <a name="updel"></a>UPDEL

  
  
**Hace referencia a**: Outlook 
  
Información para los elementos que se han eliminado en un almacén local. Esta información se usa durante la [carga Eliminar estado](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupde_
  
>  [out] Vector de [UPDELE](updele.md) entradas. 
    
 _cEnt_
  
> [out] Número de entradas en *pupde* . 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

