---
title: Celda Y Behavior (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
localization_priority: Normal
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: 'Controla el comportamiento de la coordenada y del controlador una vez que se ha movido el controlador. Hay disponibles las siguientes fórmulas:'
ms.openlocfilehash: bf8cbd490884244c92b68784dcbf041093539c94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360147"
---
# <a name="y-behavior-cell-controls-section"></a>Celda Y Behavior (Sección de controles)

Controla el comportamiento de la coordenada *y* del controlador una vez que se ha movido el controlador. Hay disponibles las siguientes fórmulas: 
  
|**Value**|**Behavior**|**Definición**|**Constante de automatización**|
|:-----|:-----|:-----|:-----|
| comprendi  <br/> | Proporcionada  <br/> | El controlador puede moverse; también se mueve de forma proporcional con la forma al estirarla.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proporcional bloqueado  <br/> | El controlador se mueve en proporción con la forma, pero no es posible moverlo por sí mismo.  <br/> |**visCtlLocked** <br/> |
| segundo  <br/> | Desplazamiento respecto al borde inferior  <br/> | El desplazamiento del controlador es constante respecto al borde inferior de la forma.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Desplazamiento respecto al centro  <br/> | El desplazamiento del controlador es constante respecto al centro de la forma.  <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> | Desplazamiento respecto al borde superior  <br/> | El desplazamiento del controlador es constante respecto al borde superior de la forma.  <br/> |**visCtlOffsetMax** <br/> |
| 2,5  <br/> | Proporcional, oculto  <br/> | El mismo efecto que 0, pero el controlador no es visible.  <br/> |**visCtlProportionalHidden** <br/> |
| 6,5  <br/> | Proporcional bloqueado, oculto  <br/> | El mismo efecto que 1, pero el controlador no es visible.  <br/> |**visCtlLockedHiddenv** <br/> |
| 0,7  <br/> | Desplazamiento respecto al borde izquierdo, oculto  <br/> | El mismo efecto que 2, pero el controlador no es visible.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8,5  <br/> | Desplazamiento respecto al centro, oculto  <br/> | El mismo efecto que 3, pero el controlador no es visible.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> | Desplazamiento respecto al borde derecho, oculto  <br/> | El mismo efecto que 4, pero el controlador no es visible.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Y Behavior por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Mando.  *nombre* . Controles YConwhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda Y Behavior por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlYCon** <br/> |
   

