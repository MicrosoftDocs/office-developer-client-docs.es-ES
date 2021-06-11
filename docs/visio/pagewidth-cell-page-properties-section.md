---
title: Celda PageWidth (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Determina el ancho de la página impresa en las unidades de dibujo.
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434273"
---
# <a name="pagewidth-cell-page-properties-section"></a>Celda PageWidth (Sección de propiedades de página)

Determina el ancho de la página impresa en las unidades de dibujo.
  
## <a name="remarks"></a>Comentarios

También puede establecer el ancho  de página  en la pestaña Tamaño  de página  del cuadro de diálogo Configurar página (en la ficha Diseño, haga clic en la flecha Configurar página) o redimensionando manualmente la página con el mouse. Para ello, arrastre el borde de la página mientras mantiene presionada la tecla CTRL. 
  
Para obtener una referencia a la celda PageWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PageWidth  <br/> |
   
Para obtener una referencia desde un programa a la celda PageWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageWidth** <br/> |
   

