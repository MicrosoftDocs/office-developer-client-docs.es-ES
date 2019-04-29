---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418711"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta estructura se usa con [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a>Members

 **ulSize**
  
> El tamaño de la estructura.
    
 **ulFlags**
  
> Marca que indica el tipo de sincronización. Debe ser uno de los siguientes valores:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Enviar el mensaje al servidor (no actualmente en uso).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Inserta los cambios en la jerarquía del servidor.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Extraer los cambios en la jerarquía del servidor.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Insertar los cambios de mensajes en el servidor.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Extraer los cambios de mensajes del servidor.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |La sincronización ha sido iniciada por el usuario y debe tener una prioridad más alta.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Solo debe sincronizar los encabezados y no los cuerpos completos.  <br/> |
   
 **psesSync**
  
> A Un puntero a la sesión MAPI.
    
 **punkCallBack**
  
> A Puntero a la interfaz en la que se va a proporcionar el progreso. Se puede usar para consultar la interfaz de [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> CONTEMPLA Evento que se producirá cuando se complete el subproceso que se acaba de crear. El puntero debe ser válido porque contendrá el evento.
    
## <a name="see-also"></a>Ver también



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

