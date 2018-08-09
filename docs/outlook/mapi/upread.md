---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa3c0b90a64c90a7c854cb22ac75438fa5fca23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820942"
---
# <a name="upread"></a>UPREAD

  
  
**Hace referencia a**: Outlook 
  
Información para cargar el estado de lectura de elementos durante la [carga lee el estado de estado](upload-read-status-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupre_
  
>  [out] Vector de **[UPREADE](upreade.md)** entradas. 
    
 _cEnt_
  
>  [out] Número de entradas **UPREADE** . 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

