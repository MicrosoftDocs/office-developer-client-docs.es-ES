---
title: Celda AsianFont (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contiene el número de la fuente empleada para dar formato al texto con caracteres de lenguas asiáticas. Los números de fuente varían según las fuentes instaladas en el sistema.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821532"
---
# <a name="asianfont-cell-character-section"></a>Celda AsianFont (Sección de caracteres)

Contiene el número de la fuente empleada para dar formato al texto con caracteres de lenguas asiáticas. Los números de fuente varían según las fuentes instaladas en el sistema. 
  
## <a name="remarks"></a>Observaciones

Las fuentes asiáticas aparecen en la ficha **fuente** en el cuadro de diálogo **texto** (haga clic en la flecha situada en la **fuente** de grupo en la ficha **Inicio** ). Esta lista aparece sólo si se ha agregado un idioma que contiene caracteres asiáticos o con alfabetos complejos, en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** . (Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.
  
El número cero indica que no hay ninguna fuente especificada. Se usará la fuente Latin o fuentes predeterminadas si contienen los caracteres necesarios.
  
Para obtener una referencia a la celda AsianFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.AsianFont [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda AsianFont por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterAsianFont** <br/> |
   

