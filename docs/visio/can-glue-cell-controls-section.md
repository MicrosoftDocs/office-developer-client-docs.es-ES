---
title: Celda Can Glue (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Determina si un controlador puede pegarse a otras formas.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821684"
---
# <a name="can-glue-cell-controls-section"></a>Celda Can Glue (sección Controles)

Determina si un controlador puede pegarse a otras formas.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El controlador puede pegarse.  <br/> |
| FALSE  <br/> | El controlador no puede pegarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Can Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre* . Controles de CanGluewhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda Can Glue por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2,...  <br/> |
| Índice de celda:  <br/> |**visCtlGlue** <br/> |
   

