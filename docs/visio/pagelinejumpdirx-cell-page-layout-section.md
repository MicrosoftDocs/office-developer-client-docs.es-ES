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
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283740"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>Celda PageLineJumpDirX (Sección de diseño de página)

Determina la dirección de los saltos de línea en conectores dinámicos horizontales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
  
|**Value**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Valor predeterminado; izquierda o la configuración de página para las formas  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Arriba  <br/> |**visLOJumpDirXUp** <br/> |
| segundo  <br/> | Abajo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda PageLineJumpDirX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLineJumpDirX  <br/> |
   
Para obtener una referencia desde un programa a la celda PageLineJumpDirX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOJumpDirX** <br/> |
   

