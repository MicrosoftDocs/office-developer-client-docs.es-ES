---
title: Celda ReadOnly (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura.
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822899"
---
# <a name="readonly-cell-actions-section"></a>Celda ReadOnly (sección de acciones)

Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La acción aparece en el menú pero es de sólo lectura.  <br/> |
|FALSE  <br/> |La acción aparece en el menú y se puede seleccionar (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

Cuando una acción es de sólo lectura, aparece en el menú contextual o de etiqueta de acción pero no se puede seleccionar. No está atenuada, pero en su lugar aparece en un fondo coloreado, como una etiqueta. Para hacer que el elemento de menú aparece atenuado, utilice la celda Disabled. 
  
Para obtener una referencia a la celda ReadOnly por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre* . Acciones de ReadOnlywhere.  *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia a la celda ReadOnly por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionReadOnly** <br/> |
   

