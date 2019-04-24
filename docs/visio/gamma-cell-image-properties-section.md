---
title: Celda Gamma (Sección de propiedades de la imagen)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajusta o corrige la intensidad de una imagen para un dispositivo específico de salida, como por ejemplo un monitor o un escáner. El valor predeterminado es 1 (sin corrección).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315207"
---
# <a name="gamma-cell-image-properties-section"></a>Celda Gamma (Sección de propiedades de la imagen)

Ajusta o corrige la intensidad de una imagen para un dispositivo específico de salida, como por ejemplo un monitor o un escáner. El valor predeterminado es 1 (sin corrección).
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Gamma por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Gamma  <br/> |
   
Para obtener una referencia desde un programa a la celda Gamma por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowImage** <br/> |
| Índice de celda:  <br/> |**visImageGamma** <br/> |
   

