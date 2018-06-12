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
ms.openlocfilehash: 99295838f5d1860e3c34cf4e37866eb477fe81ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822304"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Fila Hyperlink (Sección de hipervínculos)

Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.
  
Las filas Hyperlink se denominan Hyperlink. *nombre* y contienen las celdas siguientes. Para obtener más información, vea los temas de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[Descripción](description-cell-hyperlinks-section.md) <br/> |Texto descriptivo del hipervínculo.  <br/> |
|[Dirección](address-cell-hyperlinks-section.md) <br/> |Dirección URL, nombre de archivo MS-DOS o ruta UNC de destino.  <br/> |
|[Subdirección](subaddress-cell-hyperlinks-section.md) <br/> |Ubicación dentro del documento de destino.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Cadena de texto que pasa información utilizada para obtener una dirección URL.  <br/> |
|[Marco](frame-cell-hyperlinks-section.md) <br/> |Nombre de un marco de destino cuando Microsoft Office Visio se abre como documento Active en un contenedor ActiveX. El valor predeterminado es una cadena vacía.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Determina el orden de los hipervínculos en el menú contextual.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Especifica si el hipervínculo se abre en una ventana nueva. Si es TRUE, la página, documento o sitio Web vinculado se abre en una ventana nueva. El valor predeterminado es FALSE.  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |Hipervínculo predeterminado de una forma o de una página.  <br/> |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Indica si el hipervínculo aparece o no en el menú contextual.  <br/> |
   
## <a name="remarks"></a>Comentarios

 Puede agregar tantos hipervínculo.  *nombre* como sea necesario, asignar nombres descriptivos a las filas y establecer valores de celda. Para agregar hipervínculos a una sección de hipervínculos existente, haga clic en una fila y haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet en texto de color rojo. Para asignar un nombre descriptivo para el hipervínculo. *nombre* , haga clic en la fila y, a continuación, escriba un nombre como *Marketing* , por ejemplo, para crear el nombre de fila Hyperlink.Marketing. A continuación, puede hacer referencia a la celda Description usando Hyperlink.Marketing.Description. 
  
El nombre de fila que escriba debe ser único en la sección.
  

