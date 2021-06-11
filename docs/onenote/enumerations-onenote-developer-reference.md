---
title: Enumeraciones (OneNote de desarrollador)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: En este tema se describen las enumeraciones del OneNote de objetos de 2013.
ms.openlocfilehash: 3338e444e5b0bfd0239e363c3161aeb1914b2d53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410339"
---
# <a name="enumerations-onenote-developer-reference"></a>Enumeraciones (OneNote de desarrollador)

En este tema se describen las enumeraciones del OneNote de objetos de 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Cuando se pasa al **método OpenHierarchy,** especifica el tipo de objeto que se va a crear, si existe, si la ruta de acceso pasada al método aún no existe. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |No crea ningún objeto nuevo.  <br/> |
|**cftNotebook** <br/> |1  <br/> |Crea un bloc de notas con el nombre y la ubicación especificados.  <br/> |
|**cftFolder** <br/> |2  <br/> |Crea un grupo de secciones mediante el nombre y la ubicación especificados.  <br/> |
|**cftSection** <br/> |3  <br/> |Crea una sección mediante el nombre y la ubicación especificados.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indica la ubicación acoplada de una OneNote de 2013 mediante la [interfaz De ventana.](window-interfaces-onenote.md) Cuando se establece en **la propiedad DockedLocation,** especifica la ubicación en la que se acopla una OneNote base de datos. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |La OneNote está acoplada en la ubicación predeterminada del escritorio.  <br/> |
|**dlLeft** <br/> |1  <br/> |La OneNote está acoplada en el lado izquierdo del escritorio.  <br/> |
|**dlRight** <br/> |2  <br/> |La OneNote está acoplada en el lado derecho del escritorio.  <br/> |
|**dlTop** <br/> |3  <br/> |La OneNote está acoplada en la parte superior del escritorio.  <br/> |
|**dlBottom** <br/> |4   <br/> |La OneNote está acoplada en la parte inferior del escritorio.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Cuando se pasa al **método SetFilingLocation,** especifica el tipo de contenido para el que se establece la ubicación de archivado cuando se envía el tipo de contenido a OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Establece dónde Outlook se van a presentar los mensajes de correo electrónico.  <br/> |
|**flContacts** <br/> |1  <br/> |Establece dónde Outlook se van a presentar los contactos.  <br/> |
|**flTasks** <br/> |2  <br/> |Establece dónde Outlook se van a presentar las tareas.  <br/> |
|**flMeetings** <br/> |3  <br/> |Establece dónde Outlook se van a presentar las reuniones.  <br/> |
|**flWebContent** <br/> |4   <br/> |Establece dónde se va a presentar el contenido de Internet Explorer.  <br/> |
|**flPrintOuts** <br/> |5   <br/> |Establece dónde se presentarán las OneNote de la impresora.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Cuando se pasa al **método SetFilingLocation,** especifica dónde se OneNote contenido que se envía a la propiedad. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Establece el contenido que se va a presentar en una página nueva de una sección especificada.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Establece el contenido que se va a presentar en una página nueva de la sección actual.  <br/> |
|**fltCurrentPage** <br/> |2  <br/> |Establece el contenido que se va a presentar en la página actual.  <br/> |
|**fltNamedPage** <br/> |4   <br/> |Establece el contenido que se va a presentar en una página especificada.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Cuando se asigna a la propiedad **TreeDepth** de la interfaz [IQuickFilingDialog,](quick-filing-dialog-box-interfaces-onenote.md) especifica la profundidad del árbol de OneNote que se mostrará cuando se represente el cuadro de diálogo de archivado rápido. Cuando se pasa al **método AddButton** del **objeto IQuickFilingDialog,** hace referencia a determinados elementos de la OneNote jerarquía. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |No hace referencia a ningún elemento.  <br/> |
|**heNotebooks** <br/> |1  <br/> |Hace referencia a los elementos notebook.  <br/> |
|**heSectionGroups** <br/> |2  <br/> |Hace referencia a los elementos de grupo de secciones.  <br/> |
|**heSections** <br/> |4   <br/> |Hace referencia a los elementos Section.  <br/> |
|**hePages** <br/> |8   <br/> |Hace referencia a los elementos Page.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al **método GetHierarchy,** especifica el nivel más bajo para obtener en la jerarquía de nodos del bloc de notas. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtiene solo el nodo de inicio especificado y no hay descendientes.  <br/> |
|**hsChildren** <br/> |1  <br/> |Obtiene los nodos secundarios inmediatos del nodo de inicio y no hay descendientes en grupos de subsecciones superiores o inferiores.  <br/> |
|**hsNotebooks** <br/> |2  <br/> |Obtiene todos los blocs de notas debajo del nodo de inicio o raíz.  <br/> |
|**hsSections** <br/> |3  <br/> |Obtiene todas las secciones debajo del nodo de inicio, incluidas las secciones de grupos de secciones y grupos de subsecciones.  <br/> |
|**hsPages** <br/> |4   <br/> |Obtiene todas las páginas debajo del nodo de inicio, incluidas todas las páginas de grupos de secciones y grupos de subsección.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al **método CreateNewPage,** especifica el estilo de la nueva página. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Crea una página que tiene el estilo de página predeterminado.  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Crea una página en blanco que tiene un título.  <br/> |
|**npsBlankPageNoTitle** <br/> |2  <br/> |Crea una página en blanco que no tiene título.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **NotebookFilterOut** del objeto **QFD,** especifica qué blocs de notas se mostrarán cuando se represente el cuadro QFD. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Permitir solo blocs de notas locales.  <br/> |
|**nfoNetwork** <br/> |2  <br/> |Permite unc o SharePoint blocs de notas.  <br/> |
|**nfoWeb** <br/> |4   <br/> |Permite OneDrive blocs de notas.  <br/> |
|**nfoNoWacUrl** <br/> |8   <br/> |Blocs de notas en ubicaciones que no tienen un cliente web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (actualizado para OneNote 2013)
<a name="odc_PageInfo"> </a>

Cuando se pasa al **método GetPageContent,** especifica el tipo de información que se devolverá con el contenido de la página. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Devuelve solo contenido básico de página, sin marcado de selección, tipos de archivo para objetos de datos binarios y objetos de datos binarios. Este es el valor estándar que se debe pasar.  <br/> |
|**piBinaryData** <br/> |1  <br/> |Devuelve contenido de página sin marcado de selección, pero con todos los datos binarios.  <br/> |
|**piSelection** <br/> |2  <br/> |Devuelve contenido de página con marcado de selección, pero no datos binarios.  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |Devuelve el contenido de la página con marcado de selección y todos los datos binarios.  <br/> |
|**piFileType** <br/> |4   <br/> |Devuelve contenido de página con información de tipo de archivo para objetos de datos binarios.  <br/> |
|**piBinaryDataFileType** <br/> |5   <br/> |Devuelve contenido de página con información de tipo de archivo para objetos de datos binarios y objetos de datos binarios  <br/> |
|**piSelectionFileType** <br/> |6   <br/> |Devuelve contenido de página con marcado de selección e información de tipo de archivo para datos binarios.  <br/> |
|**piAll** <br/> |7   <br/> |Devuelve todo el contenido de la página.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Cuando se pasa al **método Publish,** especifica el formato en el que aparecerá la página publicada. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |La página publicada tiene el formato .one.  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |La página publicada tiene el formato .onepkg.  <br/> |
|**pfMHTML** <br/> |2  <br/> |La página publicada tiene el formato .mht.  <br/> |
|**pfPDF** <br/> |3  <br/> |La página publicada está en .pdf formato.  <br/> |
|**pfXPS** <br/> |4   <br/> |La página publicada tiene el formato .xps.  <br/> |
|**pfWord** <br/> |5   <br/> |La página publicada está en el .doc o .docx formato.  <br/> |
|**pfEMF** <br/> |6   <br/> |La página publicada está en el formato de metarchivo mejorado (.emf).  <br/> |
|**pfHTML** <br/> |7   <br/> |La página publicada está en .html formato. Este miembro es nuevo en OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8   <br/> |La página publicada tiene el formato 2007 .one. Este miembro es nuevo en OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Cuando se pasa al **método SetRecentResults** del objeto **IQuickFilingDialog,** especifica qué lista de resultados recientes se mostrará cuando se represente el cuadro de diálogo Archivo rápido. Las listas de resultados recientes se usan para realizar un seguimiento del conjunto de OneNote que el usuario selecciona en el cuadro de diálogo Archivo rápido. Hay tres listas de resultados recientes en OneNote 2013 que rastrean las acciones de archivado, búsqueda y vinculación. Esta enumeración es nueva en OneNote 2013. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |No establece ninguna lista de resultados recientes que se va a representar.  <br/> |
|**rrtFiling** <br/> |1  <br/> |Establece la lista de resultados recientes de "Archivado" que se va a representar.  <br/> |
|**rrtSearch** <br/> |2  <br/> |Establece la lista de resultados recientes de "Búsqueda" que se va a representar.  <br/> |
|**rrtLinks** <br/> |3  <br/> |Establece la lista de resultados recientes "Vínculos" que se va a representar.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Cuando se pasa al **método GetSpecialLocation,** especifica la ruta de acceso de ubicación especial que se debe obtener. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtiene la ruta de acceso a la ubicación de carpeta Carpetas de copia de seguridad.  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtiene la ruta de acceso a la ubicación de la carpeta Notas sin archivo.  <br/> |
|**slDefaultNotebookFolder** <br/> |2  <br/> |Obtiene la ruta de acceso a la ubicación predeterminada de la carpeta Bloc de notas.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Cuando se pasa al **método TreeCollapsedState** del objeto **QFD,** especifica si el árbol de jerarquía debe expandirse o contraerse. 
  
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Establece el árbol de jerarquía en expandido.  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |Establece el árbol de jerarquía en contraído.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (actualizado para OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Cuando se pasa a uno de los métodos siguientes, especifica la versión del esquema XML OneNote usar:
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**Miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Hace referencia OneNote esquema de 2007.  <br/> |
|**xs2010** <br/> |1  <br/> |Hace referencia OneNote esquema de 2010.  <br/> |
|**xs2013** <br/> |2  <br/> |Hace referencia OneNote esquema de 2013.  <br/> |
|**xsCurrent** <br/> |2  <br/> |Hace referencia al esquema de la versión OneNote actual.  <br/> <br/>**NOTA:** No se recomienda usar **xsCurrent** en la mayoría de los casos, ya que puede causar problemas de compatibilidad con versiones futuras de OneNote. En su lugar, especifique la versión del esquema que la aplicación se creó para controlar, como xs2013.           |
   
## <a name="see-also"></a>Ver también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

