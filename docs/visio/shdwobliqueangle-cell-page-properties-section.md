---
title: Celda ShdwObliqueAngle (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Contiene un número que especifica el ángulo de dirección oblicua cuando se aplica el tipo de sombra predeterminado de la página.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430430"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>Celda ShdwObliqueAngle (Sección de propiedades de página)

Contiene un número que especifica el ángulo de dirección oblicua cuando se aplica el tipo de sombra predeterminado de la página.
  
## <a name="remarks"></a>Comentarios

Un valor de cero (0) en esta celda indica que la dirección del ángulo es vertical hacia arriba y que se mide moviéndose en el sentido de las agujas del reloj.
  
 El ángulo descrito en esta celda se usa siempre que la celda ShapeShdwType (el tipo de sombra de una forma de la página) se establece en Page Default (**visFSTPageDefault** ), y el tipo de sombra es oblicua. El tipo de sombra predeterminado de la página se define en la celda ShdwType. 
  
Para establecer este comportamiento para una forma individual, utilice la celda ShapeShdwObliqueAngle de la sección de formato de relleno.
  
Para obtener una referencia a la celda ShdwObliqueAngle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShdwObliqueAngle  <br/> |
   
Para obtener una referencia desde un programa a la celda ShdwObliqueAngle por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

