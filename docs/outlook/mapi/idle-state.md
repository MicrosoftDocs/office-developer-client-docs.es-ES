---
title: Estado de inactividad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419481"
---
# <a name="idle-state"></a>Estado de inactividad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de inactividad de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_IDLE** <br/> |
|Estructura de datos relacionada:  <br/> | *Ninguna*  <br/> |
|Desde este estado:  <br/> | *No aplicable*  <br/> |
|A este estado:  <br/> |[Estado de sincronización](synchronize-state.md) <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que sale de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Descripción

No ocurre nada en este estado. Un almacén local está en este estado antes de iniciar la replicación y después de que se complete la replicación.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

