---
title: Celda Flags (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Indica si el texto se lee de izquierda a derecha o al revés.
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822141"
---
# <a name="flags-cell-paragraph-section"></a>Celda Flags (sección Párrafo)

Indica si el texto se lee de izquierda a derecha o al revés.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |El texto se lee de izquierda a derecha (predeterminado).  <br/> |
|1  <br/> |El texto se lee de derecha a izquierda.  <br/> |
   
## <a name="remarks"></a>Observaciones

El valor de esta celda corresponde a la opción **dirección** en la ficha de **párrafo** en el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ), que aparece únicamente si un idioma que utiliza complejas secuencias de comandos de texto ha sido se agregó en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** . (Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.) 
  
Para obtener una referencia a la celda Flags por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Para.Flags [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Flags por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionParagraph** <br/> |
|Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFlags** <br/> |
   

