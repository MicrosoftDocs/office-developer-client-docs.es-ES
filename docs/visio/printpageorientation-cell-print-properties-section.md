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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822869"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Celda PrintPageOrientation (Sección de propiedades de impresión)

Determina si la página se imprime con orientación vertical u horizontal.
  
|**Valor**|**Orientation**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Igual que la impresora  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Vertical  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Horizontal  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Notas

Cuando se insertan nuevas páginas en un documento, el valor predeterminado es la configuración en la página activa.
  
Para obtener una referencia a la celda PrintPageOrientation por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PrintPageOrientation  <br/> |
   
Para obtener una referencia a la celda PrintPageOrientation por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

