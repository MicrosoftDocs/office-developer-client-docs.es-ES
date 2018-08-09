---
title: Fila Controls (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
localization_priority: Normal
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: Contiene celdas que definen el x - e y-las coordenadas y el comportamiento de cada controlador definen para una forma. Una forma contendrá una fila Controls por cada controlador.
ms.openlocfilehash: ed1d57fce6d413b9eb7f5d119264bc2bfa968222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821871"
---
# <a name="controls-row-controls-section"></a>Fila Controls (sección Controles)

Contiene celdas que definen el *x* - e *y* -las coordenadas y el comportamiento de cada controlador definen para una forma. Una forma contendrá una fila Controls por cada controlador. 
  
Las filas Controls se denominan controles. *nombre* y contienen las celdas siguientes. Para obtener más información, vea los temas de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Representa la *x* -coordenada que indica la ubicación del controlador de una forma en coordenadas locales.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Representa la *y* -coordenada que indica la ubicación del controlador de una forma en coordenadas locales.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Representa la *x* -coordenadas de punto de anclaje del controlador en coordenadas locales.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Representa la *y* -coordenadas de punto de anclaje del controlador en coordenadas locales.  <br/> |
|[X comportamiento](x-behavior-cell-controls-section.md) <br/> |Controla el tipo de comportamiento de la *x* -coordenada del controlador cuando éste se mueve.  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |Controla el tipo de comportamiento de la *y* -coordenada del controlador cuando éste se mueve.  <br/> |
|[Puede pegar](can-glue-cell-controls-section.md) <br/> |Determina si un controlador puede pegarse a otras formas.  <br/> |
|[Sugerencia](tip-cell-controls-section.md) <br/> |Representa una cadena de texto descriptivo que aparece como información de herramientas cuando el usuario deja el puntero sobre el controlador de una forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

 Puede agregar tantos controles.  *nombre* como sea necesario, asignar nombres descriptivos a las filas y establecer valores de celda. Para agregar controladores a una sección de controles existente, haga clic en una fila y haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet en texto de color rojo. Para asignar nombres descriptivos a los controles. filas de *nombre* , haga clic en la fila y, a continuación, escriba *personalizada* , por ejemplo, para crear el nombre de fila Controls.descripción. A continuación, puede hacer referencia a la celda X usando Controls.personalizada.x. 
  
El nombre de fila que escriba debe ser único en la sección.
  

