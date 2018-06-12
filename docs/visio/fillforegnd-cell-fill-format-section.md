---
title: Celda FillForegnd (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Determina el color utilizado para el primer plano (trazo) de la trama de relleno de la forma.
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822146"
---
# <a name="fillforegnd-cell-fill-format-section"></a>Celda FillForegnd (Sección de formato de relleno)

Determina el color utilizado para el primer plano (trazo) de la trama de relleno de la forma.
  
## <a name="remarks"></a>Observaciones

Para establecer el color, escriba un número entre el 0 y el 23.
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet. Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior. 
  
Puede establecer la transparencia del relleno de primer plano en la celda FillForegndTrans.
  
Para obtener una referencia a la celda FillForegnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |FillForegnd  <br/> |
   
Para obtener una referencia a la celda FillForegnd por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillForegnd** <br/> |
   

