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
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434847"
---
# <a name="snap-cell-layers-section"></a>Celda Snap (Sección de capas)

Determina si otras formas se pueden ajustar a formas asignadas a la capa. Las formas asignadas a la capa pueden ajustarse a otras formas, pero no a la inversa.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Las demás formas pueden ajustarse a las formas de la capa.  <br/> |
|FALSE  <br/> |Las demás formas no pueden ajustarse a las formas de la capa.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede usar la opción **Ajustar** en el cuadro de diálogo **Propiedades de las capas** para establecer este valor (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Snap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers. Snap [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Snap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerSnap** <br/> |
   

