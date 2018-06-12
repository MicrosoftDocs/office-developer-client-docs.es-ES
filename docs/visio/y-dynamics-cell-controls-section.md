---
title: Celda Y Dynamics (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Representa la y-coordenadas de punto de anclaje del controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823618"
---
# <a name="y-dynamics-cell-controls-section"></a>Celda Y Dynamics (Sección de controles)

Representa la *y* -coordenadas de punto de anclaje del controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas. 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda Y Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre* . Controles de YDynwhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia a la celda Y Dynamics por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlYDyn** <br/> |
   

