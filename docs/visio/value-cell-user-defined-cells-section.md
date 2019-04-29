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
description: Especifica un valor para la celda correspondiente definida por el usuario.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422994"
---
# <a name="value-cell-user-defined-cells-section"></a>Celda Value (Sección de celdas definidas por el usuario)

Especifica un valor para la celda correspondiente definida por el usuario.
  
## <a name="remarks"></a>Comentarios

Para hacer referencia a este valor desde otra celda, especifique el nombre definido por el usuario indicado en la etiqueta de fila User.Row.
  
Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Usuario.  *Nombre* . Valor en el que el usuario.  *Name* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionUser** <br/> |
| Índice de fila:  <br/> |**visRowUser** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visUserValue** <br/> |
   

