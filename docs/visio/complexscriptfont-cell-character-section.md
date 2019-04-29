---
title: Celda ComplexScriptFont (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contiene el número de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. Los números de fuente varían según las fuentes instaladas en el sistema.
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404837"
---
# <a name="complexscriptfont-cell-character-section"></a>Celda ComplexScriptFont (Sección de caracteres)

Contiene el número de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. Los números de fuente varían según las fuentes instaladas en el sistema. 
  
## <a name="remarks"></a>Comentarios

Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** del cuadro de diálogo **texto** (haga clic en la flecha del grupo **fuente** en la ficha **Inicio** ). Esta lista aparece solo si agregó un idioma que contiene caracteres de script complejos o asiáticos en el cuadro de diálogo **Preferencias de idioma de Microsoft Office**. (Haga clic en **Inicio**, **Todos los programas**, **Microsoft Office**, **Herramientas de Microsoft Office** y, a continuación, en **Preferencias de idioma de Microsoft Office**).
  
El número cero (0) indica que no hay ninguna fuente especificada. Se usará la fuente Latin o fuentes predeterminadas.
  
Para obtener una referencia a la celda ComplexScriptFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char. ComplexScriptFont [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda ComplexScriptFont por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

