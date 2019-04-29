---
title: Descargar estado del encabezado del mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417122"
---
# <a name="download-message-header-state"></a>Descargar estado del encabezado del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que ocurre durante el estado de encabezado del mensaje de descarga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Estructura de datos relacionada:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Desde este estado:  <br/> |[Estado inactivo](idle-state.md) <br/> |
|A este estado:  <br/> |Estado inactivo  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

Durante este estado, el cliente actualiza el encabezado de un mensaje en un almacén local. El almacén local especifica este estado a partir de **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** y sale cuando se llama a **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** . Durante este estado, Outlook inicializa los miembros de la estructura de datos **HDRSYNC** asociada con la información sobre el encabezado de un mensaje. En primer lugar, el cliente descarga el elemento de mensaje completo desde el servidor y, a continuación, actualiza el encabezado del elemento de mensaje de forma local. 
  
Cuando finaliza sincronización, el cliente establece los resultados de la descarga. El almacén local vuelve al estado inactivo.
  
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

