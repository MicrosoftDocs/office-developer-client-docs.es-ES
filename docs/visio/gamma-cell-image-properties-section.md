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
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822210"
---
# <a name="gamma-cell-image-properties-section"></a>Celda Gamma (sección Propiedades de la imagen)

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
   

