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
description: Contiene celdas que definen las coordenadas x-e y-y el comportamiento de cada controlador definido para una forma. Una forma contendrá una fila de controles para cada controlador de control.
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282960"
---
# <a name="controls-row-controls-section"></a>Fila Controls (Sección de controles)

Contiene celdas que definen las coordenadas *x* - ** e y-y el comportamiento de cada controlador definido para una forma. Una forma contendrá una fila de controles para cada controlador de control. 
  
Las filas Controls se denominan Controls. *nombre* y contienen las celdas siguientes. Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Representa la coordenada *x* que indica la ubicación del controlador de una forma en coordenadas locales.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Representa la coordenada *y* que indica la ubicación del controlador de una forma en coordenadas locales.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Representa la coordenada *x* de un punto de anclaje del controlador en coordenadas locales.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Representa la coordenada *y* de un punto de anclaje del controlador en coordenadas locales.  <br/> |
|[X Behavior](x-behavior-cell-controls-section.md) <br/> |Controla el comportamiento de la coordenada *x* del controlador que va a mostrar después de mover el controlador.  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |Controla el comportamiento de la coordenada *y* del controlador una vez que se ha movido el controlador.  <br/> |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |Determina si un controlador puede pegarse a otras formas.  <br/> |
|[Sugerencia](tip-cell-controls-section.md) <br/> |Representa una cadena de texto descriptivo que aparece como información de herramientas cuando el usuario deja el puntero sobre el controlador de una forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

 Puede agregar todas las filas Controls.  Asigne un *nombre* a las filas que necesite, asigne nombres descriptivos a las filas y establezca los valores de las celdas. Para agregar controladores a una sección de controles existente, haga clic con el botón secundario en una fila y, después, haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet como texto en color rojo. Para asignar un nombre descriptivo a una fila Controls. *nombre* filas, haga clic en la fila y, a continuación, escriba *personalizada* , por ejemplo, para crear el nombre de fila Controls. Custom. Después, podrá hacer referencia a la celda X usando Controls.Personalizada.X. 
  
El nombre de fila que escriba debe ser único en la sección.
  

