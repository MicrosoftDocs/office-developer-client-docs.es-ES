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
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430948"
---
# <a name="value-cell-text-fields-section"></a>Celda Value (Sección de campos de texto)

Contiene la función de un campo.
  
## <a name="remarks"></a>Comentarios

Puede establecer el valor de esta celda mediante el cuadro de diálogo **Campo** (en la ficha **Insertar**, en el grupo **Texto**, haga clic en **Campo**).
  
Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Fields.Value[ *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionTextField** <br/> |
|Índice de fila:  <br/> |**visRowField**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFieldCell** <br/> |
   

