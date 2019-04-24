---
title: Fila Hyperlink (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329907"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Fila Hyperlink (Sección de hipervínculos)

Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.
  
Las filas Hyperlink se denominan Hyperlink. *nombre* y contienen las celdas siguientes. Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[Descripción](description-cell-hyperlinks-section.md) <br/> |Texto descriptivo del hipervínculo.  <br/> |
|[Address](address-cell-hyperlinks-section.md) <br/> |Dirección URL, nombre de archivo MS-DOS o ruta UNC de destino.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Ubicación dentro del documento de destino.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Cadena de texto que pasa información utilizada para obtener una dirección URL.  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Nombre de un marco de destino cuando Microsoft Office Visio se abre como documento Active en un contenedor ActiveX. El valor predeterminado es una cadena vacía.  <br/> |
|[Criterio](sortkey-cell-hyperlinks-section.md) <br/> |Determina el orden de los hipervínculos en el menú contextual.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Especifica si el hipervínculo se abre en una ventana nueva. Si es TRUE, se abre la página vinculada, el documento o el sitio web en una nueva ventana. El valor predeterminado es FALSE.  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |Hipervínculo predeterminado de una forma o de una página.  <br/> |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Indica si el hipervínculo aparece o no en el menú contextual.  <br/> |
   
## <a name="remarks"></a>Comentarios

 Puede agregar tantas filas Hyperlink.  Asigne un *nombre* a las filas que necesite, asigne nombres descriptivos a las filas y establezca los valores de las celdas. Para agregar hipervínculos a una sección de hipervínculos existente, haga clic con el botón secundario en una fila y, después, haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet como texto en color rojo. Para asignar un nombre descriptivo a una fila Hyperlink. *nombre* filas, haga clic en la fila y, a continuación, escriba un nombre como *marketing* , por ejemplo, para crear el nombre de fila Hyperlink. marketing. Después, podrá hacer referencia a la celda Description usando Hyperlink.Marketing.Description. 
  
El nombre de fila que escriba debe ser único en la sección.
  

