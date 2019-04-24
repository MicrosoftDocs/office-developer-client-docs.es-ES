---
title: Celda SortKey (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Un número que determina el orden de las acciones que aparecen en un menú contextual o de etiqueta de acción.
ms.openlocfilehash: d4eb98055f199f603003b068dca9fa7b4e377e52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334527"
---
# <a name="sortkey-cell-actions-section"></a>Celda SortKey (sección de acciones)

Un número que determina el orden de las acciones que aparecen en un menú contextual o de etiqueta de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

Las acciones aparecen en un menú contextual o de etiqueta de acción ordenadas de menor a mayor, con los números menores en la parte superior del menú. Si dos filas de acciones tienen el mismo valor para la celda SortKey, el orden queda determinado por el orden físico de la fila. El valor predeterminado es 0 (cero).
  
Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Actividades. *nombre* . Acciones Sortkeydonde.  *nombre* es el nombre de la fila de acciones.  <br/> |
   
Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionSortKey** <br/> |
   

