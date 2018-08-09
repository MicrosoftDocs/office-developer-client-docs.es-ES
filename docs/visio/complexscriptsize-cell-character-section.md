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
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821816"
---
# <a name="complexscriptsize-cell-character-section"></a>Celda ComplexScriptSize (sección Caracteres)

Tamaño de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. 
  
## <a name="remarks"></a>Observaciones

Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** en el cuadro de diálogo **texto** (haga clic en la flecha situada en la **fuente** de grupo en la ficha **Inicio** ). Esta lista aparece sólo si se ha agregado un idioma que contiene caracteres asiáticos o con alfabetos complejos, en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** . (Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.
  
Puede especificar este valor como un tamaño explícito o como un porcentaje. Si especifica un porcentaje, el valor se basará en el valor de la celda Size. El valor predeterminado 0 (cero) indica el 100%. 
  
Para obtener una referencia a la celda ComplexScriptFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.ComplexScriptSize [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda ComplexScriptSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

