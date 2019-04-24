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
description: 'Determina la coordenada y del centro de rotación del bloque de texto en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316425"
---
# <a name="txtpiny-cell-text-transform-section"></a>Celda TxtPinY (Sección de transformación de texto)

Determina la coordenada *y* del centro de rotación del bloque de texto en relación con el origen de la forma. La fórmula predeterminada es: 
  
= Altura \* 0,5
  
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
   

