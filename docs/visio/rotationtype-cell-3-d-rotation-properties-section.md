---
title: Celda RotationType (sección de propiedades de giro 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina si la forma sigue una rotación paralela, una rotación en perspectiva o un giro oblicuo, como un número entero de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315676"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Celda RotationType (sección de propiedades de giro 3D)

Determina si la forma sigue una rotación paralela, una rotación en perspectiva o un giro oblicuo, como un número entero de 0 a 6. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |La forma no tiene giro.  <br/> |
|1  <br/> |La forma tiene una rotación en paralelo.  <br/> |
|segundo  <br/> |La forma tiene una rotación en perspectiva.  <br/> |
|3  <br/> |La forma tiene un giro oblicua superior izquierdo.  <br/> |
|4  <br/> |La forma tiene un giro oblicuo superior derecho.  <br/> |
|2,5  <br/> |La forma tiene un giro oblicuo de la parte inferior izquierda.  <br/> |
|6,5  <br/> |La forma tiene un giro oblicuo de la parte inferior derecha.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **RotationType** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |RotationType  <br/> |
   
Para obtener una referencia desde un programa a la celda **RotationType** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de celda:  <br/> |**visRotationType** <br/> |
   

