---
title: Celda TxtPinY (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Determina la y-coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823461"
---
# <a name="txtpiny-cell-text-transform-section"></a>Celda TxtPinY (sección Transformación de texto)

Determina la *y* -coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma. La fórmula predeterminada es: 
  
= Alto \* 0,5
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtPinY  <br/> |
   
Para obtener una referencia desde un programa a la celda TxtPinY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormPinY** <br/> |
   

