---
title: Descargar estado del encabezado de mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816705"
---
# <a name="download-message-header-state"></a>Descargar estado del encabezado de mensaje

  
  
**Hace referencia a**: Outlook 
  
 En este tema se describe qué ocurre durante el estado del encabezado de mensaje de descarga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Estructura de datos relacionados:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Desde este estado:  <br/> |[Estado de inactividad](idle-state.md) <br/> |
|En este estado:  <br/> |Estado de inactividad  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Durante este estado, el cliente actualiza el encabezado de un mensaje en un almacén local. El almacén local entra en este estado después de **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** y se cierra cuando se llama a **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** . Durante este estado, Outlook inicializa a los miembros de la estructura de datos **HDRSYNC** asociado con información sobre el encabezado de un mensaje. El cliente descarga primero el elemento de mensaje completo desde el servidor y, a continuación, actualiza el encabezado del elemento de mensaje localmente. 
  
Cuando finaliza la sincronización, el cliente establece los resultados de la descarga. El almacén local se devuelve al estado de inactividad.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

