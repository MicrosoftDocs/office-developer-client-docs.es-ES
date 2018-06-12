---
title: Celda XGridDensity (regla &amp; sección de la cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica el tipo de cuadrícula horizontal que se va a utilizar.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823571"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Celda XGridDensity (regla &amp; sección de la cuadrícula)

Especifica el tipo de cuadrícula horizontal que se va a utilizar.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Fija  <br/> |**visGridFixed** <br/> |
|2  <br/> |Gruesa  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (predeterminada)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Fina  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Notas

Esta celda corresponde a la horizontal **espaciado de la cuadrícula** de opción en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda XGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |XGridDensity  <br/> |
   
Para obtener una referencia a la celda XGridDensity por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visXGridDensity** <br/> |
   

