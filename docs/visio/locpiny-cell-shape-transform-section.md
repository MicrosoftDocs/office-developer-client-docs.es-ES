---
title: Celda LocPinY (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Representa la y-coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada para determinar LocPinY es:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822543"
---
# <a name="locpiny-cell-shape-transform-section"></a>Celda LocPinY (Sección de transformación de forma)

Representa la *y* -coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada para determinar LocPinY es: 
  
= Alto \* 0,5
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda LocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LocPinY  <br/> |
   
Para obtener una referencia a la celda LocPinY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowXFormOut** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinY** <br/> |
   

