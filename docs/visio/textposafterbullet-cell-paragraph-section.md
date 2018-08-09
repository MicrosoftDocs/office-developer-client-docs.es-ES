---
title: Celda TextPosAfterBullet (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Representa la distancia entra la primera línea del párrafo y la viñeta.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823385"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>Celda TextPosAfterBullet (sección Párrafo)

Representa la distancia entra la primera línea del párrafo y la viñeta. 
  
## <a name="remarks"></a>Comentarios

Esta distancia se suma a la contenida en la celda IndFirst, que es la sangría izquierda predeterminada. Este valor no depende de la escala de dibujo. 
  
Para obtener una referencia a la celda TextPosAfterBullet por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.TextPosAfterBullet [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda TextPosAfterBullet por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visTextPosAfterBullet** <br/> |
   

