---
title: Estado inactivo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591803"
---
# <a name="idle-state"></a>Estado inactivo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante el estado de inactividad de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_IDLE** <br/> |
|Estructura de datos relacionados:  <br/> | *None*  <br/> |
|Desde este estado:  <br/> | *No disponible*  <br/> |
|En este estado:  <br/> |[Sincronizar estado](synchronize-state.md) <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

En este estado no ocurre nada. Un almacén local está en este estado antes de que se inicia la replicación y una vez completada la replicación.
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

