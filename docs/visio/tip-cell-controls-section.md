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
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424864"
---
# <a name="tip-cell-controls-section"></a>Celda Tip (Sección de controles)

Representa una cadena de texto descriptivo que aparece como información sobre herramientas cuando el usuario deja el puntero sobre el controlador de una forma. La aplicación agrega automáticamente comillas a la cadena de texto en la celda, pero las comillas no aparecen en la información sobre herramientas.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Tip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Controles.  *nombre*  . Sugerencia en los controles.  *es*  el nombre de la fila de controles.  <br/> |
   
Para obtener una referencia desde un programa a la celda Tip por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionControls** <br/> |
| Índice de fila:  <br/> |**visRowControl**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCtlTip** <br/> |
   

