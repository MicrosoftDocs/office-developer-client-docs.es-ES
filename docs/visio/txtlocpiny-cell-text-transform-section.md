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
description: 'Determina la coordenada y del centro de rotación del bloque de texto con relación al origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414063"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Celda TxtLocPinY (Sección de transformación de texto)

Determina la  *coordenada y*  del centro de rotación del bloque de texto con relación al origen del bloque de texto. La fórmula predeterminada es: 
  
= TxtHeight \* 0.5
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtLocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtLocPinY  <br/> |
   
Para obtener una referencia desde un programa a la celda TxtLocPinY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinY** <br/> |
   

