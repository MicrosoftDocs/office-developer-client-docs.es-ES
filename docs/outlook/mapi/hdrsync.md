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
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576046"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

