---
title: Celda Scale (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Controla el ancho de la fuente. El valor predeterminado de esta celda es 100%.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823102"
---
# <a name="scale-cell-character-section"></a>Celda Scale (sección Caracteres)

Controla el ancho de la fuente. El valor predeterminado de esta celda es 100%.
  
## <a name="remarks"></a>Observaciones

Establezca un porcentaje entre 1% y 99% para disminuir el ancho de la fuente. Establezca un porcentaje entre 101% y 600% para aumentar el ancho de la fuente.
  
También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**). 
  
Para obtener una referencia a la celda Scale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.FontScale [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Scale por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterFontScale** <br/> |
   

