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
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417451"
---
# <a name="flipy-cell-shape-transform-section"></a>Celda FlipY (sección de transformación de forma)

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
   

