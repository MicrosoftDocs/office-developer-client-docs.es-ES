---
title: Celda XGridSpacing (sección &amp; regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327324"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>Celda XGridSpacing (sección &amp; regla y cuadrícula)

Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).
  
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción **espaciaDo mínimo** horizontal del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
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
   

