---
title: Celda XRulerDensity (sección Cuadrícula &amp; de regla)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica las subdivisiones horizontales de la regla en la página.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411473"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Celda XRulerDensity (sección Cuadrícula &amp; de regla)

Especifica las subdivisiones horizontales de la regla en la página.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Decimal  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |Grueso  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (predeterminada)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Bien  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la opción **Subdivisiones** horizontales del cuadro de diálogo Cuadrícula de regla (en la ficha **Ver,** haga clic en **la flecha** Mostrar). **&amp;** 
  
Para obtener una referencia a la celda XRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |XRulerDensity  <br/> |
   
Para obtener una referencia desde un programa a la celda XRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowRulerGrid** <br/> |
|Índice de celda:  <br/> |**visXRulerDensity** <br/> |
   

