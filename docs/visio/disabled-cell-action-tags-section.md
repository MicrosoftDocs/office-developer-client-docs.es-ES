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
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439670"
---
# <a name="disabled-cell-action-tags-section"></a>Celda Disabled (sección de etiquetas de acción)

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
| Nombre de celda:  <br/> | SmartTags.  *nombre*  . Deshabilitado donde SmartTags. *es*  el nombre de la fila de etiqueta de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda Disabled por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagDisabled** <br/> |
   

