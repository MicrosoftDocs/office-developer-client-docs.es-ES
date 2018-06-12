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
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822990"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Celda RightMargin (Sección de formato del bloque de texto)

Determina la distancia entre el borde derecho del bloque de texto y el texto que contiene. El valor predeterminado es 0,25 centímetros.
  
## <a name="remarks"></a>Comentarios

Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el margen derecho permanece igual.
  
Para obtener una referencia a la celda RightMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | RightMargin  <br/> |
   
Para obtener una referencia a la celda RightMargin por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowText** <br/> |
| Índice de celda:  <br/> |**visTxtBlkRightMargin** <br/> |
   

