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
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316467"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>Celda LineJumpFactorX (sección de diseño de página)

Determina el tamaño de los saltos de línea en los conectores dinámicos horizontales de la página con respecto al valor de la celda LineToLineX. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
  
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineJumpFactorX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineJumpFactorX  <br/> |
   
Para obtener una referencia desde un programa a la celda LineJumpFactorX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOJumpFactorX** <br/> |
   

