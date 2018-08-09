---
title: Celda FlipY (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Indica si la forma se ha volteado verticalmente.
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822152"
---
# <a name="flipy-cell-shape-transform-section"></a>Celda FlipY (sección Transformación de forma)

Indica si la forma se ha volteado verticalmente.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma se ha volteado verticalmente.  <br/> |
| FALSE  <br/> | La forma no se ha volteado verticalmente.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda FlipY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | FlipY  <br/> |
   
Para obtener una referencia desde un programa a la celda FlipY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowXFormOut** <br/> |
| Índice de celda:  <br/> |**visXFormFlipY** <br/> |
   

