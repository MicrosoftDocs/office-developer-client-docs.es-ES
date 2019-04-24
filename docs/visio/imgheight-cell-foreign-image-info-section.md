---
title: Celda ImgHeight (Sección de información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Determina el alto de la imagen del objeto dentro de su borde. La fórmula predeterminada es:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344936"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>Celda ImgHeight (Sección de información de imagen externa)

Determina el alto de la imagen del objeto dentro de su borde. La fórmula predeterminada es:
  
= Altura \* 1
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda ImgHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ImgHeight  <br/> |
   
Para obtener una referencia desde un programa a la celda ImgHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowForeign** <br/> |
| Índice de celda:  <br/> |**visFrgnImgHeight** <br/> |
   

