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
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322515"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>Celda FillBkgnd (Sección de formato de relleno)

Determina el color utilizado para el fondo (relleno) de la trama de relleno de la forma.
  
## <a name="remarks"></a>Comentarios

Para establecer el color, escriba un número entre el 0 y el 23.
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB. En la ventana ShapeSheet se mostrará RGB(*r, g, b*) en lugar de un número. Cuando se utilizan en operaciones numéricas, los colores personalizados tienen un valor igual o mayor que 24. 
  
Puede establecer la transparencia del relleno de fondo en la celda FillBkgndTrans. 
  
Para obtener una referencia a la celda FillBkgnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | FillBkgnd  <br/> |
   
Para obtener una referencia desde un programa a la celda FillBkgnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowFill** <br/> |
| Índice de celda:  <br/> |**visFillBkgnd** <br/> |
   

