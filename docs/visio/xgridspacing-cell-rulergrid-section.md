---
title: Celda XGridSpacing (sección Regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823565"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>Celda XGridSpacing (sección Regla y cuadrícula)

Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).
  
## <a name="remarks"></a>Observaciones

Esta celda corresponde a la horizontal **Espaciado mínimo** de opción en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda XGridSpacing por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |XGridSpacing  <br/> |
   
Para obtener una referencia desde un programa a la celda XGridSpacing por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visXGridSpacing** <br/> |
   

