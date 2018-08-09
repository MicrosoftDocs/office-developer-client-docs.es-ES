---
title: Celda KeepTextFlat (sección de propiedades de giro 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica si el texto de una forma pasará por alto la rotación de la forma en 3D. No se aplica a la rotación 2D.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822398"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Celda KeepTextFlat (sección de propiedades de giro 3D)

Indica si el texto de una forma pasará por alto la rotación de la forma en 3D. No se aplica a la rotación 2D. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Texto de la forma no gira con la geometría de la forma.  <br/> |
|FALSE  <br/> |Texto de la forma se transforma para gira con la geometría de la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **KeepTextFlat** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |KeepTextFlat  <br/> |
   
Para obtener una referencia a la celda **KeepTextFlat** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de celda:  <br/> |**visKeepTextFlat** <br/> |
   

