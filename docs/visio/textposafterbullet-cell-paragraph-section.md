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
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422155"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>Celda TextPosAfterBullet (Sección de párrafo)

Representa la distancia entra la primera línea del párrafo y la viñeta. 
  
## <a name="remarks"></a>Comentarios

Esta distancia se suma a la contenida en la celda IndFirst, que es la sangría izquierda predeterminada. Este valor no depende de la escala de dibujo. 
  
Para obtener una referencia a la celda TextPosAfterBullet por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.TextPosAfterBullet[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda TextPosAfterBullet por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visTextPosAfterBullet** <br/> |
   

