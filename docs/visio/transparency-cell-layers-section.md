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
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436380"
---
# <a name="transparency-cell-layers-section"></a>Celda Transparency (Sección de capas)

Determina el grado de transparencia del color de una capa.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 -100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores se redondean al medio porcentaje más próximo. El valor 100% es totalmente transparente. Aunque una capa con un color totalmente transparente y otra sin color tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página es la misma que si su transparencia fuera del 0%. Para establecer este valor, también puede usar el control deslizante del cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers. ColorTrans [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Transparency por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerColorTrans** <br/> |
   

