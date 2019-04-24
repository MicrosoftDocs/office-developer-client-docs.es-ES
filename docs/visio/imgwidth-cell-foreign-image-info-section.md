---
title: Celda ImgWidth (Sección de información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Determina el ancho de la imagen del objeto dentro de su borde. La fórmula predeterminada es:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344726"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>Celda ImgWidth (sección de información de imagen externa)

Determina el ancho de la imagen del objeto dentro de su borde. La fórmula predeterminada es:
  
= Ancho \* 1
  
Si se recorta el objeto, cambia el factor por el que se multiplica el ancho.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda ImgWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ImgWidth  <br/> |
   
Para obtener una referencia desde un programa a la celda ImgWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowForeign** <br/> |
| Índice de celda:  <br/> |**visFrgnImgWidth** <br/> |
   

