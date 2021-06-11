---
title: Celda RotationType (sección Propiedades de rotación 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina si la forma sigue una rotación paralela, una rotación de perspectiva o una rotación oblicua, como un entero de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422946"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Celda RotationType (sección Propiedades de rotación 3D)

Determina si la forma sigue una rotación paralela, una rotación de perspectiva o una rotación oblicua, como un entero de 0 a 6. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |La forma no tiene ninguna rotación.  <br/> |
|1  <br/> |La forma tiene un giro paralelo.  <br/> |
|2  <br/> |La forma tiene un giro de perspectiva.  <br/> |
|3  <br/> |La forma tiene un giro oblicua superior izquierdo.  <br/> |
|4   <br/> |La forma tiene un giro oblicua superior derecho.  <br/> |
|5   <br/> |La forma tiene un giro oblicua inferior izquierdo.  <br/> |
|6   <br/> |La forma tiene un giro oblicua inferior derecho.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la **celda RotationType** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |RotationType  <br/> |
   
Para obtener una referencia desde un programa a **la celda RotationType** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de celda:  <br/> |**visRotationType** <br/> |
   

