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
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410626"
---
# <a name="linerouteext-cell-page-layout-section"></a>Celda LineRouteExt (Sección de diseño de página)

Determina la apariencia predeterminada para todos los conectores de una página de dibujo.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado (recta)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Recto  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Curvado  <br/> |**visLORouteExtNURBS** <br/> |
   
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
   

