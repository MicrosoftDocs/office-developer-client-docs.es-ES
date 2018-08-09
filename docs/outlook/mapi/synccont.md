---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 82923895353cf600c4d0b78b9a6e16fc7d57e466
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820812"
---
# <a name="synccont"></a>SYNCCONT

**Hace referencia a**: Outlook 
  
Información para sincronizar el contenido de las carpetas especificadas en un almacén local con el servidor durante la [sincronización de estado del contenido](synchronize-contents-state.md). Esto implica que acaba de cargar, o una sincronización completa que implican una carga y, a continuación, una descarga.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [entrada] Marcas para determinar el comportamiento adecuado durante la sincronización.
    
  - UPC_OK
    
  - [entrada] Cargar o sincronización completa realizada correctamente. El cliente establece esto después de la sincronización de la información con el servidor.
    
_iEnt_
  
> [out] Índice que se va a realizar un seguimiento de sincronizar el contenido en el número de las carpetas especificadas por _ciento_.
    
_cEnt_
  
> [out] Número de carpetas que se replican.
    
_pvReserved_
  
> Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_ptagaReserved_
  
> Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_psosReserved_
  
> Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

