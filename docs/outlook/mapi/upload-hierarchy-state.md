---
title: Cargar estado de la jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572189"
---
# <a name="upload-hierarchy-state"></a>Cargar estado de la jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante el estado de la jerarquía de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Estructura de datos relacionados:  <br/> |**[UPHIER](uphier.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar estado](synchronize-state.md) <br/> |
|En este estado:  <br/> |[Cargar el estado de la carpeta](upload-folder-state.md), o sincronizar estado  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga de una jerarquía de árbol de la carpeta que se ha especificado en una anterior sincronizar estado. Outlook determina el número de carpetas que se han creado o modificado en esa jerarquía e inicializa *cEnt* en **UPHIER**. Outlook también mantiene un recuento del número de carpetas que se cargan con otro miembro *iEnt* . Para cargar cada una de las carpetas *cEnt* , el cliente mueve el almacén local en el estado de la carpeta de carga, cuando finaliza la carga de la carpeta de nuevo en el estado de la jerarquía de carga. 
  
Cuando finaliza el estado de la jerarquía de carga, el almacén local se devuelve en el estado de sincronización.
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

