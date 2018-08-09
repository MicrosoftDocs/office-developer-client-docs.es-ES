---
title: Celda Tip (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Representa una cadena de texto descriptivo que aparece como información sobre herramientas cuando el usuario deja el puntero sobre el controlador de una forma. La aplicación agrega automáticamente comillas a la cadena de texto en la celda, pero las comillas no aparecen en la información sobre herramientas.
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823418"
---
# <a name="tip-cell-controls-section"></a>Celda Tip (sección Controles)

Representa una cadena de texto descriptivo que aparece como información sobre herramientas cuando el usuario deja el puntero sobre el controlador de una forma. La aplicación agrega automáticamente comillas a la cadena de texto en la celda, pero las comillas no aparecen en la información sobre herramientas.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Tip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre* . Controles de Tipwhere.  *nombre* es el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda Tip por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlTip** <br/> |
   

