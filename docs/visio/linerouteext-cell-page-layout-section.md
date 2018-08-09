---
title: Celda LineRouteExt (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Determina la apariencia predeterminada para todos los conectores de una página de dibujo.
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822478"
---
# <a name="linerouteext-cell-page-layout-section"></a>Celda LineRouteExt (sección Diseño de página)

Determina la apariencia predeterminada para todos los conectores de una página de dibujo.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado (recta)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Recta  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Curva  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LineRouteExt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LineRouteExt  <br/> |
   
Para obtener una referencia desde un programa a la celda LineRouteExt por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOLineRouteExt** <br/> |
   

