---
title: Celda X Dynamics (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Representa la x-coordenadas de punto de anclaje del controlador en coordenadas locales.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823588"
---
# <a name="x-dynamics-cell-controls-section"></a>Celda X Dynamics (Sección de controles)

Representa la *x* -coordenadas de punto de anclaje del controlador en coordenadas locales. 
  
## <a name="remarks"></a>Comentarios

El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
  
Para obtener una referencia a la celda X Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre* . Controles de XDynwhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia a la celda X Dynamics por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlXDyn** <br/> |
   

