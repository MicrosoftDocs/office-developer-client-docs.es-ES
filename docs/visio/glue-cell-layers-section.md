---
title: Celda Glue (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Determina si las formas que pertenecen a la capa pueden pegarse.
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822225"
---
# <a name="glue-cell-layers-section"></a>Celda Glue (Sección de capas)

Determina si las formas que pertenecen a la capa pueden pegarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se pueden pegar.  <br/> |
|FALSE  <br/> |No se pueden pegar.  <br/> |
   
## <a name="remarks"></a>Observaciones

Esta celda corresponde a la opción de **pegado** en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio** , en el grupo **Edición** , haga clic en **capas**y, a continuación, haga clic en **Propiedades de las capas** ). 
  
Para obtener una referencia a la celda Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Glue [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Glue por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerGlue** <br/> |
   

