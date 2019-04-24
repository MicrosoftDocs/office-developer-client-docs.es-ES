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
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359993"
---
# <a name="readonly-cell-actions-section"></a>Celda ReadOnly (sección de acciones)

Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La acción aparece en el menú pero es de sólo lectura.  <br/> |
|FALSE  <br/> |La acción aparece en el menú y se puede seleccionar (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando una acción es de sólo lectura, aparece en el menú contextual o de etiqueta de acción pero no se puede seleccionar. No está atenuada, sino que aparece sobre un fondo coloreado, como una etiqueta. Para hacer que el elemento del menú aparezca atenuado, utilice la celda Disabled. 
  
Para obtener una referencia a la celda ReadOnly por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Actividades. *nombre* . Acciones Readonlydonde.  *nombre* es el nombre de la fila de acciones.  <br/> |
   
Para obtener una referencia desde un programa a la celda ReadOnly por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionReadOnly** <br/> |
   

