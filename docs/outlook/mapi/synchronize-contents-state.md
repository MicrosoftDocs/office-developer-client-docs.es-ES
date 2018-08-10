---
title: Estado de sincronización de contenidos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820819"
---
# <a name="synchronize-contents-state"></a>Estado de sincronización de contenidos

  
  
**Hace referencia a**: Outlook 
  
 En este tema se describe qué ocurre durante el estado del contenido de sincronizar de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Estructura de datos relacionados:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar estado](synchronize-state.md) <br/> |
|En este estado:  <br/> |[Estado de la tabla de descarga](download-table-state.md), [cargar el estado de la tabla](upload-table-state.md), o sincronizar estado  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia uno de los dos procesos de replicación: carga el contenido de especificado las carpetas en un almacén local o una sincronización completa. En una sincronización completa, para cada una de las carpetas especificadas, contenido se cargan en primer lugar y, a continuación, se descargan. Según la *ulFlags* establecer en la estructura de **[sincronización](sync.md)** correspondiente en el anterior sincronizar estado, Outlook inicializa [out] (miembros de) en la estructura **SYNCCONT** para proporcionar información sobre el contenido. 
  
A través de la misma estructura **SYNCCONT** , el cliente obtiene el recuento de las carpetas que tienen contenido que se carga o descarga. El cliente recorre en bucle cada una de estas carpetas mover el almacén local en el estado de la tabla de cargar para cargar una carpeta, o mover el almacén local para el estado de la tabla de descarga para descargar la carpeta. 
  
Además, el cliente obtiene los identificadores de entrada para las carpetas que requieren replicación.
  
Cuando finaliza este estado, Outlook limpia su información interna. Devuelve el almacén local en el estado de sincronización.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

