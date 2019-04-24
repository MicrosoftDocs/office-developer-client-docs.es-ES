---
title: Celda Width (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Contiene el ancho de la forma seleccionada en las unidades especificadas para el dibujo. La fórmula predeterminada para especificar el ancho de una forma 1D es:'
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351222"
---
# <a name="width-cell-shape-transform-section"></a>Celda Width (Sección de transformación de forma)

Contiene el ancho de la forma seleccionada en las unidades especificadas para el dibujo. La fórmula predeterminada para especificar el ancho de una forma 1D es:
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Width por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Width  <br/> |
   
Para obtener una referencia desde un programa a la celda Width por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowXFormOut** <br/> |
| Índice de celda:  <br/> |**visXFormWidth** <br/> |
   

