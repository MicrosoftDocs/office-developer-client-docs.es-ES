---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431998"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona métodos de sincronización. Esta interfaz recupera la información necesaria para replicar los cambios locales en el servidor y en el servidor en el almacén local.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificador de interfaz:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Obtiene información ampliada sobre el último error.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informa al almacén local de que la sincronización está a punto de iniciarse.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prepara el almacén local para la sincronización en un estado determinado y recupera la información necesaria para replicar.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Finaliza la sincronización en el estado actual y sale de ese estado.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Inicia la sincronización de un encabezado de mensaje.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Finaliza la sincronización de un encabezado de mensaje.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Establece el resultado de la sincronización.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando un cliente carga o sincroniza carpetas y contenido de carpetas en un almacén local, mueve el [](about-the-replication-state-machine.md)almacén local de un estado a otro, como se muestra en el diagrama de transición de estado en Acerca de la máquina de estado de replicación. A continuación se muestra el orden de los eventos para que el cliente mueva el almacén local de un estado a otro:
  
1. El cliente llama **a IOSTX::InitSync** para informar al almacén local de que la replicación está a punto de iniciarse. 
    
2. Según la dirección de replicación y los objetos que se replicarán, el cliente llama a **IOSTX::SyncBeg** para iniciar la replicación en el estado adecuado. Outlook proporciona al cliente la información necesaria y el cliente realiza la replicación. 
    
3. El cliente llama **a IOSTX::SetSyncResult** para devolver el resultado de la replicación. 
    
4. El cliente llama **a IOSTX::SyncEnd** para finalizar la replicación y proporciona a Outlook la información necesaria para la replicación posterior. 
    
En particular, al descargar elementos de mensaje, el cliente usa **IOSTX::SyncHdrBeg** y **IOSTX::SyncHdrEnd para** actualizar un elemento de mensaje completo con el encabezado del mensaje en el almacén local: 
  
1. Tras **IOSTX::SyncHdrBeg,** el almacén local pasa al estado de encabezado del mensaje de descarga. Outlook proporciona inicialmente al cliente el encabezado del mensaje actual en el almacén local.
    
2. El cliente descarga un elemento de mensaje completo junto con el encabezado del mensaje.
    
3. Outlook actualiza el elemento en el almacén local con el elemento de mensaje completo.
    
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)

