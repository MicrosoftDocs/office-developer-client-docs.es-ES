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
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822781"
---
# <a name="plowcode-cell-page-layout-section"></a>Celda PlowCode (Sección de diseño de página)

Determina si las formas colocables se desplazan cuando se coloca una forma colocable cerca de otra en la página de dibujo.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |No mover formas  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Mover formas  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Notas

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ) mediante el uso de la casilla de verificación **mover las otras formas al colocar** . 
  
Para obtener una referencia a la celda PlowCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PlowCode  <br/> |
   
Para obtener una referencia a la celda PlowCode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOPlowCode** <br/> |
   

