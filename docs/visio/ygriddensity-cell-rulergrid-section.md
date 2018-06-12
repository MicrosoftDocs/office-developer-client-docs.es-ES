---
title: Celda YGridDensity (regla &amp; sección de la cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica el tipo de cuadrícula vertical que se va a utilizar.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823601"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Celda YGridDensity (regla &amp; sección de la cuadrícula)

Especifica el tipo de cuadrícula vertical que se va a utilizar.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Fija  <br/> |**visGridFixed** <br/> |
|2  <br/> |Gruesa  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (predeterminada)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Fina  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Notas

Esta celda corresponde a la vertical **espaciado de la cuadrícula** de opción en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda YGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |YGridDensity  <br/> |
   
Para obtener una referencia a la celda YGridDensity por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visYGridDensity** <br/> |
   

