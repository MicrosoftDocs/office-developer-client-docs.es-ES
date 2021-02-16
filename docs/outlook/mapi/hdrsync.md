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
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410255"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para sincronizar un encabezado de mensaje durante el estado [del encabezado del mensaje de descarga.](download-message-header-state.md)
  
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

## <a name="members"></a>Miembros

 _oemmsg_
  
- [salida] Información del encabezado del mensaje actual en el almacén local.
    
 _feidPar_
  
- [salida] Identificador de entrada de la carpeta principal del elemento de mensaje.
    
 _pstmReserved_
  
- [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
 _ulFlags_
  
- [entrada] Marcas para modificar el comportamiento:
    
- HSF_LOCAL
    
  - [entrada] El elemento completo reside en el mismo almacén local que el elemento de encabezado.
    
- HSF_COPYDESTRUCTIVE
    
  -  [entrada] Optimizar las operaciones de copia internas. Esto puede provocar la pérdida de datos. **HSF_LOCAL** se debe establecer. 
    
- HSF_OK
    
  - [entrada] La sincronización de encabezados se ha realizado correctamente. El cliente lo establece después de descargar la información del servidor.
    
     _pmsgFull_
    
  - [entrada] El elemento de mensaje completo, incluido el encabezado del mensaje descargado del servidor. Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**. 
    
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[FEID](feid.md)

