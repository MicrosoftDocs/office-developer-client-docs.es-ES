---
title: Celda Color (Sección de revisor)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Valor RGB que representa el color asignado a la marca de revisión de un documento.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341821"
---
# <a name="color-cell-reviewer-section"></a>Celda Color (Sección de revisor)

Valor RGB que representa el color asignado a la marca de revisión de un documento. 
  
## <a name="remarks"></a>Comentarios

Los colores se asignan a los revisores en la siguiente secuencia: rojo, azul, verde, violeta, naranja, turquesa y gris. Cuando acaba la secuencia, se vuelve a empezar desde el principio, según vayan agregándose revisores al proceso. 
  
Los comentarios incluidos en la página de dibujo original siempre aparecen en amarillo, independientemente del color asignado al revisor en la celda Color. 
  
Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Reviewer. color [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionReviewer** <br/> |
| Índice de fila:  <br/> |**visRowReviewer** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visReviewerColor** <br/> |
   

