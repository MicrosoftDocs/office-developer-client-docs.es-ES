---
title: Celda X Behavior (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251285
localization_priority: Normal
ms.assetid: 82423d08-b6ce-0f23-8b61-354c3e5f323e
description: Controla el tipo de comportamiento de la x-coordenada del controlador cuando éste se mueve.
ms.openlocfilehash: 004ad407941aa15cec3ae94188f590ec6513c4da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823556"
---
# <a name="x-behavior-cell-controls-section"></a>Celda X Behavior (Sección de controles)

Controla el tipo de comportamiento de la *x* -coordenada del controlador cuando éste se mueve. 
  
|**Valor**|**Comportamiento**|**Definición**|**Constante de automatización**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proporcional  <br/> | El controlador puede moverse; también se mueve de forma proporcional con la forma al estirarla.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proporcional bloqueado  <br/> | El controlador se mueve en proporción con la forma, pero no es posible moverlo por sí mismo.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Desplazamiento respecto al borde izquierdo  <br/> | El desplazamiento del controlador es constante respecto al lado izquierdo de la forma.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Desplazamiento respecto al centro  <br/> | El desplazamiento del controlador es constante respecto al centro de la forma.  <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> | Desplazamiento respecto al borde derecho  <br/> | El desplazamiento del controlador es constante respecto al lado derecho de la forma.  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | Proporcional, oculto  <br/> | El mismo efecto que 0, pero el controlador no es visible.  <br/> |**visCtlProportionalHidden** <br/> |
| 6  <br/> | Proporcional bloqueado, oculto  <br/> | El mismo efecto que 1, pero el controlador no es visible.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> | Desplazamiento respecto al borde izquierdo, oculto  <br/> | El mismo efecto que 2, pero el controlador no es visible.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8  <br/> | Desplazamiento respecto al centro, oculto  <br/> | El mismo efecto que 3, pero el controlador no es visible.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> | Desplazamiento respecto al borde derecho, oculto  <br/> | El mismo efecto que 4, pero el controlador no es visible.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda X Behavior por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre* . Controles de XConwhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia a la celda X Behavior por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlXCon** <br/> |
   

