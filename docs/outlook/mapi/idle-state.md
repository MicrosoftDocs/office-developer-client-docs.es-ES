---
title: Estado de inactividad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817171"
---
# <a name="idle-state"></a>Estado de inactividad

  
  
**Se aplica a**: Outlook 
  
 En este tema se describe qué ocurre durante el estado de inactividad de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_IDLE** <br/> |
|Estructura de datos relacionados:  <br/> | *None*  <br/> |
|Desde este estado:  <br/> | *No es aplicable.*  <br/> |
|En este estado:  <br/> |[Sincronizar estado](synchronize-state.md) <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

En este estado no ocurre nada. Un almacén local está en este estado antes de que se inicia la replicación y una vez completada la replicación.
  
## <a name="see-also"></a>Ver también



[Acerca de la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

