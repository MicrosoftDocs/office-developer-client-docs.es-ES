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
description: Un valor RGB que representa el color asignado a las marcas de revisión de un documento.
ms.openlocfilehash: a8771bb35cfc1b57990f24e1a0a3d677f9cffc0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821784"
---
# <a name="color-cell-reviewer-section"></a>Celda Color (sección Revisor)

Un valor RGB que representa el color asignado a las marcas de revisión de un documento. 
  
## <a name="remarks"></a>Comentarios

Los colores se asignan a los revisores en la siguiente secuencia: rojo, azul, verde, violeta, naranja, turquesa y gris. Cuando acaba la secuencia, se vuelve a empezar desde el principio, según vayan agregándose revisores al proceso. 
  
Los comentarios incluidos en la página de dibujo original siempre aparecen en amarillo, independientemente del color asignado al revisor en la celda Color. 
  
Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Reviewer.Color [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionReviewer** <br/> |
| Índice de fila:  <br/> |**visRowReviewer** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visReviewerColor** <br/> |
   

