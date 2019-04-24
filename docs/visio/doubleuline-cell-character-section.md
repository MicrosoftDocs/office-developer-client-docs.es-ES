---
title: Celda DoubleULine (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Determina si el intervalo de texto tiene doble subrayado.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357466"
---
# <a name="doubleuline-cell-character-section"></a>Celda DoubleULine (Sección de caracteres)

Determina si el intervalo de texto tiene doble subrayado.
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto tiene doble subrayado.  <br/> |
|FALSE  <br/> |El texto no tiene doble subrayado.  <br/> |
   
## <a name="remarks"></a>Comentarios

La celda DoubleULine contiene la información de formato que se aplica a un subintervalo del texto de una forma si la sección de caracteres contiene varias filas. En caso contrario, contiene información de formato para todo el texto de la forma.
  
También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (haga clic en la flecha de **Fuente** en la ficha **Inicio**). 
  
Para obtener una referencia a la celda DoubleULine por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char. DblUnderline [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda DoubleULine por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterDblUnderline** <br/> |
   

