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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823216"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>Celda ShdwForegnd (sección Formato de relleno)

Determina el color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
  
## <a name="remarks"></a>Observaciones

Para establecer el color, escriba un número entre 0 y 23, que corresponde al índice de la colección de colores.
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet. Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior. 
  
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
   

