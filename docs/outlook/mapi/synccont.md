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
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430409"
---
# <a name="synccont"></a>SYNCCONT

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para sincronizar el contenido de las carpetas especificadas en un almacén local con el servidor durante el [Estado Synchronize Contents](synchronize-contents-state.md). Esto solo implica carga o una sincronización completa que implique una carga y, a continuación, una descarga.
  
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

## <a name="members"></a>Miembros

_ulFlags_
  
> a Marcas para determinar el comportamiento adecuado durante la sincronización.
    
  - UPC_OK
    
  - a La carga o la sincronización completa se han realizado correctamente. El cliente lo establece después de sincronizar la información con el servidor.
    
_iEnt_
  
> contempla Índice para realizar un seguimiento de la sincronización del contenido en el número de carpetas especificado en _cEnt_.
    
_Ciento_
  
> contempla Número de carpetas que se van a replicar.
    
_pvReserved_
  
> Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_ptagaReserved_
  
> Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_psosReserved_
  
> Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
## <a name="see-also"></a>Ver también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

