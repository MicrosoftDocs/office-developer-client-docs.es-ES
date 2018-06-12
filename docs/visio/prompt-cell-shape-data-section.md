---
title: Celda Prompt (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Especifica el texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana datos de formas.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822863"
---
# <a name="prompt-cell-shape-data-section"></a>Celda Prompt (Sección de datos de formas)

Especifica el texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana **Datos de formas** . 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | De propiedades.  *Nombre* . Donde *nombre* es el nombre de la fila de símbolo del sistema  <br/> |
   
Para obtener una referencia a la celda Prompt por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp +** *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsPrompt** <br/> |
   

