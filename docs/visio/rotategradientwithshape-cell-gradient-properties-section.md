---
title: Celda RotateGradientWithShape (sección Propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina si un degradado de relleno gira con una forma en rotación 2D, como un valor boolean.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822996"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>Celda RotateGradientWithShape (sección Propiedades de degradado)

Determina si un degradado de relleno gira con una forma en rotación 2D, como un valor boolean.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El degradado se gira con la forma cuando se gira la forma alrededor del eje de giro. La parte "superior" del degradado es paralela al controlador de giro.  <br/> |
|FALSE  <br/> |El degradado no gira con la forma cuando se gira la forma alrededor del eje de giro. La parte "superior" del degradado es paralela al lienzo de dibujo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **RotateGradientWithShape** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | RotateGradientWithShape  <br/> |
   
Para obtener una referencia a la celda **RotateGradientWithShape** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGradientProperties** <br/> |
| Índice de celda:  <br/> |**visRotateGradientWithShape** <br/> |
   

