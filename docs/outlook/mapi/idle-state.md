---
title: Estado inActivo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351187"
---
# <a name="idle-state"></a>Estado inActivo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que ocurre durante el estado de inactividad de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_IDLE** <br/> |
|Estructura de datos relacionada:  <br/> | *Ninguno*  <br/> |
|Desde este estado:  <br/> | *No aplicable*  <br/> |
|A este estado:  <br/> |[Estado de sincronización](synchronize-state.md) <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

No sucede nada en este estado. Un almacén local se encuentra en este estado antes de que se inicie la replicación y después de que se complete la replicación.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

