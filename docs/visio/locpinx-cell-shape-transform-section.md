---
title: Celda LocPinX (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Representa la x-coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada para determinar LocPinX es:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822556"
---
# <a name="locpinx-cell-shape-transform-section"></a>Celda LocPinX (sección Transformación de forma)

Representa la *x* -coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada para determinar LocPinX es: 
  
= Width \* 0,5
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LocPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LocPinX  <br/> |
   
Para obtener una referencia desde un programa a la celda LocPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowXFormOut** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinX** <br/> |
   

