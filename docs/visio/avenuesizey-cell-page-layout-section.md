---
title: Celda AvenueSizeY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Determina la cantidad de espacio vertical entre las formas en la página de dibujo cuando se diseñan formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en página de diseño de Re y, a continuación, haga clic en más opciones de diseño).
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821553"
---
# <a name="avenuesizey-cell-page-layout-section"></a>Celda AvenueSizeY (sección Diseño de página)

Determina la cantidad de espacio vertical entre las formas en la página de dibujo cuando se diseñan formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño** , en el grupo **Diseño** , haga clic en página de **Diseño de Re** y, a continuación, haga clic en **más Opciones de diseño**).
  
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **Espaciado del diseño y el enrutamiento** (en la ficha **Diseño**, haga clic en la flecha en el grupo **Configurar página**, haga clic en la pestaña **Diseño y enrutamiento** y, a continuación, en **Espaciado**).
  
La cuadrícula dinámica emplea la configuración de la celda AvenueSizeY cuando solo hay una forma disponible para calcular el espacio vertical. Para usar la cuadrícula dinámica, en la ficha **Ajustar y pegar**, en el grupo **Herramientas**, seleccione **Cuadrícula dinámica**.
  
Para obtener una referencia a la celda AvenueSizeY por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | AvenueSizeY  <br/> |
   
Para obtener una referencia desde un programa a la celda AvenueSizeY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOAvenueSizeY** <br/> |
   

