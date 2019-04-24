---
title: Hoja de cálculo ShapeSheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251822
localization_priority: Normal
ms.assetid: f403890d-4a3a-bacc-53d7-1b9920b23639
description: Cada uno de los objetos de Microsoft Visio (documentos, páginas, estilos, formas, grupos, formas u objetos de un grupo, patrones, objetos de otros programas, guías y puntos de guía) tiene una hoja de cálculo ShapeSheet asociada en la que se almacena información acerca del objeto. Esta hoja de cálculo contiene información tal como el alto, ancho, ángulo, color y otros atributos que determinan la apariencia y el comportamiento de la forma.
ms.openlocfilehash: 37b2ae10b1f511197af5ccf739de91edb74e7819
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345188"
---
# <a name="about-the-shapesheet-spreadsheet"></a>Hoja de cálculo ShapeSheet

Cada uno de los objetos de Microsoft Visio (documentos, páginas, estilos, formas, grupos, formas u objetos de un grupo, patrones, objetos de otros programas, guías y puntos de guía) tiene una hoja de cálculo ShapeSheet asociada en la que se almacena información acerca del objeto. Esta hoja de cálculo contiene información tal como el alto, ancho, ángulo, color y otros atributos que determinan la apariencia y el comportamiento de la forma.
  
Como desarrollador de formas, deberá mantener un control preciso de la apariencia y el comportamiento de las formas que cree. Puede cambiar el comportamiento predeterminado de una forma y mejorar su capacidad si la modifica en su ShapeSheet, a la que se tiene acceso en una ventana ShapeSheet o mediante programación.
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a>Ver un objeto en una ventana ShapeSheet

La ventana de dibujo y la ventana ShapeSheet de Visio son simplemente vistas diferentes de la misma forma.
  
- Al ver una forma en la ventana de dibujo, aparecerá gráficamente y su comportamiento se ajustará a las fórmulas de ShapeSheet.
    
- Al ver una forma en la ventana ShapeSheet, podrá ver las fórmulas subyacentes que determinan su apariencia y comportamiento en la página de dibujo.
    
Puede visualizar simultáneamente la ventana ShapeSheet y la ventana de dibujo para ver cómo cambia la forma en la segunda cuando se modifican las celdas de la primera, o viceversa. Por ejemplo, al mover la forma con el puntero, las fórmulas PinX y PinY de la sección Shape Transform cambian para reflejar la nueva posición en la página de dibujo.
  
## <a name="structure-of-the-shapesheet-window"></a>Estructura de la ventana ShapeSheet.

Una hoja de cálculo ShapeSheet se divide en *secciones* que controlan un aspecto concreto del comportamiento o la apariencia de una forma, por ejemplo, su geometría o su formato. Cada sección contiene una o varias *filas* que contienen *celdas* . Cada celda puede contener una fórmula, su resultado (normalmente denominado valor de la celda) e información opcional de error. Una fórmula puede ser requerida u opcional dependiendo de la celda de que se trate. Los datos de una celda (por ejemplo, su fórmula o valor) pueden estar definidos localmente o, con más frecuencia, se heredan de la celda equivalente del patrón o estilo de la forma. 
  
El siguiente ejemplo muestra la barra de fórmulas ![barra de fórmulas](media/callout1_ZA01036259.gif), una sección ![section](media/callout2_ZA01036260.gif), una celda ![móviles](media/callout3_ZA01036261.gif)y una fila ![row](media/callout4_ZA01036262.gif) en la ventana ShapeSheet. 
  
![Ventana ShapeSheet](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
Al dibujar una forma, Visio la registra como una colección de ubicaciones horizontales y verticales conectadas por segmentos. Estas ubicaciones (llamadas vértices) se registran en las celdas X e y de la sección de **geometría** de la forma. Como se muestra en el siguiente ejemplo, cuando hace clic en las celdas X e y en la sección **geometría** de la ventana ShapeSheet de una forma, verá un cuadro con borde negro que resalta el vértice de la forma en la ventana de dibujo. 
  
![Cuadro con borde negro que resalta el vértice de la forma en la ventana de dibujo.](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a>Editar un objeto en la ventana ShapeSheet

Cuando hay una ventana ShapeSheet activa, la cinta cambia para mostrar opciones específicas para trabajar en esa ventana. Al seleccionar una celda de ShapeSheet, aparece una barra de fórmulas que puede usar para especificar y modificar las fórmulas de un objeto. También puede escribir directamente en la celda.
  
En la ventana ShapeSheet puede agregar secciones a la hoja de cálculo de una forma para agregarle nuevas características en la página de dibujo. Por ejemplo, puede Agregar una sección de **puntos de conexión** para crear una conexión. Si ya no necesita una sección, puede eliminarla. 
  
También puede agregar filas a las secciones para albergar fórmulas adicionales o cambiar la apariencia de una forma. Por ejemplo, puede Agregar una fila a una sección de **geometría** para agregar un segmento a una forma. Igualmente, puede eliminar las filas que ya no necesite. 
  
En las celdas pueden mostrarse fórmulas o valores. Muestre las fórmulas cuando especifique fórmulas nuevas, cuando modifique las existentes o cuando desee ver cómo se relacionan entre sí las fórmulas de las distintas celdas. Un valor es el resultado que se obtiene cuando Visio evalúa la fórmula de una celda. Puede mostrar los valores de las celdas para ver el resultado de la evaluación.
  
## <a name="additional-shapesheet-references"></a>Más material de referencia sobre ShapeSheet

Para obtener información detallada sobre una sección, fila o celda en particular en la ShapeSheet, vea el artículo correspondiente en esta [referencia de ShapeSheet](reference-visio-shapesheet.md).
  
Si desea información detallada acerca del acceso por programa a la hoja de cálculo ShapeSheet, vea la Referencia de automatización de Microsoft Visio.
  

