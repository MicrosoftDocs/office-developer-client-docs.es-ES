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
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822195"
---
# <a name="format-cell-text-fields-section"></a>Celda Format (sección de campos de texto)

Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.
  
## <a name="remarks"></a>Comentarios

Si el valor de la celda Type es 0, 2, 5, 6 o 7 (cadena, número, fecha u hora, duración o moneda, respectivamente), especifique una imagen de formato adecuado para el tipo de datos. Por ejemplo, el formato de imagen "# #/ 4 UU" da formato el número en 12,43. como 12 2/4 pulgadas. Para obtener más información acerca de cómo especificar una imagen de formato, vea [acerca de las imágenes de formato](about-format-pictures.md).
  
Un número (Type = 2) puede representar una dimensión, un escalar, un ángulo, una fecha, una hora o una moneda. Para asegurar que el número de entrada sea siempre tratado como una fecha, hora o moneda, utilice la función DATETIME o CY en la celda Format en lugar de un formato de imagen.
  
Para obtener una referencia a la celda Format por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.Format [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Format por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldFormat** <br/> |
   

