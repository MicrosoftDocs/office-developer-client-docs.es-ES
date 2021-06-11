---
title: Celda QuickStyleFillColor (sección Estilo rápido)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Determina qué color de tema usa el relleno de una forma, como un entero de 0 a 7
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407966"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>Celda QuickStyleFillColor (sección Estilo rápido)

Determina qué color de tema usa el relleno de una forma, como un entero de 0 a 7
  
|||
|:-----|:-----|
|Valor  <br/> |Descripción  <br/> |
|0  <br/> |El color de relleno de forma hereda del color del tema Oscuro.  <br/> |
|1  <br/> |El color de relleno de forma hereda del color del tema Light.  <br/> |
|2  <br/> |El color de relleno de la forma se hereda del color del tema Énfal 1  <br/> |
|3  <br/> |El color de relleno de la forma se hereda del color del tema Énfal 2  <br/> |
|4   <br/> |El color de relleno de la forma se hereda del color del tema Énfal 3  <br/> |
|5   <br/> |El color de relleno de la forma se hereda del color del tema Énfal 4  <br/> |
|6   <br/> |El color de relleno de la forma se hereda del color del tema Énfal 5  <br/> |
|7   <br/> |El color de relleno de forma se hereda del color del tema Énfénf 6  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la **celda QuickStyleFillColor** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | QuickStyleFillColor  <br/> |
   
Para obtener una referencia desde un programa a la **celda QuickStyleFillColor** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de celda:  <br/> |**visQuickStyleFillColor** <br/> |
   

