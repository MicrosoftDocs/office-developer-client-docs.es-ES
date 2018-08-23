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
ms.openlocfilehash: 887c66277b54e2e14c7f67c76b8e9dd4fa8bc719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589234"
---
# <a name="upread"></a>UPREAD

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

