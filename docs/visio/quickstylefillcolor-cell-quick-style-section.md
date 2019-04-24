---
title: Celda QuickStyleFillColor (sección estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Determina qué color del tema utiliza el relleno de una forma, como un entero entre 0 y 7.
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358732"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>Celda QuickStyleFillColor (sección estilos rápidos)

Determina qué color del tema utiliza el relleno de una forma, como un entero entre 0 y 7.
  
|||
|:-----|:-----|
|Valor  <br/> |Descripción  <br/> |
|comprendi  <br/> |El color de relleno de la forma hereda del color del tema oscuro.  <br/> |
|1  <br/> |El color de relleno de la forma hereda del color del tema claro.  <br/> |
|segundo  <br/> |El color de relleno de la forma hereda del color del tema énfasis 1  <br/> |
|3  <br/> |El color de relleno de la forma hereda del color del tema énfasis 2  <br/> |
|4  <br/> |El color de relleno de la forma hereda del color del tema énfasis 3  <br/> |
|2,5  <br/> |El color de relleno de la forma hereda del color del tema énfasis 4  <br/> |
|6,5  <br/> |El color de relleno de la forma hereda del color del tema énfasis 5  <br/> |
|0,7  <br/> |El color de relleno de la forma hereda del color del tema énfasis 6  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **QuickStyleFillColor** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | QuickStyleFillColor  <br/> |
   
Para obtener una referencia desde un programa a la celda **QuickStyleFillColor** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de celda:  <br/> |**visQuickStyleFillColor** <br/> |
   

