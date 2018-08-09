---
title: Celda DontMoveChildren (Sección de propiedades del grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Determina si se puede utilizar el mouse (ratón) para arrastrar las formas de un grupo.
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822011"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>Celda DontMoveChildren (sección Propiedades de grupo)

Determina si se puede utilizar el mouse (ratón) para arrastrar las formas de un grupo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | No se permite el uso del mouse para arrastrar las formas de un grupo.  <br/> |
| FALSE  <br/> | Se permite el uso del mouse para arrastrar las formas de un grupo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el valor de esta celda es TRUE, puede voltear, girar o cambiar el tamaño y la posición de las formas de los grupos mediante otros métodos.
  
El valor de esta celda es TRUE para los grupos de los patrones e instancias de patrones que se crearon en versiones de Microsoft Visio anteriores a Visio 2000.
  
Para obtener una referencia a la celda DontMoveChildren por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DontMoveChildren  <br/> |
   
Para obtener una referencia desde un programa a la celda DontMoveChildren por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGroup** <br/> |
| Índice de celda:  <br/> |**visGroupDontMoveChildren** <br/> |
   

