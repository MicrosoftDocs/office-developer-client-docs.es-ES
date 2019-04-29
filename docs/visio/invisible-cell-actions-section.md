---
title: Celda Invisible (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indica si la acción está visible en el menú contextual o de etiqueta de acción.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423877"
---
# <a name="invisible-cell-actions-section"></a>Celda Invisible (sección de acciones)

Indica si la acción está visible en el menú contextual o de etiqueta de acción. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La acción no está visible en el menú.  <br/> |
|FALSE  <br/> |La acción está visible en el menú (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Actividades. *nombre* . Acciones Invisibledonde.  *nombre* es el nombre de la fila de acciones.  <br/> |
   
Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionInvisible** <br/> |
   

