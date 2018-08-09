---
title: Celda ShdwOffsetX (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Determina el desplazamiento horizontal en unidades de página del sombreado de una forma con respecto a la forma.
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823210"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>Celda ShdwOffsetX (sección Propiedades de la página)

Determina el desplazamiento horizontal en unidades de página del sombreado de una forma con respecto a la forma.
  
## <a name="remarks"></a>Observaciones

Este valor se establece en el cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el desplazamiento de la sombra permanece igual. 
  
Para obtener una referencia a la celda ShdwOffsetX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShdwOffsetX  <br/> |
   
Para obtener una referencia desde un programa a la celda ShdwOffsetX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageShdwOffsetX** <br/> |
   

