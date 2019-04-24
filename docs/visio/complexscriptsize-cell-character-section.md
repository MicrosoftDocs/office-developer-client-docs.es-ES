---
title: Celda ComplexScriptSize (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Tamaño de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359354"
---
# <a name="complexscriptsize-cell-character-section"></a>Celda ComplexScriptSize (Sección de caracteres)

Tamaño de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. 
  
## <a name="remarks"></a>Comentarios

Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** del cuadro de diálogo **texto** (haga clic en la flecha del grupo **fuente** en la ficha **Inicio** ). Esta lista aparece solo si agregó un idioma que contiene caracteres de script complejos o asiáticos en el cuadro de diálogo **Preferencias de idioma de Microsoft Office**. (Haga clic en **Inicio**, **Todos los programas**, **Microsoft Office**, **Herramientas de Microsoft Office** y, a continuación, en **Preferencias de idioma de Microsoft Office**).
  
Puede especificar este valor como un tamaño explícito o como un porcentaje. Si especifica un porcentaje, el valor se basará en el valor de la celda Size. El valor predeterminado 0 (cero) indica el 100%. 
  
Para obtener una referencia a la celda ComplexScriptFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char. ComplexScriptSize [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda ComplexScriptSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

