---
title: Controles de contenido en Word
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- controles de contenido [word], los controles de contenido [Word], novedades
localization_priority: Normal
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Obtenga información sobre cómo los controles de contenido de Microsoft Word 2013 habilitan una mayor variedad de escenarios de documentos estructurados.
ms.openlocfilehash: 1b0b88da4bc3347ac6748ab57b99d45edd57558d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823646"
---
# <a name="content-controls-in-word"></a>Controles de contenido en Word

Obtenga información sobre cómo los controles de contenido de Microsoft Word 2013 habilitan una mayor variedad de escenarios de documentos estructurados.

En este tema se proporciona información acerca de los cambios realizados en los controles de contenido en Microsoft Word 2013 y los escenarios de documentos que permiten a esos cambios.
  
### <a name="structured-documents"></a>Documentos estructurados
<a name="WordCC_StructuredDocs"> </a>

Los documentos estructurados son documentos que controlan donde puede aparecer el contenido en un documento, el tipo de contenido que puede aparecer en el documento y si dicho contenido se puede editar.
  
A continuación presentamos algunos escenarios comunes para contenido estructurado en Microsoft Word:
  
- Una asesoría jurídica necesita crear documentos que contienen lenguaje legal que no debería ser modificado por el usuario.
    
- Una empresa necesita crear una portada de propuesta en la que el usuario solo escribe el título, el autor y la fecha.
    
- Una empresa necesita crear facturas en las que los datos del cliente aparezcan en la factura en zonas predefinidas.
    
### <a name="using-content-controls-to-structure-a-document"></a>Uso de controles de contenido para estructurar un documento
<a name="WordCC_StructuredDocs"> </a>

Controles de contenido son entidades de Microsoft Word que actúan como contenedores de contenido específico en un documento. Los controles de contenido individuales pueden incluir elementos como fechas, listas o párrafos de texto con formato. Controles de contenido de ayuda crear enriquecido, bloques de contenido estructurados y están diseñados para su uso en las plantillas que insertan bloques perfectamente definidos en los documentos, creación de documentos estructurados.
  
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
    
Controles de contenido de Word 2010 habilitar diversas soluciones de documentos estructurados posibles, pero en Word 2013 controles de contenido permiten una mayor variedad de escenarios.
  
## <a name="content-control-improvements-in-word-2013"></a>Mejoras de control de contenido en Word 2013
<a name="WordCC_WhatsNew"> </a>

En Word 2013, los controles de contenido proporcionan tres mejoras claves: mejorado de la visualización, soporte técnico para la asignación de XML para los controles de contenido de texto Rich y un nuevo control de contenido para contenido repetido.
  
### <a name="improved-visualization"></a>Visualización mejorada

Word 2013 permite que un control de contenido individual que aparezca en uno de tres estados posibles:
  
- Rectángulo de selección
    
- Etiquetas de inicio o finalización
    
- Ninguno
    
> [!NOTE]
> Si no se indique lo contrario, en esta sección se describe la visualización de los controles de contenido cuando el documento no se ve en **Modo de diseño**. Establecer el modo de presentación para un control de contenido mediante el control de lista desplegable **se muestran como** en el cuadro de diálogo **Propiedades del Control de contenido** . 
  
**En la figura 1. Cuadro de diálogo de propiedades de Control de contenido**

![Cuadro de diálogo de propiedades de control de contenido] (media/DK2_WordCC_Fig01.jpg "Cuadro de diálogo de propiedades de control de contenido")
  
También puede establecer el modo de presentación para un control de contenido mediante el modelo de objetos de Word 2013 (Esto se describe más adelante en [miembros del modelo de objeto de control de contenido de nuevo Word 2013](#WordCC_NewOM)).
  
### <a name="bounding-box"></a>Rectángulo de selección
<a name="WordCC_DefaultRendering"> </a>

La representación predeterminada para los controles de contenido en Word 2013 es conservar el aspecto de los controles de contenido, tal como aparecen en Word 2007 y Word 2010; es decir, como un cuadro de límite. Cuando un control de contenido está configurado para mostrar como **Cuadro de límite**, la visualización cambia según la interacción del usuario siguientes:
  
- Cuando el control de contenido no tiene el foco, no se produce ninguna visualización.
    
- Al pasar el mouse sobre él, el control de contenido aparece como un rectángulo sombreado.
    
**La figura 2. Control de contenido al pasar el mouse**

![Control en el mouse (ratón) de contenido a través de] (media/DK2_WordCC_Fig02.jpg "Control en el mouse (ratón) de contenido a través de")
  
- Cuando el control de contenido tiene el foco (cuando el usuario elige el control de contenido), el control aparece como un "rectángulo de selección" (con una línea alrededor del contenido y la exhibición de título, si se ha definido un título).
    
**La figura 3. Control de contenido con foco**

![Control con el foco de contenido] (media/DK2_WordCC_Fig03.jpg "Control con el foco de contenido")
  
### <a name="startend-tags"></a>Etiquetas de inicio o finalización
<a name="WordCC_StartEndTags"> </a>

Cuando el control de contenido está configurado para mostrar como **etiqueta de inicio y finalización**, se muestran las etiquetas independientemente de la interacción del usuario, y el título no aparecerá nunca; pero los botones, como el botón de **Lista desplegable** , aparecen en el mouse (ratón) a través de. 
  
**La figura 4. Control de contenido configurado para mostrar como etiquetas de inicio y finalización**

![Control de contenido configurado para mostrar como de inicio y finalización de las etiquetas] (media/DK2_WordCC_Fig04.jpg "Control de contenido configurado para mostrar como de inicio y finalización de las etiquetas")
  
### <a name="none"></a>None
<a name="WordCC_Invisible"> </a>

Cuando el control de contenido está configurado para mostrar como **Ninguno**, no se muestra el control de contenido.
  
### <a name="content-control-colorization"></a>Coloración del control de contenido
<a name="WordCC_CCColorization"> </a>

Además de habilitar a un tipo de presentación para un control de contenido diferente, Word 2013 también le ayuda a establecer el color de un control de contenido individual. Establecer el color de un control de contenido mediante el botón de **Color** en el cuadro de diálogo **Propiedades del Control de contenido** . 
  
También puede establecer el color de un control de contenido mediante el modelo de objetos de Word 2013 (Esto se describe más adelante en [miembros del modelo de objeto de control de contenido de nuevo Word 2013](#WordCC_NewOM)).
  
**La figura 5. Cuadro de diálogo de propiedades de Control de contenido**

![Cuadro de diálogo de propiedades de control de contenido] (media/DK2_WordCC_Fig05.jpg "Cuadro de diálogo de propiedades de control de contenido")
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a>Compatibilidad con la asignación XML para controles de contenido de texto enriquecido
<a name="WordCC_XMLMapping"> </a>

Word 2013 le ayuda a asignar el contenido de los controles de contenido de texto enriquecido y controles de contenido de bloque de creación de documentos en el almacén de datos XML. Para ello, se establece la *asignación XML* para el control de contenido. Puede establecer esta propiedad mediante el método **XMLMapping.SetMapping** existente en el modelo de objetos. En el fragmento XML personalizado, el código XML personalizado se almacena como marcado de Open XML plano convertido en una cadena (mediante el uso de codificación XML estándar), por lo que se puede almacenar como un nodo de texto en el fragmento XML personalizado. Sin embargo, la asignación sigue teniendo la limitación que puede asignar solo correctamente para atributos o nodos de hoja. 
  
> [!NOTE]
> Los controles de contenido de texto enriquecido no pueden contener otros controles de contenido de texto enriquecido. Si uno existe dentro de otro (por ejemplo, debido a una manipulación del formato de archivo, mediante copiar y pegar, etc.), se desvincula hasta que deja de estar contenido dentro de un control de texto enriquecido. 
  
Para obtener más información acerca de cómo configurar la asignación de XML, vea la sección [miembros del modelo de objeto de control de contenido de nuevo Word 2013](#WordCC_NewOM) más adelante en este tema. 
  
### <a name="supporting-repeating-content"></a>Compatibilidad con contenido de repetición
<a name="WordCC_SupportingRepeating"> </a>

Además de las mejoras de visualización y soporte técnico para la asignación de XML a los controles de contenido de texto enriquecido, Word 2013 también agrega un nuevo control de contenido que permite a repetir el contenido. El control de contenido de sección de repetición repite el contenido dentro del mismo, incluidos otros controles de contenido.
  
El control de contenido para repetición de secciones se inserta alrededor de párrafos enteros o de filas de tablas. Una vez que el control rodea una sección, puede insertar copias de la sección encima o debajo de la sección contenida.
  
**La figura 6. Menú contextual de control de contenido de sección de repetición**

![Contexto de control de contenido de sección de repetición] (media/DK2_WordCC_Fig06.jpg "Contexto de control de contenido de sección de repetición")
  
Puede repetir la sección insertada mediante el control en el extremo del control de contenido (que se muestra como un botón con un![signo más]((media/DK2_WordCC_Fig06A.jpg "signo más")) de signo más) o eligiendo un comando en el menú contextual, como se muestra en la figura 6. El contenido repetido se convierte en una sección independiente del control que puede asignar un título mediante el cuadro de diálogo **Propiedades del Control de contenido** . 
  
**La figura 7. Asignar un título de sección en el cuadro de diálogo Propiedades del Control de contenido**

![Cuadro de diálogo de propiedades de control de contenido] (media/DK2_WordCC_Fig07.jpg "Cuadro de diálogo de propiedades de control de contenido")
  
Una vez que se ha concedido a la sección un título, si selecciona **Permitir a los usuarios para agregar y quitar secciones** en el cuadro de diálogo **Propiedades del Control de contenido** , los usuarios pueden agregar o eliminar la sección por su nombre. 
  
**La figura 8. Use el menú de contexto de control de contenido de sección extensible para eliminar una sección**

![Contexto de control de contenido de sección de repetición] (media/DK2_WordCC_Fig08.jpg "Contexto de control de contenido de sección de repetición")
  
Cuando un control de contenido para repetición de secciones rodea a otros controles de contenido, los controles de contenido rodeados se repiten en cada nuevo elemento; pero el contenido de dichos controles de contenido se restablece a texto de marcador de posición. Hay dos excepciones en las que se conserva el contenido del control secundario: 
  
- Cuando un control secundario es un control para repetición de secciones.
    
- Cuando un control secundario se asigna mediante XML a un nodo fuera del control de contenido para repetición de secciones.
    
**En la figura 9. Control de contenido de la sección que contiene los controles secundarios antes de la repetición de repetición**

![Repita el control de contenido antes de repetición] (media/DK2_WordCC_Fig09.jpg "Repita el control de contenido antes de repetición")
  
**La figura 10. Control de contenido de la sección que contiene los controles secundarios después de la repetición de repetición**

![Repita el control de contenido de sección después de repetición] (media/DK2_WordCC_Fig10.jpg "Repita el control de contenido de sección después de repetición")
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a>Controles de contenido de para repetición de secciones alrededor de los controles asignados XML
<a name="WordCC_RepeatingSectionCCs"> </a>

Para asignaciones XML que están contenidas en una sección de repetición, Word 2013 asignan como se indica a continuación.
  
Si la asignación no se cruzan con un elemento en el nodo establecido como parte de su cadena de principales, el enlace es un "enlace absoluto" y muestra el mismo contenido en todos los elementos de sección de repetición.
  
Si la asignación forma una intersección con un elemento en el nodo establecido como parte de su cadena de principales, el enlace es un "enlace relativo" y se reasignan como sigue:
  
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

Si inserta un control de contenido de sección extensible que se asigna a los datos XML, cada vez que el usuario vuelve a abrir el documento, Word vuelve a crear los elementos de sección de repetición, basándose en la información en el almacén de datos. Incluso si se guarda el documento, se pierden todos los cambios que realiza el usuario en los elementos de sección extensible en el documento que no se asignan también en el almacén de datos.
  
Para impedir que esto ocurra, bloquee el control de contenido para repetición de secciones y permita que el usuario solo pueda modificar los controles de contenido secundarios desbloqueados que también estén asignados al XML.
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a>Enlace de un control de contenido para repetición de secciones a una tabla
<a name="WordCC_RepeatingSectionCCs"> </a>

Si desea enlazar un control de contenido de sección extensibles a una tabla, insertar en la tabla y *, a continuación,* el control de contenido insertar repetición sección y no al revés. (De lo contrario, no podrá seleccionar sólo la tabla). 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a>Anidamiento de controles de contenido para repetición de secciones dentro de una tabla
<a name="WordCC_RepeatingSectionCCs"> </a>

El anidamiento ajustado de controles de contenido para repetición de secciones dentro de una tabla (por ejemplo, cuando el final del control de contenido para repetición de secciones principal y el secundario se encuentran en la misma celda) provoca que la sección de repetición externa se elimine cuando se agregue o se quite algún elemento de la sección interna.
  
Puede evitar que esto ocurra mediante la adición de un marcador de párrafo entre el final de un control de contenido de sección extensible y el siguiente. Para ocultar el marcador de párrafo, anule la selección de la opción **Mostrar u ocultar** de la ficha **Inicio** de la cinta de opciones. 
  
### <a name="open-xml-file-format-schema-additions"></a>Adiciones al esquema de formato de archivo Open XML
<a name="WordCC"> </a>

Se han agregado los siguientes elementos al esquema de formato de archivo Open XML de WordprocessingML.
  
**La tabla 1. Nuevos elementos en el esquema de formato de archivo XML abierto de WordprocessingML para los controles de contenido**

|**Element**|**Descripción**|
|:-----|:-----|
|\<w:Appearance\>  <br/> |\<w:Appearance\> es un elemento secundario de \<w:sdtPr\>.  <br/> Los valores siguientes son válidos para el atributo val:  <br/> \<w:Appearance val = boundingBox|de cierre|oculto.  <br/> El valor predeterminado es boundingBox.  <br/> |
|\<w:color\>  <br/> |\<w:color\> es un elemento secundario de \<w:sdtPr\>.  <br/> El modelo de contenido coincide con el tipo complejo CT_Color existente. El valor predeterminado es el color utilizado en Word 2010.  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a>Nuevos miembros de modelo de objeto de control de contenido de Word 2013
<a name="WordCC_NewOM"> </a>

Con las nuevas mejoras y adiciones a controles de contenido en Word 2013, se actualizó el modelo de objetos de Word para permitir la manipulación mediante programación del nuevo conjunto de características. Además, también se efectuaron cambios en el formato de archivo XML abierto subyacente para documentos de procesamiento.
  
Las secciones siguientes proporcionan más información acerca de los cambios específicos al modelo de objetos relacionados con cada mejora de los controles de contenido.
  
### <a name="visualization-enhancements"></a>Mejoras de visualización
<a name="WordCC_VisEnhancements"> </a>

Varias adiciones al modelo de objetos se incluyen en Word 2013 para mejoras de visualización de control de contenido. En la siguiente tabla se enumeran nuevos miembros del objeto **ContentControl** para la visualización. 
  
**Tabla 2. Nuevos miembros de objeto ContentControl**

|**Elemento**|**Descripción**|
|:-----|:-----|
|. **Apariencia** como **WdContentControlAppearance** <br/> |Obtiene o establece la visualización del control de contenido.  <br/> |
|. **Color** como **WdColor** <br/> |Obtiene o establece el color del control de contenido.  <br/> |
   
En la siguiente tabla se enumera las constantes en la enumeración **WdContentControlAppearance** nuevo. 
  
**Tabla 3. Nuevas constantes de WdContentControlAppearance (enumeración)**

|**Constante**|**Descripción**|
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

Se han realizado ningún adiciones al modelo de objetos de Word 2013 para dar cabida a la asignación de texto enriquecido a los nodos XML en el almacén de datos del documento. En su lugar, use el modelo de objetos existente para asignar un control de contenido de texto enriquecido a un nodo XML en el almacén de datos del documento. Además, no se realizaron cambios en el esquema WordprocessingML de formato de archivo Open XML subyacente como parte de la compatibilidad de control de contenido de texto enriquecido recién incluido específicamente para una asignación XML.
  
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

El control de contenido de sección de repetición está disponible en el modelo de objetos mediante el uso de las siguientes adiciones al objeto **ContentControl** y los nuevos objetos **RepeatingSectionItem** y **RepeatingSectionItemColl** . Tabla 4 se enumeran a los nuevos miembros más importantes del objeto **ContentControl** para controles de contenido de la sección de repetición. 
  
**Tabla 4. Miembros del objeto ContentControl**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**AllowInsertDeleteSection** como **Boolean** <br/> |Obtiene o establece si los usuarios pueden agregar o quitar secciones desde el control de contenido mediante el uso de la interfaz de usuario. Si se llama a esta propiedad para un control de contenido que no es del tipo de sección de repetición, se produce un error en la llamada con el siguiente mensaje de error: "esta propiedad sólo se puede usar con controles de contenido de la sección de repetición."  <br/> |
|**RepeatingSectionItemTitle** como **cadena.** <br/> |Obtiene o establece el nombre de elementos usados en el menú contextual de la sección de repetición. Si se llama a esta propiedad para un control de contenido que no es del tipo de sección de repetición, se produce un error en la llamada con: "esta propiedad sólo se puede usar con controles de contenido de la sección de repetición."  <br/> |
|**InsertRepeatingSectionItemBefore** como **ContentControl** <br/> |Agrega un elemento de sección de repetición antes del elemento actual y devuelve el nuevo elemento de sección de repetición. Si se llama a este método para un control de contenido que no es del tipo de elemento de la sección de repetición, se produce un error en la llamada con: "esta propiedad sólo se puede usar con controles de contenido de elemento de sección de repetición."  <br/> |
|**InsertRepeatingSectionItemAfter** como **ContentControl** <br/> |Agrega un elemento de sección de repetición después del elemento actual y devuelve el nuevo elemento de sección de repetición. Si se llama a este método para un control de contenido que no es del tipo de elemento de la sección de repetición, se produce un error en la llamada con: "esta propiedad sólo se puede usar con controles de contenido de elemento de sección de repetición."  <br/> |
   
En la tabla 5 se enumeran a los miembros más importantes del objeto **RepeatingSectionItem** . 
  
**Tabla 5. Miembros del objeto RepeatingSectionItem**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**Intervalo** como **intervalo** <br/> |Devuelve el intervalo del elemento de sección extensible especificado, excluyendo las etiquetas de inicio y finalización.  <br/> |
|**Delete** <br/> |Elimina el elemento de sección de repetición especificado.  <br/> |
|**InsertItemAfter** como **RepeatingSectionItem** <br/> |Agrega un elemento de la sección de repetición después del elemento especificado y devuelve el elemento nuevo.  <br/> |
|**InsertItemBefore** como **RepeatingSectionItem** <br/> |Agrega un elemento de la sección de repetición antes del elemento especificado y devuelve el elemento nuevo.  <br/> |
   
Tabla 6 se enumeran a los miembros más importantes del objeto **RepeatingSectionItemColl** . 
  
**Tabla 6. Miembros del objeto RepeatingSectionItemColl**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**Elemento** como **RepeatingSectionItem** <br/> |Devuelve un elemento individual de sección de repetición.  <br/> |
   
La tabla 7 muestra al nuevo miembro de la enumeración **WdContentControlType** para controles de contenido de la sección de repetición. 
  
**Tabla 7. Adición de WdContentControlType (enumeración)**

|**Constante**|**Descripción**|
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

La representación del formato de archivo de un control de contenido de sección extensible generalmente usa los mismos nombres de elemento, los valores, y así sucesivamente, como el marcado XML existente; Sin embargo, el \<sdt\> elemento que representa el contenedor de sección de repetición exterior existe en el espacio de nombres de Word 2013, para garantizar la compatibilidad con versiones anteriores de Word.
  
Los elementos individuales de repetición dentro del control de contenido para repetición de secciones (que rodean a cada elemento individual) se guardan como controles de contenido de texto enriquecido con la representación de WordprocessingML existente. En la tabla 8 se enumeran los elementos nuevos en el esquema WordprocessingML para controles de contenido para repetición de secciones.
  
**La tabla 8. Controles de contenido de nuevos elementos en el esquema WordprocessingML de sección de repetición**

|**Element**|**Descripción**|
|:-----|:-----|
|\<w15:repeatingSection\>  <br/> |Especifica un control de contenido para repetición de secciones. Este elemento es mutuamente exclusivo con todos los demás tipos de controles y no tiene elementos secundarios ni atributos.  <br/> |
|\<w15:repeatingSectionItem\>  <br/> |Especifica un control de contenido de elemento de sección de repetición. Este elemento es mutuamente exclusivo con todos los demás tipos de controles y no tiene elementos secundarios ni atributos.  <br/> |
|\<w15:doNotAllowInsertDeleteSection\>  <br/> |Especifica que el usuario no puede agregar o eliminar secciones mediante la interfaz de usuario en Word 2013.  <br/> |
|\<w15:sectionTitle\>  <br/> |Especifica el nombre de los elementos de la sección de repetición (y se usa en el menú contextual cuando se elige el control).  <br/> |
   

  

