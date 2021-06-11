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
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413843"
---
# <a name="uptble"></a>UPTBLE

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información extendida para cargar el contenido de una carpeta durante el [estado de la tabla de carga.](upload-table-state.md)
  
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

## <a name="members"></a>Miembros

 _iEntMod_
  
>  [salida] Indexar para realizar un seguimiento de la  _carga del número cEntMod_ de elementos nuevos o modificados. 
    
 _cEntMod_
  
>  [salida] Número de elementos nuevos o modificados en la carpeta. 
    
 _iEntRead_
  
>  [salida] Indexar para realizar un seguimiento de la carga del número de _elementos de lectura de cEntRead._ 
    
 _cEntRead_
  
>  [salida] Número de elementos leídos en la carpeta. 
    
 _iEntDel_
  
>  [salida] Indexar para realizar un seguimiento de la carga del número de _elementos eliminados de cEntDel._ 
    
 _cEntDel_
  
>  [salida] Número de elementos eliminados en la carpeta. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md) 
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

