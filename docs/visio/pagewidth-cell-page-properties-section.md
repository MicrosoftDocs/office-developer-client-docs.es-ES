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
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822733"
---
# <a name="pagewidth-cell-page-properties-section"></a>Celda PageWidth (sección Propiedades de impresión)

Determina el ancho de la página impresa en las unidades de dibujo.
  
## <a name="remarks"></a>Observaciones

También puede establecer el ancho de la página en la ficha **Tamaño de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ) o manualmente si cambia el tamaño de la página con el mouse. Para ello, arrastre el borde de la página mientras mantiene presionada la tecla CTRL. 
  
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
   

