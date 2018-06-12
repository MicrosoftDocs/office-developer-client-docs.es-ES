---
title: Celda TxtLocPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Determina la x-coordenadas del centro del bloque de texto de rotación con respecto al origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823444"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Celda TxtLocPinX (Sección de transformación de texto)

Determina la *x* -coordenadas del centro del bloque de texto de rotación con respecto al origen del bloque de texto. La fórmula predeterminada es: 
  
= TxtWidth \* 0,5
  
Esta fórmula da como resultado el centro horizontal del bloque de texto.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtLocPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtLocPinX  <br/> |
   
Para obtener una referencia a la celda TxtLocPinX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinX** <br/> |
   

