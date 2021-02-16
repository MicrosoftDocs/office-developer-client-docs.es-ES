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
description: 'Representa la coordenada x del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439243"
---
# <a name="locpinx-cell-shape-transform-section"></a>Celda LocPinX (Sección de transformación de forma)

Representa la coordenada  *x*  del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada es: 
  
= Ancho \* 0,5
  
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
   

