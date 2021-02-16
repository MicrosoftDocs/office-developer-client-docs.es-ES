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
description: Especifica un texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana Datos de formas.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405488"
---
# <a name="prompt-cell-shape-data-section"></a>Celda Prompt (Sección de datos de formas)

Especifica un texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana **Datos de formas**. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Prop.  *Nombre*  . Símbolo del sistema  *donde Nombre*  es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Prompt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp +** *i*  donde  *i*  = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsPrompt** <br/> |
   

