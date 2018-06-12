---
title: Celda LineJumpFactorX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Determina el tamaño de los saltos de línea en los conectores dinámicos horizontales de la página con respecto al valor de la celda LineToLineX. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822451"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>Celda LineJumpFactorX (Sección de diseño de página)

Determina el tamaño de los saltos de línea en los conectores dinámicos horizontales de la página con respecto al valor de la celda LineToLineX. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
  
## <a name="remarks"></a>Observaciones

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineJumpFactorX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineJumpFactorX  <br/> |
   
Para obtener una referencia a la celda LineJumpFactorX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOJumpFactorX** <br/> |
   

