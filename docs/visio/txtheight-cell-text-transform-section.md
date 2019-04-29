---
title: Celda TxtHeight (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Determina el alto del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409310"
---
# <a name="txtheight-cell-text-transform-section"></a>Celda TxtHeight (Sección de transformación de texto)

Determina el alto del bloque de texto. La fórmula predeterminada es:
  
= Altura \* 1
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtHeight  <br/> |
   
Para obtener una referencia desde un programa a la celda TxtHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormHeight** <br/> |
   

