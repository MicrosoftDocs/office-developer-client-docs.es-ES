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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337257"
---
# <a name="can-glue-cell-controls-section"></a>Celda Can Glue (Sección de controles)

Determina si un controlador puede pegarse a otras formas.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El controlador puede pegarse.  <br/> |
| FALSE  <br/> | El controlador no puede pegarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Can Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Mando.  *nombre* . Controles CanGluewhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda Can Glue por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2,...  <br/> |
| Índice de celda:  <br/> |**visCtlGlue** <br/> |
   

