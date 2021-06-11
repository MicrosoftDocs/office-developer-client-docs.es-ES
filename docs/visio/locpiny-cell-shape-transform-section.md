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
description: 'Representa la coordenada y del pin de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410598"
---
# <a name="locpiny-cell-shape-transform-section"></a>Celda LocPinY (Sección de transformación de forma)

Representa la  *coordenada y*  del pin de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada es: 
  
= Alto \* 0,5
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LocPinY  <br/> |
   
Para obtener una referencia desde un programa a la celda LocPinY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowXFormOut** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinY** <br/> |
   

