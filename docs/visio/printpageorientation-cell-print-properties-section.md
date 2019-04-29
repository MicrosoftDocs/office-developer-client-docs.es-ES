---
title: Celda PrintPageOrientation (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Determina si la página se imprime con orientación vertical u horizontal.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434868"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Celda PrintPageOrientation (Sección de propiedades de impresión)

Determina si la página se imprime con orientación vertical u horizontal.
  
|**Valor**|**Orientación**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Igual que la impresora  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|segundo  <br/> |Mundo  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se insertan nuevas páginas en un documento, esta configuración se establece de forma predeterminada en la configuración de la página activa.
  
Para obtener una referencia a la celda PrintPageOrientation por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PrintPageOrientation  <br/> |
   
Para obtener una referencia desde un programa a la celda PrintPageOrientation por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

