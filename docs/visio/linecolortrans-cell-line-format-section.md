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
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822456"
---
# <a name="linecolortrans-cell-line-format-section"></a>Celda LineColorTrans (Sección de formato de línea)

Determina el grado de transparencia del color de línea de una forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 - 100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Observaciones

Los valores se redondean al porcentaje medio más próximo. El valor 100% hace que sea totalmente transparente. Aunque en la página de dibujo una forma con un color de línea totalmente transparente y otra sin líneas aparecen igual, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del cero por ciento. 
  
También puede establecer este valor mediante el control deslizante en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, elija **grosor**y, a continuación, haga clic en **Más líneas**).
  
Para obtener una referencia a la celda LineColorTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineColorTrans  <br/> |
   
Para obtener una referencia a la celda LineColorTrans por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineColorTrans** <br/> |
   

