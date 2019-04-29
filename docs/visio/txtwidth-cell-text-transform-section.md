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
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426096"
---
# <a name="txtwidth-cell-text-transform-section"></a>Celda TxtWidth (Sección de transformación de texto)

Determina el ancho del bloque de texto. La fórmula predeterminada es:
  
= Ancho \* 1
  
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
   

