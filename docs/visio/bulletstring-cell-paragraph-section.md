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
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337565"
---
# <a name="bulletstring-cell-paragraph-section"></a>Celda BulletString (Sección de párrafo)

Permite crear un estilo de viñeta personalizado. 
  
## <a name="remarks"></a>Comentarios

Especifique el estilo como una cadena (entre comillas). Por ejemplo, podría escribir la cadena "ooo".
  
Asimismo, para establecer el valor de esta celda, haga clic con el botón secundario en una forma, elija **Formato**, haga clic en **Texto** y, a continuación, haga clic en la pestaña **Viñetas**. 
  
Para obtener una referencia a la celda BulletString por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Para. BulletStr [ *i* ] donde *i* = <1>, 2, 3,...  <br/> |
   
Para obtener una referencia desde un programa a la celda BulletString por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionParagraph** <br/> |
|Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visBulletString** <br/> |
   

