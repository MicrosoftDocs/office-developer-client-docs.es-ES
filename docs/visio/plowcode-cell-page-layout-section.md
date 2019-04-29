---
title: Celda PlowCode (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Determina si las formas colocables se desplazan cuando se coloca una forma colocable cerca de otra en la página de dibujo.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420356"
---
# <a name="plowcode-cell-page-layout-section"></a>Celda PlowCode (Sección de diseño de página)

Determina si las formas colocables se desplazan cuando se coloca una forma colocable cerca de otra en la página de dibujo.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |No mover formas  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Mover formas  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **diseño** , haga clic en la flecha **Configurar página** ) mediante la casilla de verificación **mover las otras formas al colocar** . 
  
Para obtener una referencia a la celda PlowCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PlowCode  <br/> |
   
Para obtener una referencia desde un programa a la celda PlowCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOPlowCode** <br/> |
   

