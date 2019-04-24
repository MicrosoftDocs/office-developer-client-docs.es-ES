---
title: Celda YGridDensity (sección &amp; regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica el tipo de cuadrícula vertical que se va a utilizar.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307710"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Celda YGridDensity (sección &amp; regla y cuadrícula)

Especifica el tipo de cuadrícula vertical que se va a utilizar.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Decimal  <br/> |**visGridFixed** <br/> |
|segundo  <br/> |Generales  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (predeterminada)  <br/> |**visGridNormal** <br/> |
|8,5  <br/> |Minucioso  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción espaciado de la **cuadrícula** vertical del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda YGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |YGridDensity  <br/> |
   
Para obtener una referencia desde un programa a la celda YGridDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visYGridDensity** <br/> |
   

