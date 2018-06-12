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
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823517"
---
# <a name="visible-cell-layers-section"></a>Celda Visible (sección de capas)

Especifica si las formas de la capa son visibles en la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Las formas son visibles.  <br/> |
|FALSE  <br/> |Las formas están ocultas.  <br/> |
   
## <a name="remarks"></a>Observaciones

Esta celda corresponde a la opción **Visible** en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio** , en el grupo **Edición** , haga clic en **capas**y, a continuación, haga clic en **Propiedades de las capas** ). 
  
Para obtener una referencia a la celda Visible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Visible [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Visible por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerVisible** <br/> |
   

