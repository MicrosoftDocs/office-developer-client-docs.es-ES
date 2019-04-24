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
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341332"
---
# <a name="asianfont-cell-character-section"></a>Celda AsianFont (Sección de caracteres)

Contiene el número de la fuente empleada para dar formato al texto con caracteres de lenguas asiáticas. Los números de fuente varían según las fuentes instaladas en el sistema. 
  
## <a name="remarks"></a>Comentarios

Las fuentes asiáticas aparecen en la ficha **Fuente** en el cuadro de diálogo **Texto** (haga clic en la flecha del grupo **Fuente** en la ficha **Inicio**). Esta lista aparece solo si agregó un idioma que contiene caracteres de script complejos o asiáticos en el cuadro de diálogo **Preferencias de idioma de Microsoft Office**. (Haga clic en **Inicio**, **Todos los programas**, **Microsoft Office**, **Herramientas de Microsoft Office** y, a continuación, en **Preferencias de idioma de Microsoft Office**).
  
El número cero indica que no hay ninguna fuente especificada. Se usará la fuente Latin o fuentes predeterminadas si contienen los caracteres necesarios.
  
Para obtener una referencia a la celda AsianFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char. AsianFont [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia a la celda AsianFont por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterAsianFont** <br/> |
   

