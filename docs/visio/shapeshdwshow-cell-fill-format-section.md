---
title: Celda ShapeShdwShow (sección Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina si la forma muestra una sombra, como un número entero de 0 a 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823175"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Celda ShapeShdwShow (sección Fill Format)

Determina si la forma muestra una sombra, como un número entero de 0 a 2.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Mostrar siempre la sombra si se especifica una sombra. No se muestran las sombras para las subformas.  <br/> |
|1  <br/> |No se representará una sombra a menos que la forma no tiene un elemento primario. Usar sombras de forma subcaracterística si se agrupan juntos.  <br/> |
|2  <br/> |Mostrar siempre una sombra si se especifica una sombra. Se muestran las sombras para las subformas.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **ShapeShdwShow** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShapeShdwShow  <br/> |
   
Para obtener una referencia a la celda **ShapeShdwShow** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowFill** <br/> |
| Índice de celda:  <br/> |**visFillShdwShow** <br/> |
   

