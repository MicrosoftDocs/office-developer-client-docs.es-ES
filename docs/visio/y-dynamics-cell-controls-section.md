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
description: Representa la coordenada y del punto de anclaje de un controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404830"
---
# <a name="y-dynamics-cell-controls-section"></a>Celda Y Dynamics (Sección de controles)

Representa la  *coordenada y*  del punto de anclaje de un controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Y Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre*  . Controles de YDynwhere.  *es*  el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda Y Dynamics por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlYDyn** <br/> |
   

