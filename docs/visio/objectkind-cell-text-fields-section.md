---
title: Celda ObjectKind (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indica el tipo de campo de texto.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822683"
---
# <a name="objectkind-cell-text-fields-section"></a>Celda ObjectKind (sección Campos de texto)

Indica el tipo de campo de texto.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Estándar  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |Horizontal en vertical  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Comentarios

Los campos de texto pueden ser de uno de los dos siguientes tipos:
  
- Estándar, que indica que el campo se insertó por su categoría.
    
- Horizontal en vertical, que indica que el campo es de texto horizontal sobre texto vertical.
    
Para obtener una referencia a la celda ObjectKind por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.ObjectKind [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda ObjectKind por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldObjectKind** <br/> |
   

