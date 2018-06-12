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
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823457"
---
# <a name="txtheight-cell-text-transform-section"></a>Celda TxtHeight (Sección de transformación de texto)

Determina el alto del bloque de texto. La fórmula predeterminada es:
  
= Alto \* 1
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda TxtHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtHeight  <br/> |
   
Para obtener una referencia a la celda TxtHeight por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormHeight** <br/> |
   

