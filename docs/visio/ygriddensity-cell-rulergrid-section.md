---
title: Celda YGridDensity (sección Cuadrícula &amp; de regla)
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429813"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Celda YGridDensity (sección Cuadrícula &amp; de regla)

Especifica el tipo de cuadrícula vertical que se va a utilizar.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Decimal  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grueso  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (predeterminada)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Bien  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción **espaciado** vertical cuadrícula del cuadro de diálogo Cuadrícula de regla (en la ficha **Ver,** haga clic en **la flecha** Mostrar). **&amp;** 
  
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
   

