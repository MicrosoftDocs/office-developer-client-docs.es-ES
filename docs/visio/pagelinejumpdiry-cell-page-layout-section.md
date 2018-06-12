---
title: Celda PageLineJumpDirY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Determina la dirección de los saltos de línea en conectores dinámicos verticales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822726"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>Celda PageLineJumpDirY (Sección de diseño de página)

Determina la dirección de los saltos de línea en conectores dinámicos verticales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
  
|**Valor**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado; arriba o la configuración de página para las formas  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Izquierda  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Derecha  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda PageLineJumpDirY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLineJumpDirY  <br/> |
   
Para obtener una referencia a la celda PageLineJumpDirY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOJumpDirY** <br/> |
   

