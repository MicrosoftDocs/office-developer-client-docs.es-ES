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
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823228"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>Celda ShdwObliqueAngle (Sección de propiedades de página)

Contiene un número que especifica el ángulo de dirección oblicua cuando se aplica el tipo de sombra predeterminado de la página.
  
## <a name="remarks"></a>Comentarios

Un valor de cero (0) en esta celda indica que la dirección del ángulo es vertical hacia arriba y que se mide moviéndose en el sentido de las agujas del reloj.
  
 El ángulo que se describe en esta celda se utiliza cuando la celda ShapeShdwType (tipo de sombra para una forma en la página) se establece en el valor predeterminado de página (**visFSTPageDefault** ), y el tipo de sombra es oblicuo. El tipo de sombra de página predeterminado se define en la celda ShdwType. 
  
Para establecer este comportamiento para una forma individual, utilice la celda ShapeShdwObliqueAngle de la sección de formato de relleno.
  
Para obtener una referencia a la celda ShdwObliqueAngle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShdwObliqueAngle  <br/> |
   
Para obtener una referencia a la celda ShdwObliqueAngle por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

