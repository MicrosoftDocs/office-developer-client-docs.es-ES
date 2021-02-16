---
title: Celda Visible (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Especifica si las formas de la capa son visibles en la página de dibujo.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405453"
---
# <a name="visible-cell-layers-section"></a>Celda Visible (sección de capas)

Especifica si las formas de la capa son visibles en la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Las formas son visibles.  <br/> |
|FALSE  <br/> |Las formas están ocultas.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la  opción **Visible** del cuadro  de diálogo  Propiedades de capa (en la ficha Inicio, en el grupo Edición, haga clic en Capas y, a continuación, haga clic en **Propiedades de capa).** 
  
Para obtener una referencia a la celda Visible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Visible[ *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Visible por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerVisible** <br/> |
   

