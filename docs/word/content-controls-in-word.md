---
title: Controles de contenido en Word
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- controles de contenido [word], controles de contenido [Word], novedades
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Aprenda cómo los controles de contenido de Microsoft Word 2013 permiten una mayor variedad de escenarios de documentos estructurados.
localization_priority: Priority
ms.openlocfilehash: 4234425cc8398d87b72108d389953fc0eb802c87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358705"
---
# <a name="content-controls-in-word"></a>Controles de contenido en Word

Aprenda cómo los controles de contenido de Microsoft Word 2013 permiten una mayor variedad de escenarios de documentos estructurados.

En este artículo se ofrece información sobre los cambios en los controles de contenido en Microsoft Word 2013 y los escenarios de documentos que dichos cambios permiten.
  
### <a name="structured-documents"></a>Documentos estructurados
<a name="WordCC_StructuredDocs"> </a>

Los documentos estructurados son documentos que controlan dónde puede aparecer el contenido en un documento, el tipo de contenido que puede aparecer en el documento y si dicho contenido se puede editar.
  
Estos son algunos de los escenarios habituales de contenido estructurado en Microsoft Word:
  
- Una asesoría jurídica necesita crear documentos que contienen lenguaje legal que no debería ser modificado por el usuario.
    
- Una empresa necesita crear una portada de propuesta en la que el usuario solo escribe el título, el autor y la fecha.
    
- Una empresa necesita crear facturas en las que los datos del cliente aparezcan en la factura en zonas predefinidas.
    
### <a name="using-content-controls-to-structure-a-document"></a>Uso de controles de contenido para estructurar un documento
<a name="WordCC_StructuredDocs"> </a>

Los controles de contenido son entidades de Microsoft Word que actúan como contenedores de contenido específico en un documento. Los controles de contenido individuales pueden incluir contenido como fechas, listas o párrafos de texto con formato. Estos controles de contenido le permiten crear bloques avanzados y estructurados de contenido, diseñados para su uso en plantillas que insertan bloques bien definidos en sus documentos, creando así documentos estructurados.
  
Los controles de contenido son ideales para crear documentos estructurados porque los controles de contenido le ayudan a fijar la posición de contenido, especificar el tipo de contenido (por ejemplo, una fecha, una imagen o texto), restringir o habilitar la edición, y agregar significado semántico al contenido.
  
### <a name="content-controls-in-word-2010"></a>Controles de contenido en Word 2010
<a name="WordCC_StructuredDocs"> </a>

Los siguientes controles de contenido están disponibles en Word 2010:
  
- Texto enriquecido
    
- Texto sin formato
    
- Imagen
    
- Galería de bloques de creación
    
- Cuadro combinado
    
- Lista desplegable
    
- Fecha
    
- Casilla de verificación
    
- Grupo
    
Los controles de contenido de Word 2010 permiten varias posibles soluciones de documentos estructurados; sin embargo, es en Word 2013 donde los controles de contenido permiten una mayor variedad de escenarios.
  
## <a name="content-control-improvements-in-word-2013"></a>Mejoras a los controles de contenido en Word 2013
<a name="WordCC_WhatsNew"> </a>

En Word 2013, los controles de contenido proporcionan tres mejoras clave: visualización mejorada, compatibilidad con la asignación XML para controles de contenido de texto enriquecido y un nuevo control de contenido para el contenido de repetición.
  
### <a name="improved-visualization"></a>Visualización mejorada

Word 2013 permite que un control de contenido individual aparezca en uno de estos tres estados posibles:
  
- Rectángulo de selección
    
- Etiquetas de inicio o finalización
    
- Ninguno
    
> [!NOTE]
> A menos que se indique lo contrario, en esta sección se explica la visualización de controles de contenido cuando el documento no se está viendo en **Modo Diseño**. El modo de presentación de un control de contenido se establece mediante el control de lista desplegable **Mostrar como** en el cuadro de diálogo **Propiedades del control de contenido**. 
  
**Figura 1. Cuadro de diálogo Propiedades del control de contenido**

![Cuadro de diálogo Propiedades del control de contenido](media/DK2_WordCC_Fig01.jpg "Cuadro de diálogo Propiedades del control de contenido")
  
También puede establecer el modo de presentación de un control de contenido mediante el modelo de objetos de Word 2013 (esto se explica más adelante, en la sección [Nuevos miembros del modelo de objetos de controles de contenido de Word 2013](#WordCC_NewOM)).
  
### <a name="bounding-box"></a>Rectángulo de selección
<a name="WordCC_DefaultRendering"> </a>

La representación predeterminada para los controles de contenido en Word 2013 es conservar el aspecto de los controles de contenido tal como aparecen en Word 2007 y Word 2010: es decir, como un rectángulo de selección. Cuando un control de contenido está establecido para que aparezca como **Rectángulo de selección**, la visualización cambia según la interacción del usuario siguiente:
  
- Cuando el control de contenido no tiene el foco, no se produce ninguna visualización
    
- Al pasar el mouse sobre él, el control de contenido aparece como un rectángulo sombreado
    
**Figura 2. Control de contenido al pasar el mouse sobre él**

![Control de contenido al pasar el mouse sobre él](media/DK2_WordCC_Fig02.jpg "Control de contenido al pasar el mouse sobre él")
  
- Cuando el control de contenido tiene el foco (cuando el usuario elige el control de contenido), el control aparece como un "rectángulo de selección" (con una línea alrededor del contenido y la exhibición de título, si se ha definido un título).
    
**Figura 3. Control de contenido con foco**

![Control de contenido con foco](media/DK2_WordCC_Fig03.jpg "Control de contenido con foco")
  
### <a name="startend-tags"></a>Etiquetas de inicio o finalización
<a name="WordCC_StartEndTags"> </a>

Cuando se establece el control de contenido para que aparezca como **Etiqueta de inicio o finalización**, las etiquetas se muestran con independencia de la interacción del usuario y nunca aparecerá el título; sin embargo, los botones, como el botón **Lista desplegable**, aparecen al pasar el mouse sobre él. 
  
**Figura 4. Control de contenido establecido para aparecer como etiquetas de inicio o finalización**

![Control de contenido establecido para aparecer como etiquetas de inicio o finalización](media/DK2_WordCC_Fig04.jpg "Control de contenido establecido para aparecer como etiquetas de inicio o finalización")
  
### <a name="none"></a>Ninguno
<a name="WordCC_Invisible"> </a>

Cuando se establece el control de contenido para que aparezca como **Ninguno**, no se muestra el control de contenido.
  
### <a name="content-control-colorization"></a>Coloración del control de contenido
<a name="WordCC_CCColorization"> </a>

Además de permitir un tipo diferente de visualización para un control de contenido, Word 2013 también le ayuda a establecer el color de un control de contenido individual. Para configurar el color de un control de contenido, use el botón **Color** del cuadro de diálogo **Propiedades del control de contenido**. 
  
También puede definir el color de un control de contenido mediante el modelo de objetos de Word 2013 (esto se explica más adelante, en la sección [Nuevos miembros del modelo de objetos de controles de contenido de Word 2013](#WordCC_NewOM)).
  
**Figura 5. Cuadro de diálogo Propiedades del control de contenido**

![Cuadro de diálogo Propiedades del control de contenido](media/DK2_WordCC_Fig05.jpg "Cuadro de diálogo Propiedades del control de contenido")
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a>Compatibilidad con la asignación XML para controles de contenido de texto enriquecido
<a name="WordCC_XMLMapping"> </a>

Word 2013 le ayudará a asignar el contenido de los controles de contenido de texto enriquecido y los controles de contenido de los bloques de creación de documentos en el almacén de datos XML. Para ello, debe establecer la *asignación XML* para el control de contenido. Puede establecer esta propiedad usando el método existente **XMLMapping.SetMapping** del modelo de objetos. En el elemento XML personalizado, el XML personalizado se almacena como formato Open XML plano convertido en una cadena (mediante codificación estándar de XML), por lo que se puede almacenar como un nodo de texto en el elemento XML personalizado. Sin embargo, la asignación correcta sigue estando limitada a atributos o nodos de hoja. 
  
> [!NOTE]
> Los controles de contenido de texto enriquecido no pueden contener otros controles de contenido de texto enriquecido. Si uno existe dentro de otro (por ejemplo, debido a una manipulación del formato de archivo, mediante copiar y pegar, etc.), se desvincula hasta que deja de estar contenido dentro de un control de texto enriquecido. 
  
Para obtener más información acerca de cómo configurar la asignación XML, consulte la sección [Nuevos miembros del modelo de objetos de controles de contenido de Word 2013](#WordCC_NewOM) más adelante en este tema. 
  
### <a name="supporting-repeating-content"></a>Compatibilidad con contenido de repetición
<a name="WordCC_SupportingRepeating"> </a>

Además de las mejoras de visualización y el soporte para la asignación XML a los controles de contenido de texto enriquecido, Word 2013 también agrega un nuevo control de contenido que le permite repetir el contenido. El control de contenido para repetición de secciones repite el contenido dentro del mismo, incluidos otros controles de contenido.
  
El control de contenido para repetición de secciones se inserta alrededor de párrafos enteros o de filas de tablas. Una vez que el control rodea una sección, puede insertar copias de la sección encima o debajo de la sección contenida.
  
**Figura 6. Menú contextual del control de contenido para repetición de secciones**

![Menú contextual del control de contenido para repetición de secciones](media/DK2_WordCC_Fig06.jpg "Menú contextual del control de contenido para repetición de secciones")
  
Puede repetir la sección insertada con el control en el extremo del control de contenido (aparece como un botón con el signo más (![Signo más](media/DK2_WordCC_Fig06A.jpg "Signo más"))) o mediante un comando del menú contextual, como se muestra en la figura 6. El contenido repetido pasa a ser una sección independiente del control a la que puede asignar un título a través del cuadro de diálogo **Propiedades del control de contenido**. 
  
**Figura 7. Asignar un título de sección en el cuadro de diálogo Propiedades del control de contenido**

![Cuadro de diálogo Propiedades del control de contenido](media/DK2_WordCC_Fig07.jpg "Cuadro de diálogo Propiedades del control de contenido")
  
Una vez que ha asignado un título a la sección, si selecciona **Permitir a usuarios agregar y quitar secciones** en el cuadro de diálogo **Propiedades del control de contenido**, los usuarios podrán agregar o eliminar la sección por su nombre. 
  
**Figura 8. Usar el menú contextual del control de contenido para repetición de secciones para eliminar una sección**

![Menú contextual del control de contenido para repetición de secciones](media/DK2_WordCC_Fig08.jpg "Menú contextual del control de contenido para repetición de secciones")
  
Cuando un control de contenido para repetición de secciones rodea a otros controles de contenido, los controles de contenido rodeados se repiten en cada nuevo elemento; pero el contenido de dichos controles de contenido se restablece a texto de marcador de posición. Hay dos excepciones en las que se conserva el contenido del control secundario: 
  
- Cuando un control secundario es un control para repetición de secciones.
    
- Cuando un control secundario se asigna mediante XML a un nodo fuera del control de contenido para repetición de secciones.
    
**Figura 9. Control de contenido para repetición de secciones que contiene controles secundarios antes de la repetición**

![Control de contenido para repetición de secciones antes de repetición](media/DK2_WordCC_Fig09.jpg "Control de contenido para repetición de secciones antes de repetición")
  
**Figura 10. Control de contenido para repetición de secciones que contiene controles secundarios después de la repetición**

![Control de contenido para repetición de secciones después de repetición](media/DK2_WordCC_Fig10.jpg "Control de contenido para repetición de secciones después de repetición")
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a>Controles de contenido de para repetición de secciones alrededor de los controles asignados XML
<a name="WordCC_RepeatingSectionCCs"> </a>

Para asignaciones XML que estén contenidas en una sección de repetición, Word 2013 las asigna como se muestra a continuación.
  
Si la asignación no interseca con un elemento del grupo de nodos como parte de su cadena primaria, el enlace es un "enlace absoluto" y muestra el mismo contenido en todos los elementos de sección de repetición.
  
Si la asignación sí interseca con un elemento del grupo de nodos como parte de su cadena primaria, el enlace es un "enlace relativo" y se reasigna de la siguiente manera:
  
- Se determina el enlace absoluto del nodo (reduciendo cualquier expresión de consulta), esto debería suceder en la asignación inicial.
    
- Se quita el eje del enlace que interseca con el grupo de nodos.
    
- El resto de la XPath se evalúa en relación con la XPath del elemento de contenido de la sección de repetición.
    
Por ejemplo, podrían producirse las siguientes asignaciones:
  
- La sección de repetición se asigna a \root\next\path.
    
- El control en el elemento de ejemplo se asigna a \root\next\path[2]\baz.
    
- Word hace coincidir \root\next\path[2] con un elemento del grupo de nodos.
    
Por lo tanto, el enlace se evalúa como .\baz, donde la base es el nodo del elemento de contenido de repetición.
  
Las siguientes sugerencias para trabajar con controles para repetición de contenido pueden ayudar a evitar la pérdida de datos y evitar frustraciones.
  
### <a name="working-with-repeating-section-content-controls-that-are-mapped-to-xml-data"></a>Trabajo con controles de contenido para repetición de secciones que están asignados a datos XML
<a name="WordCC_RepeatingSectionCCs"> </a>

Si inserta un control de contenido para repetición de secciones que está asignado a datos XML, cada vez que el usuario vuelva a abrir el documento, Word recrea los elementos de sección de repetición, según la información del almacén de datos. Incluso si guarda el documento, se perderán los cambios realizados por el usuario en los elementos de sección de repetición del documento que no se hayan asignado también en el almacén de datos.
  
Para impedir que esto ocurra, bloquee el control de contenido para repetición de secciones y permita que el usuario solo pueda modificar los controles de contenido secundarios desbloqueados que también estén asignados al XML.
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a>Enlace de un control de contenido para repetición de secciones a una tabla
<a name="WordCC_RepeatingSectionCCs"> </a>

Si desea enlazar un control de contenido para repetición de secciones a una tabla, inserte la tabla y, *después*, inserte el control de contenido para repetición de secciones, y no al revés. (De lo contrario, no podrá seleccionar solo la tabla). 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a>Anidamiento de controles de contenido para repetición de secciones dentro de una tabla
<a name="WordCC_RepeatingSectionCCs"> </a>

El anidamiento ajustado de controles de contenido para repetición de secciones dentro de una tabla (por ejemplo, cuando el final del control de contenido para repetición de secciones principal y el secundario se encuentran en la misma celda) provoca que la sección de repetición externa se elimine cuando se agregue o se quite algún elemento de la sección interna.
  
Puede evitar que esto ocurra agregando un marcador de párrafo entre el final de un control de contenido para repetición de secciones y el siguiente. Para ocultar el marcador de párrafo, anule la selección de la opción **Mostrar u ocultar** de la ficha **Inicio** en la cinta de opciones. 
  
### <a name="open-xml-file-format-schema-additions"></a>Adiciones al esquema de formato de archivo Open XML
<a name="WordCC"> </a>

Se han agregado los siguientes elementos al esquema de formato de archivo Open XML de WordprocessingML.
  
**Tabla 1. Nuevos elementos en el esquema de formato de archivo Open XML de WordprocessingML para controles de contenido**

|**Elemento**|**Description**|
|:-----|:-----|
|\<w:appearance\>  <br/> |\<w:appearance\> es un elemento secundario de \<w:sdtPr\>.  <br/> Los valores siguientes son válidos para el atributo val:  <br/> \<w:appearance val= boundingBox|etiquetas|se ocultan.  <br/> El valor predeterminado es boundingBox.  <br/> |
|\<w:color\>  <br/> |\<w:color\> es un elemento secundario de \<w:sdtPr\>.  <br/> El modelo de contenido coincide con el tipo complejo CT_Color existente. El valor predeterminado es el color utilizado en Word 2010.  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a>Nuevos miembros del modelo de objetos de controles de contenido de Word 2013
<a name="WordCC_NewOM"> </a>

Con las nuevas mejoras y adiciones en los controles de contenido en Word 2013, se ha actualizado el modelo de objetos de Word para permitir la manipulación del nuevo conjunto de características mediante programación. Además, también se han realizado cambios en el formato de archivo Open XML subyacente para documentos de procesamiento de texto.
  
Las secciones siguientes proporcionan más información acerca de los cambios específicos al modelo de objetos relacionados con cada mejora de los controles de contenido.
  
### <a name="visualization-enhancements"></a>Mejoras de visualización
<a name="WordCC_VisEnhancements"> </a>

Las mejoras de control de contenido de visualización incluyen varias adiciones al modelo de objetos en Word 2013. La siguiente tabla enumera nuevos miembros del objeto **ContentControl** para la visualización. 
  
**Tabla 2. Nuevos miembros del objeto ContentControl**

|**Miembro**|**Description**|
|:-----|:-----|
|. **Appearance** como **WdContentControlAppearance** <br/> |Obtiene o establece la visualización del control de contenido.  <br/> |
|. **Color** como **WdColor** <br/> |Obtiene o establece el color del control de contenido.  <br/> |
   
En la siguiente tabla se muestran las constantes en la nueva enumeración **WdContentControlAppearance**. 
  
**Tabla 3. Nuevas constantes de la enumeración WdContentControlAppearance**

|**Constante**|**Description**|
|:-----|:-----|
|**wdContentControlBoundingBox** <br/> |Representa un control de contenido que se muestra como un cuadro rectangular o un cuadro de selección sombreado (con título opcional).  <br/> |
|**wdContentControlTags** <br/> |Representa un control de contenido que se muestran como marcadores de inicio o finalización.  <br/> |
|**wdContentControlHidden** <br/> |Representa un control de contenido que no se muestra.  <br/> |
   
### <a name="code-sample"></a>Ejemplo de código
<a name="WordCC_VisEnhancements"> </a>

El siguiente ejemplo de código muestra cómo crear controles de contenido de texto enriquecido y establecer la visualización mediante programación.
  
```vb
Sub testVisualization()
   Dim objcc As ContentControl
   Dim objRange As Range
   
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Default Bounding Box"
   ' Set visualization to the default.
   objcc.Appearance = wdContentControlBoundingBox
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(2).Range
   ' Create a rich text content control around the second paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Non Bounding"
   ' Set visualization to invisible.
   objcc.Appearance = wdContentControlHidden
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(3).Range
   ' Create a rich text content control around the third paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Tags Only with Pink color"
   ' Set visualization to Start/End tags with pink color.
   objcc.Appearance = wdContentControlTags
   objcc.Color = wdColorPink
End Sub
```

### <a name="xml-mapping"></a>Asignación XML
<a name="WordCC_XMLMappingOM"> </a>

No se han hecho adiciones al modelo de objetos de Word 2013 para dar cabida a la asignación de texto enriquecido a los nodos XML en el almacén de datos del documento. En su lugar, puede usar el modelo de objetos existente para asignar un control de contenido de texto enriquecido a un nodo XML en el almacén de datos del documento. Tampoco se ha modificado el esquema WordprocessingML de formato de archivo Open XML subyacente como parte de la compatibilidad con el control de contenido de texto enriquecido incluida recientemente, específicamente para la asignación XML.
  
#### <a name="code-sample"></a>Ejemplo de código

El siguiente ejemplo de código muestra cómo asignar un control de contenido de texto enriquecido a un nodo XML mediante programación.
  
```vb
Sub testRichBinding()
   Dim objRange As Range
   Dim objcc As ContentControl
   Dim objCustomPart As CustomXMLPart
   Dim blnMap As Boolean
   
   ' Add a custom XML part to the data store.
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   ' Load XML fragment into the custom XML part.
   objCustomPart.LoadXML ("<x>Rich Text Databinding</x>")
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   ' Bind the XML node to the rich text content control.
   blnMap = objcc.XMLMapping.SetMapping("/x")
   ' Return whether mapping worked.
   MsgBox objcc.XMLMapping.IsMapped
End Sub
```

### <a name="repeating-section-content-controls-represented-in-the-object-model"></a>Controles de contenido para repetición de secciones representados en el modelo de objetos
<a name="WordCC_RepeatingSection"> </a>

El control de contenido para repetición de secciones está disponible en el modelo de objetos mediante las siguientes adiciones al objeto **ContentControl** y los nuevos objetos **RepeatingSectionItem** y **RepeatingSectionItemColl**. En la tabla 4 se enumeran los nuevos miembros más importantes del objeto **ContentControl** para controles de contenido para la repetición de secciones. 
  
**Tabla 4. Miembros del objeto ContentControl**

|**Miembro**|**Description**|
|:-----|:-----|
|**AllowInsertDeleteSection** como **Boolean** <br/> |Obtiene o establece si los usuarios pueden agregar o quitar secciones del control de contenido mediante la interfaz de usuario. Si se llama a esta propiedad para un control de contenido que no es del tipo de sección de repetición, se produce el siguiente error en la llamada: "Esta propiedad solo se puede usar con controles de contenido de sección de repetición".  <br/> |
|**RepeatingSectionItemTitle** como **String** <br/> |Obtiene o establece el nombre de elementos de sección de repetición utilizados en el menú contextual. Si se llama a esta propiedad para un control de contenido que no es del tipo de sección de repetición, se produce el siguiente error en la llamada: "Esta propiedad solo se puede usar con controles de contenido de sección de repetición".  <br/> |
|**InsertRepeatingSectionItemBefore** como **ContentControl** <br/> |Agrega un elemento de sección de repetición antes del elemento actual y devuelve el nuevo elemento de sección de repetición. Si se llama a esta propiedad para un control de contenido que no es del tipo de elemento de sección de repetición, se produce el siguiente error en la llamada: "Esta propiedad solo se puede usar con controles de contenido del elemento de sección de repetición".  <br/> |
|**InsertRepeatingSectionItemAfter** como **ContentControl** <br/> |Agrega un elemento de sección de repetición después del elemento actual y devuelve el nuevo elemento de sección de repetición. Si se llama a esta propiedad para un control de contenido que no es del tipo de elemento de sección de repetición, se produce el siguiente error en la llamada: "Esta propiedad solo se puede usar con controles de contenido del elemento de sección de repetición".  <br/> |
   
En la tabla 5 se muestran los miembros más importantes del objeto **RepeatingSectionItem**. 
  
**Tabla 5. Miembros del objeto RepeatingSectionItem**

|**Miembro**|**Description**|
|:-----|:-----|
|**Range** como **Range** <br/> |Devuelve el intervalo del elemento de sección de repetición especificado, excepto las etiquetas de inicio y finalización.  <br/> |
|**Delete** <br/> |Elimina el elemento de sección de repetición especificado.  <br/> |
|**InsertItemAfter** como **RepeatingSectionItem** <br/> |Agrega un elemento de la sección de repetición después del elemento especificado y devuelve el elemento nuevo.  <br/> |
|**InsertItemBefore** como **RepeatingSectionItem** <br/> |Agrega un elemento de sección de repetición antes del elemento especificado y devuelve el elemento nuevo.  <br/> |
   
En la tabla 6 se muestran los miembros más importantes del objeto **RepeatingSectionItemColl**. 
  
**Tabla 6. Miembros del objeto RepeatingSectionItemColl**

|**Miembro**|**Description**|
|:-----|:-----|
|**Elemento** como **RepeatingSectionItem** <br/> |Devuelve un elemento individual de sección de repetición.  <br/> |
   
La tabla 7 muestra el nuevo miembro de la enumeración **WdContentControlType** para controles de contenido para repetición de secciones. 
  
**Tabla 7. Adición a la enumeración WdContentControlType**

|**Constante**|**Description**|
|:-----|:-----|
|**wdContentControlRepeatingSection** <br/> |Representa un control de contenido que contiene un elemento único en una sección de repetición.  <br/> |
   
### <a name="code-sample"></a>Ejemplo de código
<a name="WordCC_RepeatingSection"> </a>

El siguiente ejemplo de código muestra cómo usar controles de contenido para repetición de secciones mediante programación.
  
```vb
Sub testRepeatingSectionControl()
   Dim objRange As Range
   Dim objTable As Table
   Dim objCustomPart As CustomXMLPart
   Dim objCC As ContentControl
   Dim objCustomNode As CustomXMLNode
   
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   objCustomPart.LoadXML ("<books>" & _
       "<book><title>Everyday Italian</title>" & _
       "<author>Giada De Laurentiis</author></book>" & _
       "<book><title>Harry Potter</title>" & _
       "<author>J K. Rowling</author></book>" & _
       "<book><title>Learning XML</title>" & _
       "<author>Erik T. Ray</author></book></books>")
   
   Set objRange = ActiveDocument.Paragraphs(1).Range
   Set objTable = ActiveDocument.Tables.Add(objRange, 2, 2)
   With objTable.Borders
       .InsideLineStyle = wdLineStyleSingle
       .OutsideLineStyle = wdLineStyleDouble
   End With
   Set objRange = objTable.Cell(1, 1).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/title[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Cell(1, 2).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/author[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Rows(1).Range
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlRepeatingSection, objRange)
   objCC.XMLMapping.SetMapping ("/books[1]/book")
End Sub
```

### <a name="open-xml-file-format-changes-for-repeating-section-content-controls"></a>Cambios al formato de archivo Open XML para controles de contenido para repetición de secciones
<a name="WordCC_RepeatingSection"> </a>

La representación del formato de archivo de un control de contenido para repetición de secciones generalmente usa los mismos nombres de elemento, los valores, etc., que el formato XML existente; sin embargo, el elemento \<sdt\> que representa el contenedor de sección de repetición exterior existe en el espacio de nombres de Word 2013, para garantizar la compatibilidad con versiones anteriores de Word.
  
Los elementos individuales de repetición dentro del control de contenido para repetición de secciones (que rodean a cada elemento individual) se guardan como controles de contenido de texto enriquecido con la representación de WordprocessingML existente. En la tabla 8 se enumeran los elementos nuevos en el esquema WordprocessingML para controles de contenido para repetición de secciones.
  
**Tabla 8. Elementos nuevos en el esquema WordprocessingML para controles de contenido para repetición de secciones**

|**Elemento**|**Description**|
|:-----|:-----|
|\<w15:repeatingSection\>  <br/> |Especifica un control de contenido para repetición de secciones. Este elemento es mutuamente exclusivo con todos los demás tipos de controles y no tiene elementos secundarios ni atributos.  <br/> |
|\<w15:repeatingSectionItem\>  <br/> |Especifica un control de contenido de elemento de sección de repetición. Este elemento es mutuamente exclusivo con todos los demás tipos de controles y no tiene elementos secundarios ni atributos.  <br/> |
|\<w15:doNotAllowInsertDeleteSection\>  <br/> |Especifica que el usuario no puede agregar ni eliminar secciones mediante la interfaz de usuario en Word 2013.  <br/> |
|\<w15:sectionTitle\>  <br/> |Especifica el nombre de los elementos de sección de repetición (y se usa en el menú contextual cuando se elige el control).  <br/> |
   

  

