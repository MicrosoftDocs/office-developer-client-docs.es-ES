---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820954"
---
# <a name="uptble"></a>UPTBLE

**Hace referencia a**: Outlook 
  
Información extendida para cargar el contenido de una carpeta durante la [carga de estado de la tabla](upload-table-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Members

 _iEntMod_
  
>  [out] Índice que se va a realizar un seguimiento de cargar el número de _cEntMod_ de elementos nuevos o modificados. 
    
 _cEntMod_
  
>  [out] Número de elementos nuevos o modificados en la carpeta. 
    
 _iEntRead_
  
>  [out] Para realizar un seguimiento de cargar el número de _cEntRead_ leer elementos de índice. 
    
 _cEntRead_
  
>  [out] Número de elementos de lectura en la carpeta. 
    
 _iEntDel_
  
>  [out] Índice que se va a realizar un seguimiento de cargar el número de _cEntDel_ elementos eliminados. 
    
 _cEntDel_
  
>  [out] Número de elementos eliminados en la carpeta. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md) 
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

