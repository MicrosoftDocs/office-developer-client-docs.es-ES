---
title: Celda BulletString (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permite crear un estilo de viñeta personalizado.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821702"
---
# <a name="bulletstring-cell-paragraph-section"></a>Celda BulletString (Sección de párrafo)

Permite crear un estilo de viñeta personalizado. 
  
## <a name="remarks"></a>Observaciones

Especifique el estilo como una cadena (entre comillas). Por ejemplo, podría escribir la cadena "ooo".
  
Puede también establecer el valor de esta celda, bien de una forma, que señala al **formato**, haga clic en **texto**y, a continuación, haga clic en la ficha **viñetas** . 
  
Para obtener una referencia a la celda BulletString por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Para.BulletStr [ *i* ] donde *i* = < 1 >, 2, 3,...  <br/> |
   
Para obtener una referencia a la celda BulletString por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionParagraph** <br/> |
|Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visBulletString** <br/> |
   

