---
title: Celda ShapeShdwShow (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina si la forma muestra una sombra, como un número entero de 0 a 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422120"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Celda ShapeShdwShow (Sección de formato de relleno)

Determina si la forma muestra una sombra, como un número entero de 0 a 2.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Muestra siempre la sombra si se especifica una sombra. No se muestran las sombras de las subformas.  <br/> |
|1   <br/> |No represente una sombra a menos que la forma no tenga un elemento primario. Use sombras de sub shape si se agrupan.  <br/> |
|2   <br/> |Muestra siempre una sombra si se especifica una sombra. Se muestran las sombras de las subformas.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ShapeShdwShow** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShapeShdwShow  <br/> |
   
Para obtener una referencia desde un programa a la celda **ShapeShdwShow** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowFill** <br/> |
| Índice de celda:  <br/> |**visFillShdwShow** <br/> |
   

