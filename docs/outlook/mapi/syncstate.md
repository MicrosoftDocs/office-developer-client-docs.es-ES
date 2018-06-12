---
title: ESTADO DE SINCRONIZACIÓN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 080556a7ed4530bb96db20fd96d9dda86672a720
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820847"
---
# <a name="syncstate"></a>ESTADO DE SINCRONIZACIÓN

**Se aplica a**: Outlook 
  
Esta estructura define los Estados de la máquina de estado de replicación.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a>Ver también

- [Acerca de la API de replicación](about-the-replication-api.md)
- [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

