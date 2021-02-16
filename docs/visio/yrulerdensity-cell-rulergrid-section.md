---
title: Celda YRulerDensity (Sección &amp; de cuadrícula de regla)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica las subdivisiones verticales de la regla en la página.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406804"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Celda YRulerDensity (Sección &amp; de cuadrícula de regla)

Especifica las subdivisiones verticales de la regla en la página.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Decimal  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |Grueso  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (predeterminada)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Bien  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción **Subdivisiones** verticales del  cuadro de diálogo Cuadrícula de regla (en la ficha Ver, haga clic en **la flecha** Mostrar). **&amp;** 
  
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
   

