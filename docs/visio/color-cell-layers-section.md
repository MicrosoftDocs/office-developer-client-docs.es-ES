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
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435134"
---
# <a name="color-cell-layers-section"></a>Celda Color (Sección de capas)

Especifica el color utilizado para mostrar la capa.
  
## <a name="remarks"></a>Comentarios

Para establecer el color, escriba un número entre el 0 y el 23.
  
Este valor de celda corresponde a  la configuración **Color** de  capa del  cuadro de  diálogo Propiedades de capa (en el grupo Edición de la ficha Inicio, haga clic en Capas y, a continuación, en **Propiedades de capa).**
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet. Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24. Un valor de 255 indica que la capa no tiene color. 
  
Puede establecer la transparencia del color de la capa en la celda Transparency.
  
Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Color[ *i*  ] donde  *i*  = <1>, 2, 3, ...  <br/> |
   
Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer**  +   *i* donde *i* = 0, 1, 2, ...  <br/> |
|Índice de celda:  <br/> |**visLayerColor** <br/> |
   

