---
title: Celda Format (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431522"
---
# <a name="format-cell-text-fields-section"></a>Celda Format (Sección de campos de texto)

Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.
  
## <a name="remarks"></a>Comentarios

Si el valor de la celda Type es 0, 2, 5, 6 o 7 (cadena, número, fecha u hora, duración o moneda, respectivamente), especifique el formato de imagen adecuado para el tipo de datos. Por ejemplo, la imagen de formato "# #/4 UU" muestra el número 12,43 pulgadas como 12 2/4 PULGADAS. Para obtener más información sobre cómo especificar una imagen de formato, vea [Imágenes de formato](about-format-pictures.md).
  
Un número (Type = 2) puede representar una dimensión, un escalar, un ángulo, una fecha, una hora o una moneda. Para asegurar que el número de entrada sea siempre tratado como una fecha, hora o moneda, utilice la función DATETIME o CY en la celda Format en lugar de un formato de imagen.
  
Para obtener una referencia a la celda Format por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.Format[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Format por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldFormat** <br/> |
   

