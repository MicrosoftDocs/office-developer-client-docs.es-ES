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
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821704"
---
# <a name="bulletfont-cell-paragraph-section"></a>Celda BulletFont (sección Párrafo)

Representa el número de la fuente empleada para dar formato al texto cuando se especifica una cadena de viñeta personalizada y el valor de la celda Bullet no es cero. 
  
## <a name="remarks"></a>Comentarios

Los números de fuente varían según las fuentes instaladas en el sistema. Si el valor es 0 y hay una cadena de viñeta personalizada, la fuente utilizada será la misma que la del primer carácter del párrafo.
  
Para obtener una referencia a la celda BulletFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.BulletFont [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda BulletFont por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visBulletFont** <br/> |
   

