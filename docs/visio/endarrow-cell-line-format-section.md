---
title: Celda EndArrow (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como vértice final. final.
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822061"
---
# <a name="endarrow-cell-line-format-section"></a>Celda EndArrow (Sección de formato de línea)

Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como vértice final. final.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No hay punta de flecha.  <br/> |
|1: 45  <br/> |Estilos de punta de flecha varias tramas que se corresponden con entradas de índice en el cuadro de diálogo **línea** .  <br/> |
   
## <a name="remarks"></a>Notas

También puede establecer este valor en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, elija **flechas**y, a continuación, haga clic en **Más flechas**). El tamaño de la punta de flecha se establece en la celda EndArrowSize.
  
Puede especificar un extremo de línea personalizada con la función USE en esta celda. 
  
Para obtener una referencia a la celda EndArrow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |EndArrow  <br/> |
   
Para obtener una referencia a la celda EndArrow por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineEndArrow** <br/> |
   

