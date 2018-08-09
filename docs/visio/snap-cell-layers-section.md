---
title: Celda Snap (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Determina si otras formas se pueden ajustar a formas asignadas a la capa. Las formas asignadas a la capa pueden ajustarse a otras formas, pero no a la inversa.
ms.openlocfilehash: 7fc684afb67d0454ea5907c08f4f7644d97c7f74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823268"
---
# <a name="snap-cell-layers-section"></a>Celda Snap (sección Capas)

Determina si otras formas se pueden ajustar a formas asignadas a la capa. Las formas asignadas a la capa pueden ajustarse a otras formas, pero no a la inversa.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Las demás formas pueden ajustarse a las formas de la capa.  <br/> |
|FALSE  <br/> |Las demás formas no pueden ajustarse a las formas de la capa.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede usar la opción **Ajustar** en el cuadro de diálogo **Propiedades de las capas** para establecer este valor (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Snap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Snap [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Snap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerSnap** <br/> |
   

