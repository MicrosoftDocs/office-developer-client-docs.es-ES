---
title: Celda RotateGradientWithShape (sección Propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina si un degradado de relleno gira con una forma en rotación 2D, como un valor booleano.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412222"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>Celda RotateGradientWithShape (sección Propiedades de degradado)

Determina si un degradado de relleno gira con una forma en rotación 2D, como un valor booleano.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El degradado gira con la forma cuando se gira la forma alrededor del eje de rotación. La "parte superior" del degradado es paralela al controlador de giro.  <br/> |
|FALSE  <br/> |El degradado no gira con la forma cuando se gira la forma alrededor del eje de rotación. La "parte superior" del degradado es paralela al lienzo de dibujo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **RotateGradientWithShape** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | RotateGradientWithShape  <br/> |
   
Para obtener una referencia desde un programa a la celda **RotateGradientWithShape** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGradientProperties** <br/> |
| Índice de celda:  <br/> |**visRotateGradientWithShape** <br/> |
   

