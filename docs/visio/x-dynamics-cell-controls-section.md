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
description: Representa la coordenada x del punto de anclaje de un controlador en coordenadas locales.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432131"
---
# <a name="x-dynamics-cell-controls-section"></a>Celda X Dynamics (Sección de controles)

Representa la coordenada  *x*  del punto de anclaje de un controlador en coordenadas locales. 
  
## <a name="remarks"></a>Comentarios

El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
  
Para obtener una referencia a la celda X Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre*  . Controles XDynwhere.  *es*  el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda X Dynamics por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlXDyn** <br/> |
   

