---
title: Celda FillBkgnd (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Determina el color utilizado para el fondo (relleno) de la trama de relleno de la forma.
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822125"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>Celda FillBkgnd (Sección de formato de relleno)

Determina el color utilizado para el fondo (relleno) de la trama de relleno de la forma.
  
## <a name="remarks"></a>Observaciones

Para establecer el color, escriba un número entre el 0 y el 23.
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB (*r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet. Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior. 
  
Puede establecer la transparencia del relleno de fondo en la celda FillBkgndTrans. 
  
Para obtener una referencia a la celda FillBkgnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | FillBkgnd  <br/> |
   
Para obtener una referencia a la celda FillBkgnd por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowFill** <br/> |
| Índice de celda:  <br/> |**visFillBkgnd** <br/> |
   

