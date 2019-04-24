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
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346798"
---
# <a name="placedepth-cell-page-layout-section"></a>Celda PlaceDepth (sección de diseño de página)

Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.
  
|**Value**|**Profundidad de colocación para los diseños verticales y horizontales**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Valor predeterminado de página  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Medio  <br/> |**visPLOPlaceDepthMedium** <br/> |
| segundo  <br/> | Gran  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Profunda  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
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
   

