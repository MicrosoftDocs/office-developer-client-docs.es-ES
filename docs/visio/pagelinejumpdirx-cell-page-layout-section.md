---
title: Celda PageLineJumpDirX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Determina la dirección de los saltos de línea en conectores dinámicos horizontales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822715"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>Celda PageLineJumpDirX (Sección de diseño de página)

Determina la dirección de los saltos de línea en conectores dinámicos horizontales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
  
|**Valor**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado; izquierda o la configuración de página para las formas  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Arriba  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Abajo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda PageLineJumpDirX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLineJumpDirX  <br/> |
   
Para obtener una referencia a la celda PageLineJumpDirX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOJumpDirX** <br/> |
   

