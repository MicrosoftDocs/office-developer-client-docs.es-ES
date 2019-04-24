---
title: Celda AvenueSizeX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Determina la cantidad de espacio horizontal entre las formas en la página de dibujo cuando se disponen las formas con el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo diseño, haga clic en reDistribuir página y, a continuación, haga clic en más opciones de diseño).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338825"
---
# <a name="avenuesizex-cell-page-layout-section"></a>Celda AvenueSizeX (Sección de diseño de página)

Determina la cantidad de espacio horizontal entre las formas en la página de dibujo cuando se disponen las formas con el cuadro de diálogo **configurar diseño** (en la ficha **diseño** , en el grupo **diseño** , haga clic en **redistribuir página**y, a continuación, haga clic en * * más Opciones de diseño * *).
  
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **Espaciado del diseño y el enrutamiento** (en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página**, haga clic en la pestaña **Diseño y enrutamiento** y, a continuación, en **Espaciado**).
  
La cuadrícula dinámica emplea la configuración de la celda AvenueSizeX cuando solo hay una forma disponible para calcular el espacio horizontal. Para usar la cuadrícula dinámica, en la ficha **Ver**, en el grupo **Ayudas visuales**, seleccione **Cuadrícula dinámica**.
  
Para obtener una referencia a la celda AvenueSizeX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | AvenueSizeY  <br/> |
   
Para obtener una referencia desde un programa a la celda AvenueSizeX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOAvenueSizeX** <br/> |
   

