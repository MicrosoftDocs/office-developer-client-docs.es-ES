---
title: Celda RightMargin (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Determina la distancia entre el borde derecho del bloque de texto y el texto que contiene. El valor predeterminado es 0,25 centímetros.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326778"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Celda RightMargin (Sección de formato del bloque de texto)

Determina la distancia entre el borde derecho del bloque de texto y el texto que contiene. El valor predeterminado es 0,25 centímetros.
  
## <a name="remarks"></a>Comentarios

Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el margen derecho permanece igual.
  
Para obtener una referencia a la celda RightMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | RightMargin  <br/> |
   
Para obtener una referencia desde un programa a la celda RightMargin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowText** <br/> |
| Índice de celda:  <br/> |**visTxtBlkRightMargin** <br/> |
   

