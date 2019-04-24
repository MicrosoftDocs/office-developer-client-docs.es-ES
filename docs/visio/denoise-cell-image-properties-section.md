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
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360252"
---
# <a name="denoise-cell-image-properties-section"></a>Celda Denoise (Sección de propiedades de la imagen)

Quita el ruido (píxeles con niveles de color distribuidos aleatoriamente) de una imagen de mapa de bits. El valor predeterminado es 0%.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Denoise por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Denoise  <br/> |
   
Para obtener una referencia desde un programa a la celda Denoise por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowImage** <br/> |
| Índice de celda:  <br/> |**visImageDenoise** <br/> |
   

