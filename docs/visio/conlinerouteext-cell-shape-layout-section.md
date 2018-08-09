---
title: Celda ConLineRouteExt (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Determina la apariencia de un conector.
ms.openlocfilehash: 7724466b6ad225fcf39243bc80ba2e440f3b700b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821841"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>Celda ConLineRouteExt (sección Diseño de forma)

Determina la apariencia de un conector.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado (se usa la configuración de página)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Recta  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Curva  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda ConLineRouteExt por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ConLineRouteExt  <br/> |
   
Para obtener una referencia desde un programa a la celda ConLineRouteExt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
| Índice de celda:  <br/> |**visSLOLineRouteExt** <br/> |
   

