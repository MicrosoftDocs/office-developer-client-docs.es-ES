---
title: Celda Color (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Especifica el color utilizado para mostrar la capa.
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821778"
---
# <a name="color-cell-layers-section"></a>Celda Color (sección Capas)

Especifica el color utilizado para mostrar la capa.
  
## <a name="remarks"></a>Observaciones

Para establecer el color, escriba un número entre el 0 y el 23.
  
Valor de esta celda corresponde a la configuración de **color de la capa** en el cuadro de diálogo **Propiedades de las capas** (en el grupo **Edición** , en la ficha **Inicio** , haga clic en **capas** y, a continuación, haga clic en **Propiedades de las capas**).
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet. Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior. Un valor de 255 indica que la capa no tiene color. 
  
Puede establecer la transparencia del color de la capa en la celda Transparency.
  
Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Color [ *i* ] donde *i* = < 1 >, 2, 3,...  <br/> |
   
Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visLayerColor** <br/> |
   

