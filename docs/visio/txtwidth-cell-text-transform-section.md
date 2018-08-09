---
title: Celda TxtWidth (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Determina el ancho del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823477"
---
# <a name="txtwidth-cell-text-transform-section"></a>Celda TxtWidth (sección Transformación de texto)

Determina el ancho del bloque de texto. La fórmula predeterminada es:
  
= Width \* 1
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtWidth  <br/> |
   
Para obtener una referencia desde un programa a la celda TxtWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormWidth** <br/> |
   

