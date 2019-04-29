---
title: Celda Color (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Determina el color utilizado para el texto de la forma.
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439992"
---
# <a name="color-cell-character-section"></a>Celda Color (Sección de caracteres)

Determina el color utilizado para el texto de la forma.
  
## <a name="remarks"></a>Comentarios

Para establecer el color, escriba un número entre el 0 y el 23.
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet. Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24. 
  
Puede establecer la transparencia del color del texto en la celda Transparency.
  
Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char. color [ *i* ] donde *i* = <1>, 2, 3,...  <br/> |
   
Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visCharacterColor** <br/> |
   

