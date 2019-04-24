---
title: Celda LineJumpFactorY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Determina el tamaño de los saltos de línea en los conectores dinámicos verticales de la página con respecto al valor de la celda LineToLineY. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
ms.openlocfilehash: 36712c1558ff2f50309dc31e8f918061180c8fa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316460"
---
# <a name="linejumpfactory-cell-page-layout-section"></a>Celda LineJumpFactorY (sección de diseño de página)

Determina el tamaño de los saltos de línea en los conectores dinámicos verticales de la página con respecto al valor de la celda LineToLineY. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
  
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineJumpFactorY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineJumpFactorY  <br/> |
   
Para obtener una referencia desde un programa a la celda LineJumpFactorY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOJumpFactorY** <br/> |
   

