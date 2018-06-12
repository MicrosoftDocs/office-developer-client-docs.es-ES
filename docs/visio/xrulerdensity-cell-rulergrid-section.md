---
title: Celda XRulerDensity (regla &amp; sección de la cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica las subdivisiones horizontales de la regla en la página.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823567"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Celda XRulerDensity (regla &amp; sección de la cuadrícula)

Especifica las subdivisiones horizontales de la regla en la página.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Fija  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Gruesa  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (predeterminada)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fina  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Notas

Esta celda corresponde a la opción **subdivisiones** horizontales en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ). 
  
Para obtener una referencia a la celda XRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |XRulerDensity  <br/> |
   
Para obtener una referencia a la celda XRulerDensity por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visXRulerDensity** <br/> |
   

