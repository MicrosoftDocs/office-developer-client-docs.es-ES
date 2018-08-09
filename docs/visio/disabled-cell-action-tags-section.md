---
title: Celda Disabled (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indica si la etiqueta de acción aparece en la ventana de dibujo.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821980"
---
# <a name="disabled-cell-action-tags-section"></a>Celda Disabled (sección Etiquetas de acción)

Indica si la etiqueta de acción aparece en la ventana de dibujo.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Se deshabilita la etiqueta de acción.  <br/> |
| FALSE  <br/> | Se habilita la etiqueta de acción (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se deshabilita una etiqueta de acción, ésta no aparece en absoluto hasta que se vuelva a habilitar. 
  
Para obtener una referencia a la celda Disabled por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Etiquetas inteligentes.  *nombre* . Deshabilitado donde SmartTags. *nombre* es el nombre de la fila de etiquetas de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda Disabled por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagDisabled** <br/> |
   

