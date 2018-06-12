---
title: Celda Y (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Representa la y-coordenada que indica la ubicación del controlador de una forma en coordenadas locales.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823584"
---
# <a name="y-cell-controls-section"></a>Celda Y (Sección de controles)

Representa la *y* -coordenada que indica la ubicación del controlador de una forma en coordenadas locales. 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda Y por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre* . Controles de Ywhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia a la celda Y por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlY** <br/> |
   

