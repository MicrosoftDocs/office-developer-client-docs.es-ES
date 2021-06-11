---
title: Celda KeepTextFlat (sección Propiedades de rotación 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica si el texto de una forma omitirá el giro de la forma en 3D. No se aplica a la rotación 2D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422043"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Celda KeepTextFlat (sección Propiedades de rotación 3D)

Indica si el texto de una forma omitirá el giro de la forma en 3D. No se aplica a la rotación 2D. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto de la forma no gira con la geometría de la forma.  <br/> |
|FALSE  <br/> |El texto de la forma se transforma para girar con la geometría de la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la **celda KeepTextFlat** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |KeepTextFlat  <br/> |
   
Para obtener una referencia desde un programa a la **celda KeepTextFlat** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de celda:  <br/> |**visKeepTextFlat** <br/> |
   

