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
ms.openlocfilehash: 9c9252e83ce212bacf185d0eedb75d30617f9807
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581751"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona métodos de sincronización. Esta interfaz recupera la información necesaria para replicar los cambios locales en el servidor y los cambios del servidor en el almacén local.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificador de interfaz:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Obtiene información sobre el último error ampliada.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informa el almacén local que sincronización está a punto de inicio.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prepara el almacén local para la sincronización en un estado determinado y recupera la información necesaria para replicar.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Finaliza la sincronización en el estado actual y sale de ese estado.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Inicia la sincronización para un encabezado de mensaje.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Finaliza la sincronización para un encabezado de mensaje.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Establece el resultado de la sincronización.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando un cliente de carga o sincroniza las carpetas y el contenido de la carpeta en un almacén local, mueve el almacén local de un estado a otro como se muestra en el diagrama de transición de estado en [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md). El siguiente es el orden de eventos para el cliente mover el almacén local de un estado a otro:
  
1. El cliente llama a **IOSTX::InitSync** para informarle de que la replicación esté a punto de iniciar el almacén local. 
    
2. Dependiendo de la dirección de la replicación y la replicación de objetos, el cliente llama a **IOSTX::SyncBeg** para comenzar la replicación en el estado apropiado. Outlook proporciona al cliente la información necesaria y el cliente realiza la replicación. 
    
3. El cliente llama a **IOSTX::SetSyncResult** para devolver el resultado de la replicación. 
    
4. El cliente llama a **IOSTX::SyncEnd** para finalizar la replicación, proporcionar la información necesaria para la replicación posterior de Outlook. 
    
En particular, cuando la descarga de elementos de mensaje, el cliente utiliza **IOSTX::SyncHdrBeg** y **IOSTX::SyncHdrEnd** para actualizar un elemento de mensaje completo con el encabezado del mensaje en el almacén local: 
  
1. Una vez **IOSTX::SyncHdrBeg**, local almacenar transiciones en el estado del encabezado de mensaje de descarga. Outlook proporciona inicialmente el cliente con el encabezado del mensaje actual en el almacén local.
    
2. El cliente descarga un elemento de mensaje completo junto con el encabezado del mensaje.
    
3. Outlook actualiza el elemento en el almacén local con el elemento de mensaje completo.
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)

