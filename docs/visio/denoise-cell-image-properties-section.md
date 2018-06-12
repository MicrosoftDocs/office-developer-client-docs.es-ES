---
title: Celda Denoise (Sección de propiedades de la imagen)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Quita el ruido (píxeles con niveles de color distribuidos aleatoriamente) de una imagen de mapa de bits. El valor predeterminado es 0%.
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821982"
---
# <a name="denoise-cell-image-properties-section"></a>Celda Denoise (Sección de propiedades de la imagen)

Quita el ruido (píxeles con niveles de color distribuidos aleatoriamente) de una imagen de mapa de bits. El valor predeterminado es 0%.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Denoise por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Denoise  <br/> |
   
Para obtener una referencia a la celda Denoise por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowImage** <br/> |
| Índice de celda:  <br/> |**visImageDenoise** <br/> |
   

