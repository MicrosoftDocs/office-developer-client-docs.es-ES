---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818278"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Se aplica a**: Outlook 
  
Esta estructura se utiliza con [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
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

## <a name="members"></a>Miembros

 **ulSize**
  
> El tamaño de la estructura.
    
 **ulFlags**
  
> Marca que indica el tipo de sincronización. Debe ser uno de los siguientes valores:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0 x 00000200  <br/> |Enviar el mensaje al servidor (que no están en uso).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Publicar los cambios de jerarquía en el servidor.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Extraer los cambios en la jerarquía del servidor.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Cambios en el mensaje de inserción al servidor.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Extraer los cambios de los mensajes del servidor.  <br/> |
|SYNC_ON_DEMAND  <br/> |0 x 20000000  <br/> |La sincronización iniciada por el usuario y debe ser una prioridad superior.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Sólo se debe sincronizar los encabezados y cuerpos no completas.  <br/> |
   
 **psesSync**
  
> [IN] Un puntero a la sesión MAPI.
    
 **punkCallBack**
  
> [IN] Un puntero a la interfaz en la que se va a proporcionar el progreso. Se puede utilizar para consultar la interfaz para [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] El evento que se producirá cuando se haya completado el subproceso que se acaba de crear. El puntero debe ser válido debido a que contendrá el evento.
    
## <a name="see-also"></a>Ver también



[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync: IUnknown](imapisynciunknown.md)

