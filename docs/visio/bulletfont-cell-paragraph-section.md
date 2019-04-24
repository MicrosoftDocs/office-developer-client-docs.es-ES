---
title: Celda BulletFont (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Representa el número de la fuente empleada para dar formato al texto cuando se especifica una cadena de viñeta personalizada y el valor de la celda Bullet no es cero.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337558"
---
# <a name="bulletfont-cell-paragraph-section"></a>Celda BulletFont (Sección de párrafo)

Representa el número de la fuente empleada para dar formato al texto cuando se especifica una cadena de viñeta personalizada y el valor de la celda Bullet no es cero. 
  
## <a name="remarks"></a>Comentarios

Los números de fuente varían según las fuentes instaladas en el sistema. Si el valor es 0 y hay una cadena de viñeta personalizada, la fuente utilizada será la misma que la del primer carácter del párrafo.
  
Para obtener una referencia a la celda BulletFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para. BulletFont [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda BulletFont por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visBulletFont** <br/> |
   

