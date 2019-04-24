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
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329900"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>Celda PageLineJumpDirY (Sección de diseño de página)

Determina la dirección de los saltos de línea en conectores dinámicos verticales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
  
|**Value**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Valor predeterminado; arriba o la configuración de página para las formas  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Hacia la izquierda  <br/> |**visLOJumpDirYLeft** <br/> |
| segundo  <br/> | Derecha  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda PageLineJumpDirY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLineJumpDirY  <br/> |
   
Para obtener una referencia desde un programa a la celda PageLineJumpDirY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOJumpDirY** <br/> |
   

