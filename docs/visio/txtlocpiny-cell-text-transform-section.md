---
title: Celda TxtLocPinY (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Determina la y-coordenadas del centro del bloque de texto de rotación en relación con el origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823453"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Celda TxtLocPinY (Sección de transformación de texto)

Determina la *y* -coordenadas del centro del bloque de texto de rotación en relación con el origen del bloque de texto. La fórmula predeterminada es: 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda TxtLocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtLocPinY  <br/> |
   
Para obtener una referencia a la celda TxtLocPinY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinY** <br/> |
   

