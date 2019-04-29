---
title: Celda BeginArrow (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como primer vértice. Escriba un número entre 0 y 45 o la función USE con el nombre de un extremo de línea personalizado, o bien, utilice el cuadro de diálogo Línea.
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410297"
---
# <a name="beginarrow-cell-line-format-section"></a>Celda BeginArrow (Sección de formato de línea)

Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como primer vértice. Escriba un número entre 0 y 45 o la función USE con el nombre de un extremo de línea personalizado, o bien, utilice el cuadro de diálogo **Línea**. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| comprendi  <br/> | No hay punta de flecha.  <br/> |
| 1 -45  <br/> | Varios estilos de punta de flecha que se corresponden con las entradas indizadas del cuadro de diálogo **Línea**.  <br/> |
   
## <a name="remarks"></a>Comentarios

El tamaño de la punta de flecha se establece en la celda BeginArrowSize.
  
Para obtener una referencia a la celda BeginArrow por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | BeginArrow  <br/> |
   
Para obtener una referencia a la celda BeginArrow por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visLineBeginArrow** <br/> |
   

