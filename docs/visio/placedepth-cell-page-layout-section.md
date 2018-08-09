---
title: Celda PlaceDepth (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822739"
---
# <a name="placedepth-cell-page-layout-section"></a>Celda PlaceDepth (sección Diseño de página)

Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.
  
|**Valor**|**Profundidad de colocación para los diseños verticales y horizontales**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado de página  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Media  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Profunda  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Superficial  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda PlaceDepth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PlaceDepth  <br/> |
   
Para obtener una referencia desde un programa a la celda PlaceDepth por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOPlaceDepth** <br/> |
   

