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
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408519"
---
# <a name="glue-cell-layers-section"></a>Celda Glue (Sección de capas)

Determina si las formas que pertenecen a la capa pueden pegarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se pueden pegar.  <br/> |
|FALSE  <br/> |No se pueden pegar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda corresponde a la  opción **Pegar** del cuadro  de diálogo  Propiedades de capa (en la ficha Inicio, en el grupo Edición, haga clic en Capas **y,** a continuación, haga clic en **Propiedades de capa).** 
  
Para obtener una referencia a la celda Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Glue[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Glue por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerGlue** <br/> |
   

