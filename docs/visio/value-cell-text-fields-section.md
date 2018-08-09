---
title: Celda Value (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contiene la función de un campo.
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823503"
---
# <a name="value-cell-text-fields-section"></a>Celda Value (sección Campos de texto)

Contiene la función de un campo.
  
## <a name="remarks"></a>Observaciones

Puede establecer el valor de esta celda mediante el cuadro de diálogo **Campo** (en la ficha **Insertar**, en el grupo **Texto**, haga clic en **Campo**).
  
Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Fields.Value [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionTextField** <br/> |
|Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFieldCell** <br/> |
   

