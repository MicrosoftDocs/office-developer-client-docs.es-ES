---
title: Celda ShdwForegnd (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Determina el color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349108"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>Celda ShdwForegnd (Sección de formato de relleno)

Determina el color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
  
## <a name="remarks"></a>Comentarios

Para establecer el color, escriba un número entre 0 y 23, que corresponde al índice de la colección de colores.
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet. Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24. 
  
Puede establecer la transparencia del color de primer plano de la trama de relleno sombreado de la forma en la celda ShdwForegndTrans.
  
Para obtener una referencia a la celda ShdwForegnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShdwForegnd  <br/> |
   
Para obtener una referencia desde un programa a la celda ShdwForegnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowFill** <br/> |
| Índice de celda:  <br/> |**visFillShdwForegnd** <br/> |
   

