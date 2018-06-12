---
title: Celda TxtPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina la x-coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823455"
---
# <a name="txtpinx-cell-text-transform-section"></a>Celda TxtPinX (Sección de transformación de texto)

Determina la *x* -coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma. La fórmula predeterminada es: 
  
= Width \* 0,5
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda TxtPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtPinX  <br/> |
   
Para obtener una referencia a la celda TxtPinX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormPinX** <br/> |
   

