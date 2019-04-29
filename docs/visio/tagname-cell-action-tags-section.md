---
title: Celda TagName (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nombre de la etiqueta de acción empleado como clave para asociarla con sus acciones.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417913"
---
# <a name="tagname-cell-action-tags-section"></a>Celda TagName (sección de etiquetas de acción)

Nombre de la etiqueta de acción empleado como clave para asociarla con sus acciones.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

 La celda TagName de la sección de etiquetas de acción funciona en conjunción con la celda TagName de la sección de acciones para asociar la etiqueta de acción con sus acciones. Las filas de la sección de acciones también tienen una celda TagName y las filas con el mismo valor de celda TagName que esta celda definen las acciones que se deben llevar a cabo para esta etiqueta de acción. 
  
Para obtener una referencia a la celda TagName por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre* . TagName donde SmartTags. *nombre* es el nombre de la fila de la etiqueta de acción.  <br/> |
   
Para obtener una referencia a la celda TagName por su índice
 desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagName** <br/> |
   

