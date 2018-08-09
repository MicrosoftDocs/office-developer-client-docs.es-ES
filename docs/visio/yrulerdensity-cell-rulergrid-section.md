---
title: Celda YRulerDensity (sección Regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica las subdivisiones verticales de la regla en la página.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823599"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Celda YRulerDensity (sección Regla y cuadrícula)

Especifica las subdivisiones verticales de la regla en la página.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Fija  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Gruesa  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (predeterminada)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fina  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción **subdivisiones** verticales en el **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda YRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |YRulerDensity  <br/> |
   
Para obtener una referencia desde un programa a la celda YRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visYRulerDensity** <br/> |
   

