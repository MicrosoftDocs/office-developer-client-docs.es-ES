---
title: Celda XGridDensity (sección &amp; regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica el tipo de cuadrícula horizontal que se va a utilizar.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328994"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Celda XGridDensity (sección &amp; regla y cuadrícula)

Especifica el tipo de cuadrícula horizontal que se va a utilizar.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Decimal  <br/> |**visGridFixed** <br/> |
|segundo  <br/> |Generales  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (predeterminada)  <br/> |**visGridNormal** <br/> |
|8,5  <br/> |Minucioso  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción espaciado de la **cuadrícula** horizontal del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda XGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |XGridDensity  <br/> |
   
Para obtener una referencia desde un programa a la celda XGridDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visXGridDensity** <br/> |
   

