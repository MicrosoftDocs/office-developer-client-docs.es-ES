---
title: Celda TagName (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contiene el nombre de la etiqueta de acción a la que está asociada esta acción.
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823373"
---
# <a name="tagname-cell-actions-section"></a>Celda TagName (sección de acciones)

Contiene el nombre de la etiqueta de acción a la que está asociada esta acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Observaciones

Mediante la celda TagName de la sección de acciones y la celda TagName de la sección de etiquetas de acción se asocian etiquetas de acción y acciones. 
  
- Si la celda TagName de una fila de acciones está en blanco, la acción aparece en un menú contextual, no en un menú de etiqueta de acción.
    
- Si un valor de la celda TagName de la fila de acciones coincide con el valor de la celda TagName de una fila de etiquetas inteligentes, la acción aparece en el menú de etiqueta de acción.
    
- Si la celda TagName de una acción tiene un valor, pero no coincide con el valor de TagName de ninguna fila de etiqueta, esa acción no aparecen en los menús de etiqueta de acción o los menús contextuales.
    
- Si varias filas de etiquetas inteligentes tienen el mismo valor de TagName, todas mostrarán las mismas acciones.
    
Para obtener una referencia a la celda TagName por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre* . Acciones de TagNamewhere.  *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia a la celda TagName por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionTagName** <br/> |
   

