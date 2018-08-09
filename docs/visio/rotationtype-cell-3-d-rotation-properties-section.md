---
title: Celda RotationType (sección de propiedades de giro 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina si la forma sigue un giro paralelo, una rotación en perspectiva o un giro oblicua, como un número entero de 0 a 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823040"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Celda RotationType (sección de propiedades de giro 3D)

Determina si la forma sigue un giro paralelo, una rotación en perspectiva o un giro oblicua, como un número entero de 0 a 6. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |La forma no tiene ningún giro.  <br/> |
|1  <br/> |La forma tiene un giro en paralelo.  <br/> |
|2  <br/> |La forma tiene una rotación en perspectiva.  <br/> |
|3  <br/> |La forma tiene un giro oblicua hacia arriba e izquierdo superior.  <br/> |
|4  <br/> |La forma tiene un giro oblicuo derecha superior.  <br/> |
|5  <br/> |La forma tiene un giro de oblicua hacia arriba e izquierda inferior.  <br/> |
|6  <br/> |La forma tiene un inferior giro oblicua hacia la derecha.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **RotationType** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |RotationType  <br/> |
   
Para obtener una referencia a la celda **RotationType** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de celda:  <br/> |**visRotationType** <br/> |
   

