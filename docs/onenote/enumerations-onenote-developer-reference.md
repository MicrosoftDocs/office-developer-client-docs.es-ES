---
title: Enumeraciones (referencia para desarrolladores de OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: En este tema se describen las enumeraciones del modelo de objetos de OneNote 2013.
ms.openlocfilehash: 3338e444e5b0bfd0239e363c3161aeb1914b2d53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410339"
---
# <a name="enumerations-onenote-developer-reference"></a>Enumeraciones (referencia para desarrolladores de OneNote)

En este tema se describen las enumeraciones del modelo de objetos de OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Cuando se pasa al método **OpenHierarchy** , especifica el tipo de objeto que se va a crear, si lo hay, si la ruta de acceso que se ha pasado al método todavía no existe. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**cftNone** <br/> |comprendi  <br/> |No crea ningún objeto nuevo.  <br/> |
|**cftNotebook** <br/> |1  <br/> |Crea un bloc de notas utilizando el nombre y la ubicación especificados.  <br/> |
|**cftFolder** <br/> |segundo  <br/> |Crea un grupo de secciones mediante el nombre y la ubicación especificados.  <br/> |
|**cftSection** <br/> |3  <br/> |Crea una sección con el nombre y la ubicación especificados.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indica la ubicación acoplada de una ventana de 2013 de OneNote mediante la interfaz de [ventana](window-interfaces-onenote.md) . Cuando se establece en la propiedad **DockedLocation** , especifica la ubicación en la que se va a acoplar una ventana de OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |La ventana de OneNote se acopla en la ubicación predeterminada del escritorio.  <br/> |
|**dlLeft** <br/> |1  <br/> |La ventana de OneNote se acopla en el lado izquierdo del escritorio.  <br/> |
|**dlRight** <br/> |segundo  <br/> |La ventana de OneNote se acopla en el lado derecho del escritorio.  <br/> |
|**dlTop** <br/> |3  <br/> |La ventana de OneNote se acopla en la parte superior del escritorio.  <br/> |
|**dlBottom** <br/> |4   <br/> |La ventana de OneNote se acopla en la parte inferior del escritorio.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Cuando se pasa al método **SetFilingLocation** , especifica el tipo de contenido en el que se establece la ubicación de archivado cuando se envía el tipo de contenido a OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**flEMail** <br/> |comprendi  <br/> |Establece dónde se archivarán los mensajes de correo electrónico de Outlook.  <br/> |
|**flContacts** <br/> |1  <br/> |Establece dónde se archivarán los contactos de Outlook.  <br/> |
|**flTasks** <br/> |segundo  <br/> |Establece dónde se archivarán las tareas de Outlook.  <br/> |
|**flMeetings** <br/> |3  <br/> |Establece dónde se archivarán las reuniones de Outlook.  <br/> |
|**flWebContent** <br/> |4   <br/> |Establece el lugar en el que se archivará el contenido de Internet Explorer.  <br/> |
|**flPrintOuts** <br/> |5   <br/> |Establece dónde se archivarán las copias impresas de la impresora de OneNote.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Cuando se pasa al método **SetFilingLocation** , especifica dónde se archiva el contenido que se envía a OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |comprendi  <br/> |Establece el contenido que se va a archivar en una página nueva de una sección especificada.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Establece el contenido que se va a archivar en una página nueva de la sección actual.  <br/> |
|**fltCurrentPage** <br/> |segundo  <br/> |Establece el contenido que se archivará en la página actual.  <br/> |
|**fltNamedPage** <br/> |4   <br/> |Establece el contenido que se va a archivar en una página especificada.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Cuando se asigna a la propiedad **TreeDepth** de la interfaz [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md) , especifica la profundidad del árbol de OneNote que se mostrará cuando se represente el cuadro de diálogo de archivado rápido. Cuando se pasa al método **AddButton** del objeto **IQuickFilingDialog** , hace referencia a ciertos elementos de la jerarquía de OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**heNone** <br/> |comprendi  <br/> |Hace referencia a ningún elemento.  <br/> |
|**heNotebooks** <br/> |1  <br/> |Hace referencia a los elementos del Bloc de notas.  <br/> |
|**heSectionGroups** <br/> |segundo  <br/> |Hace referencia a los elementos del grupo de secciones.  <br/> |
|**heSections** <br/> |4   <br/> |Hace referencia a los elementos de la sección.  <br/> |
|**hePages** <br/> |8   <br/> |Hace referencia a los elementos de la página.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **GetHierarchy** , especifica el nivel más bajo para obtener en la jerarquía de nodos del Bloc de notas. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |comprendi  <br/> |Obtiene solo el nodo de inicio especificado y ningún descendiente.  <br/> |
|**hsChildren** <br/> |1  <br/> |Obtiene los nodos secundarios inmediatos del nodo de inicio y no tiene descendientes en grupos de subsecciones superiores o inferiores.  <br/> |
|**hsNotebooks** <br/> |segundo  <br/> |Obtiene todos los blocs de notas por debajo del nodo de inicio o raíz.  <br/> |
|**hsSections** <br/> |3  <br/> |Obtiene todas las secciones debajo del nodo de inicio, incluidas las secciones en grupos de secciones y subsecciones.  <br/> |
|**hsPages** <br/> |4   <br/> |Obtiene todas las páginas bajo el nodo de inicio, incluidas todas las páginas de los grupos de secciones y subsecciones.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **CreateNewPage** , especifica el estilo de la nueva página. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |comprendi  <br/> |Crea una página que tiene el estilo de página predeterminado.  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Crea una página en blanco con un título.  <br/> |
|**npsBlankPageNoTitle** <br/> |segundo  <br/> |Crea una página en blanco sin título.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **NotebookFilterOut** del objeto **QFD** , especifica los blocs de notas que se mostrarán cuando se represente el cuadro de QFD. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Permitir solo blocs de notas locales.  <br/> |
|**nfoNetwork** <br/> |segundo  <br/> |Permite los blocs de notas UNC o SharePoint.  <br/> |
|**nfoWeb** <br/> |4   <br/> |Permite los blocs de notas de OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8   <br/> |Cualquier Bloc de notas en ubicaciones que no tienen un cliente web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (actualizado para OneNote 2013)
<a name="odc_PageInfo"> </a>

Cuando se pasa al método **GetPageContent** , especifica el tipo de información que se va a devolver con el contenido de la página. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**piBasic** <br/> |comprendi  <br/> |Devuelve sólo el contenido de la página básica, sin marcado de selección, los tipos de archivo de los objetos de datos binarios y los objetos de datos binarios. Este es el valor estándar que se va a pasar.  <br/> |
|**piBinaryData** <br/> |1  <br/> |Devuelve el contenido de la página sin marcado de selección, pero con todos los datos binarios.  <br/> |
|**piSelection** <br/> |segundo  <br/> |Devuelve el contenido de la página con marcado de selección, pero sin datos binarios.  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |Devuelve el contenido de la página con marcado de selección y todos los datos binarios.  <br/> |
|**piFileType** <br/> |4   <br/> |Devuelve el contenido de la página con información de tipo de archivo para los objetos de datos binarios.  <br/> |
|**piBinaryDataFileType** <br/> |5   <br/> |Devuelve el contenido de la página con información de tipo de archivo para objetos de datos binarios y objetos de datos binarios  <br/> |
|**piSelectionFileType** <br/> |6   <br/> |Devuelve el contenido de la página con marcado de selección y la información de tipo de archivo de los datos binarios.  <br/> |
|**piAll** <br/> |7   <br/> |Devuelve todo el contenido de la página.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Cuando se pasa al método **Publish** , especifica el formato en el que aparecerá la página publicada. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |comprendi  <br/> |La página publicada está en el formato. One.  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |La página publicada tiene el formato. onepkg.  <br/> |
|**pfMHTML** <br/> |segundo  <br/> |La página publicada tiene el formato. mht.  <br/> |
|**pfPDF** <br/> |3  <br/> |La página publicada está en formato. pdf.  <br/> |
|**pfXPS** <br/> |4   <br/> |La página publicada está en formato. XPS.  <br/> |
|**pfWord** <br/> |5   <br/> |La página publicada está en formato. doc o. docx.  <br/> |
|**pfEMF** <br/> |6   <br/> |La página publicada está en formato de metarchivo mejorado (. EMF).  <br/> |
|**pfHTML** <br/> |7   <br/> |La página publicada está en formato. html. Este miembro es nuevo en OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8   <br/> |La página publicada está en el formato 2007. One. Este miembro es nuevo en OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Cuando se pasa al método **SetRecentResults** del objeto **IQuickFilingDialog** , especifica la lista de resultados recientes que se va a mostrar cuando se represente el cuadro de diálogo de archivado rápido. Las listas de resultados recientes se usan para realizar un seguimiento del conjunto de ubicaciones de OneNote que el usuario selecciona en el cuadro de diálogo de archivado rápido. Hay tres listas de resultados recientes de OneNote 2013 que realizan un seguimiento de las acciones de archivado, búsqueda y vinculación. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |comprendi  <br/> |No establece la lista de resultados recientes que se va a representar.  <br/> |
|**rrtFiling** <br/> |1  <br/> |Establece la lista de resultados recientes de "archivar" que se va a representar.  <br/> |
|**rrtSearch** <br/> |segundo  <br/> |Establece la lista de resultados "Buscar" reciente que se va a representar.  <br/> |
|**rrtLinks** <br/> |3  <br/> |Establece la lista de resultados recientes "links" que se va a representar.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Cuando se pasa al método **GetSpecialLocation** , especifica la ruta de acceso de ubicación especial que se debe obtener. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |comprendi  <br/> |Obtiene la ruta de acceso a la ubicación de la carpeta de carpetas de copia de seguridad.  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtiene la ruta de acceso a la ubicación de la carpeta notas no archivadas.  <br/> |
|**slDefaultNotebookFolder** <br/> |segundo  <br/> |Obtiene la ruta de acceso a la ubicación predeterminada de la carpeta del Bloc de notas.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Cuando se pasa al método **TreeCollapsedState** del objeto **QFD** , especifica si el árbol de jerarquía se debe expandir o contraer. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |comprendi  <br/> |Establece el árbol de jerarquía en expandido.  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |Establece el árbol de jerarquía en contraído.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (actualizado para OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Cuando se pasa a uno de los métodos siguientes, especifica la versión del esquema XML de OneNote que se va a usar:
  
- **OneNote15. Application. GetPageContent**
    
- **OneNote15. Application. FindMeta**
    
- **OneNote15. Application. FindPages**
    
- **OneNote15. Application. GetHierarchy**
    
- **OneNote15. Application. GetPageContent**
    
- **OneNote15. Application. UpdateHierarchy**
    
- **OneNote15. Application. UpdatePageContent**
    
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**xs2007** <br/> |comprendi  <br/> |Hace referencia al esquema de OneNote 2007.  <br/> |
|**xs2010** <br/> |1  <br/> |Hace referencia al esquema de OneNote 2010.  <br/> |
|**xs2013** <br/> |segundo  <br/> |Hace referencia al esquema de OneNote 2013.  <br/> |
|**xsCurrent** <br/> |segundo  <br/> |Hace referencia al esquema de la versión actual de OneNote.  <br/> <br/>**Nota**: no se recomienda usar **xsCurrent** en la mayoría de los casos, ya que puede causar problemas de compatibilidad con versiones futuras de OneNote. En su lugar, especifique la versión del esquema con el que se creó la aplicación, como xs2013.           |
   
## <a name="see-also"></a>Ver también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

