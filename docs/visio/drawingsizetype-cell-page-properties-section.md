---
title: Celda DrawingSizeType (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Determina el tamaño del dibujo.
ms.openlocfilehash: 33c85b6c2f0587654038eaec1a9490ca8bd8301b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425452"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>Celda DrawingSizeType (Sección de propiedades de página)

Determina el tamaño del dibujo.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Igual que la impresora  <br/> |**visPrintSetup** <br/> |
|1  <br/> |Ajustar la página al contenido del dibujo  <br/> |**visTight** <br/> |
|2  <br/> |Estándar  <br/> |**visStandard** <br/> |
|3  <br/> |Tamaño de página personalizado  <br/> |**visCustom** <br/> |
|4   <br/> |Tamaño del dibujo a escala personalizada  <br/> |**visLogical** <br/> |
|5   <br/> |Métrico (ISO)  <br/> |**visDSMetric** <br/> |
|6   <br/> |Ingeniería ANSI  <br/> |**visDSEngr** <br/> |
|7   <br/> |De arquitectura ANSI  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el tamaño del dibujo, use el cuadro de diálogo **Configurar página** (haga clic en la flecha **Configurar página** en la ficha **Diseño**) o cambie el tamaño de la página manualmente con el mouse. 
  
Para obtener una referencia a la celda DrawingSizeType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |DrawingSizeType  <br/> |
   
Para obtener una referencia desde un programa a la celda DrawingSizeType por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageDrawSizeType** <br/> |
   

