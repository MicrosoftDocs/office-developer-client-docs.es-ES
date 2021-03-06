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
description: Determina la cantidad de espacio vertical entre las formas de la página de dibujo al establecer formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Re-Layout Página y, a continuación, haga clic en Más opciones de diseño).
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420209"
---
# <a name="avenuesizey-cell-page-layout-section"></a>Celda AvenueSizeY (Sección de diseño de página)

Determina la cantidad de espacio vertical entre las formas de la  página de dibujo al  establecer formas mediante el  cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Página de nuevo diseño y, a continuación, haga clic en Más opciones de **diseño).** 
  
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **Espaciado del diseño y el enrutamiento** (en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página**, haga clic en la pestaña **Diseño y enrutamiento** y, a continuación, en **Espaciado**).
  
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
   

