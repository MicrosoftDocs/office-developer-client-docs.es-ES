---
title: Celda Transparency (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Determina el grado de transparencia del color de una capa.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823436"
---
# <a name="transparency-cell-layers-section"></a>Celda Transparency (Sección de capas)

Determina el grado de transparencia del color de una capa.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 - 100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Observaciones

Los valores se redondean al porcentaje medio más próximo. Un valor de 100% es completamente transparente. Aunque una capa que tiene un color completamente transparente el mismo en la página de dibujo aparece como una capa que no tiene ningún color, interactúa con otros objetos en la página de la misma manera como si su transparencia fuera 0%. También puede establecer este valor mediante el control deslizante en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio** , en el grupo **Edición** , haga clic en **capas**y, a continuación, haga clic en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.ColorTrans [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Transparency por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerColorTrans** <br/> |
   

