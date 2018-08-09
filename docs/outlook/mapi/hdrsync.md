---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816958"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Hace referencia a**: Outlook 
  
Información para la sincronización de un encabezado de mensaje durante el [estado del encabezado de mensaje de descarga](download-message-header-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a>Members

 _pupmsg_
  
- [out] Información para el encabezado del mensaje actual en el almacén local.
    
 _feidPar_
  
- [out] Identificador de entrada para la carpeta principal del elemento del mensaje.
    
 _pstmReserved_
  
- [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
 _ulFlags_
  
- [entrada] Indicadores para modificar el comportamiento:
    
- HSF_LOCAL
    
  - [entrada] Elemento completo reside en el mismo almacén local como el elemento de encabezado.
    
- HSF_COPYDESTRUCTIVE
    
  -  [entrada] Optimizar las operaciones de copia interno. Esto podría provocar una pérdida de datos. Se debe establecer **HSF_LOCAL** . 
    
- HSF_OK
    
  - [entrada] Sincronización de encabezado fue correcta. El cliente establece esto después de descargar información desde el servidor.
    
     _pmsgFull_
    
  - [entrada] El elemento de mensaje completo, incluido el encabezado del mensaje se descarga desde el servidor. Vea mapidefs.h para la definición de tipo de **LPMESSAGE**. 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

