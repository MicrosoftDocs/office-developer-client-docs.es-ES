---
title: Celda Value (Sección de celdas definidas por el usuario)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Especifica un valor para la correspondiente celda definida por el usuario.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823508"
---
# <a name="value-cell-user-defined-cells-section"></a>Celda Value (Sección de celdas definidas por el usuario)

Especifica un valor para la celda correspondiente definida por el usuario.
  
## <a name="remarks"></a>Comentarios

Para hacer referencia a este valor desde otra celda, especifique el nombre definido por el usuario indicado en la etiqueta de fila User.Row.
  
Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Usuario.  *Nombre* . El valor de where usuario.  *Nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia a la celda Value por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionUser** <br/> |
| Índice de fila:  <br/> |**visRowUser** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visUserValue** <br/> |
   

