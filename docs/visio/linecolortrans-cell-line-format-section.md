---
title: Celda LineColorTrans (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Determina el grado de transparencia del color de línea de una forma.
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359300"
---
# <a name="linecolortrans-cell-line-format-section"></a>Celda LineColorTrans (sección de formato de línea)

Determina el grado de transparencia del color de línea de una forma.
  
|**Value**|**Descripción**|
|:-----|:-----|
|0 -100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores se redondean al porcentaje medio más próximo. El valor 100% hace que sea totalmente transparente. Aunque en la página de dibujo una forma con un color de línea totalmente transparente y otra sin líneas aparecen igual, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del cero por ciento. 
  
También puede establecer este valor con el control deslizante en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, seleccione **Grosor** y, a continuación, haga clic en **Más líneas**).
  
Para obtener una referencia a la celda LineColorTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineColorTrans  <br/> |
   
Para obtener una referencia desde un programa a la celda LineColorTrans por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineColorTrans** <br/> |
   

