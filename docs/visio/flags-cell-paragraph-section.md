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
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413118"
---
# <a name="flags-cell-paragraph-section"></a>Celda Flags (Sección de párrafo)

Indica si el texto se lee de izquierda a derecha o al revés.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |El texto se lee de izquierda a derecha (predeterminado).  <br/> |
|1  <br/> |El texto se lee de derecha a izquierda.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta celda corresponde a la configuración de **Dirección** de la ficha **párrafo** del cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ), que solo aparece si se ha configurado un idioma que utiliza texto de scripts complejos agregado en el cuadro de diálogo **preferencias de idioma de Microsoft Office** . (Haga clic en **Inicio**, en **todos los programas**, en **Microsoft Office**, haga clic en **herramientas de Microsoft Office**y, a continuación, haga clic en **preferencias de idioma de Microsoft Office**). 
  
Para obtener una referencia a la celda Flags por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Para. Flags [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Flags por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionParagraph** <br/> |
|Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFlags** <br/> |
   

