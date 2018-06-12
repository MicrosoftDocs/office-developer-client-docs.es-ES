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
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821811"
---
# <a name="complexscriptfont-cell-character-section"></a>Celda ComplexScriptFont (Sección de caracteres)

Contiene el número de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. Los números de fuente varían según las fuentes instaladas en el sistema. 
  
## <a name="remarks"></a>Observaciones

Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** en el cuadro de diálogo **texto** (haga clic en la flecha situada en la **fuente** de grupo en la ficha **Inicio** ). Esta lista aparece sólo si se ha agregado un idioma que contiene caracteres asiáticos o con alfabetos complejos, en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** . (Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.
  
El número 0 (cero) indica que no hay ninguna fuente especificada. Se usan el nombre de fuente latino o fuentes predeterminadas.
  
Para obtener una referencia a la celda ComplexScriptSize por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.ComplexScriptFont [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda ComplexScriptFont por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

