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
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326155"
---
# <a name="upread"></a>UPREAD

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar el estado de lectura de los elementos durante el [Estado de lectura](upload-read-status-state.md)de la carga.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Miembros

 _pupre_
  
>  contempla Vector de las entradas que se han **[leído](upreade.md)** . 
    
 _Ciento_
  
>  contempla Número de entradas que se han **leído** . 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

