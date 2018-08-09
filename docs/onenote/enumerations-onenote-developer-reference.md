---
title: Enumeraciones (referencia para desarrolladores de OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: En este tema se describe las enumeraciones en el modelo de objetos de OneNote 2013.
ms.openlocfilehash: ccd75843326ea5942aa80d02246e59e92331a7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816040"
---
# <a name="enumerations-onenote-developer-reference"></a>Enumeraciones (referencia para desarrolladores de OneNote)

En este tema se describe las enumeraciones en el modelo de objetos de OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Cuando se pasa al método **OpenHierarchy** , especifica el tipo del objeto que se va a crear, si lo hay, si la ruta de acceso que se pasa al método todavía no existe. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |No crea ningún objeto nuevo.  <br/> |
|**cftNotebook** <br/> |1  <br/> |Crea un bloc de notas con el nombre especificado y la ubicación.  <br/> |
|**cftFolder** <br/> |2  <br/> |Crea un grupo de sección con el nombre especificado y la ubicación.  <br/> |
|**cftSection** <br/> |3  <br/> |Crea una sección con el nombre especificado y la ubicación.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indica la ubicación de una ventana de OneNote 2013 acoplada mediante la interfaz de la [ventana](window-interfaces-onenote.md) . Cuando se establece en el **DockedLocation** (propiedad), especifica la ubicación en la que se acopla una ventana de OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |La ventana de OneNote está acoplada en la ubicación predeterminada en el escritorio.  <br/> |
|**dlLeft** <br/> |1  <br/> |La ventana de OneNote está acoplada en el lado izquierdo del escritorio.  <br/> |
|**dlRight** <br/> |2  <br/> |La ventana de OneNote está acoplada en el lado derecho del escritorio.  <br/> |
|**dlTop** <br/> |3  <br/> |La ventana de OneNote está acoplada en la parte superior del escritorio.  <br/> |
|**dlBottom** <br/> |4  <br/> |La ventana de OneNote está acoplada en la parte inferior del escritorio.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Cuando se pasa al método **SetFilingLocation** , especifica qué tipo de contenido se establece la ubicación de archivado para cuando el tipo de contenido se envía a OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Conjuntos de donde se archivará los mensajes de correo electrónico de Outlook.  <br/> |
|**flContacts** <br/> |1  <br/> |Conjuntos de donde se archivará los contactos de Outlook.  <br/> |
|**flTasks** <br/> |2  <br/> |Conjuntos de donde se almacenará las tareas de Outlook.  <br/> |
|**flMeetings** <br/> |3  <br/> |Conjuntos de donde se archivará reuniones de Outlook.  <br/> |
|**flWebContent** <br/> |4  <br/> |Conjuntos de donde se almacenará el contenido de Internet Explorer.  <br/> |
|**flPrintOuts** <br/> |5  <br/> |Conjuntos de donde se almacenará copias impresas de la impresora de OneNote.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Cuando se pasa al método **SetFilingLocation** , especifica donde se archiva el contenido que se envía a OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Establece el contenido que desea archivar en una página nueva en un objeto section especificado.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Establece el contenido que desea archivar en una nueva página en la sección actual.  <br/> |
|**fltCurrentPage** <br/> |2  <br/> |Establece el contenido que desea archivar en la página actual.  <br/> |
|**fltNamedPage** <br/> |4  <br/> |Establece el contenido que desea archivar en la página especificada.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Cuando se asigna a la propiedad **TreeDepth** de la interfaz [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md) , especifica la profundidad del árbol de OneNote para mostrar cuando se presenta el cuadro de diálogo de archivado rápido. Cuando se pasa al método **botón Agregar** del objeto **IQuickFilingDialog** , hace referencia a ciertos elementos en la jerarquía de OneNote. Esta enumeración es nueva en OneNote 2013. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |Hace referencia a ningún elemento.  <br/> |
|**heNotebooks** <br/> |1  <br/> |Hace referencia a los elementos del Bloc de notas.  <br/> |
|**heSectionGroups** <br/> |2  <br/> |Hace referencia a los elementos del grupo de sección.  <br/> |
|**heSections** <br/> |4  <br/> |Hace referencia a los elementos de sección.  <br/> |
|**hePages** <br/> |8  <br/> |Hace referencia a los elementos de página.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **GetHierarchy** , especifica el nivel más bajo para obtener en la jerarquía de nodos de Bloc de notas. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtiene sólo en el nodo de inicio especificado y ningún descendiente.  <br/> |
|**hsChildren** <br/> |1  <br/> |Obtiene los inmediato nodos secundarios del nodo de inicio y ningún descendiente en grupos de subsección mayores o menores.  <br/> |
|**hsNotebooks** <br/> |2  <br/> |Obtiene todos los blocs de notas debajo del nodo de inicio o raíz.  <br/> |
|**hsSections** <br/> |3  <br/> |Obtiene todas las secciones debajo del nodo de inicio, incluidas las secciones en grupos de secciones y grupos de la subsección.  <br/> |
|**hsPages** <br/> |4  <br/> |Obtiene todas las páginas por debajo del nodo de inicio, incluidas todas las páginas en grupos de secciones y grupos de la subsección.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **CreateNewPage** , especifica el estilo de la nueva página. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Crea una página que tiene el estilo de página predeterminado.  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Crea una página en blanco que tiene un título.  <br/> |
|**npsBlankPageNoTitle** <br/> |2  <br/> |Crea una página en blanco que no tiene ningún título.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Cuando se pasa al método **NotebookFilterOut** del objeto **QFD** , especifica qué blocs de notas para mostrar cuando se procesa el cuadro QFD. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Permitir que solo los blocs de notas Local.  <br/> |
|**nfoNetwork** <br/> |2  <br/> |Permite UNC o blocs de notas de SharePoint.  <br/> |
|**nfoWeb** <br/> |4  <br/> |Permite a los blocs de notas de OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8  <br/> |Los blocs de notas en ubicaciones que no tienen un cliente web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (que se actualizó para OneNote 2013)
<a name="odc_PageInfo"> </a>

Cuando se pasa al método **GetPageContent** , especifica el tipo de información que se devuelve con el contenido de la página. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Devuelve el contenido de página sólo básica, sin marcas de revisión de selección, tipos de archivo para objetos de datos binarios y datos binarios. Éste es el valor estándar para pasar.  <br/> |
|**piBinaryData** <br/> |1  <br/> |Devuelve la página contenido con ningún formato de la selección, pero con todos los datos binarios.  <br/> |
|**piSelection** <br/> |2  <br/> |Devuelve la página contenido con el marcado de la selección, pero no hay datos binarios.  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |Devuelve la página contenido con formato de la selección y todos los datos binarios.  <br/> |
|**piFileType** <br/> |4  <br/> |Devuelve la página contenido con información de tipo de archivo para los objetos de datos binarios.  <br/> |
|**piBinaryDataFileType** <br/> |5  <br/> |Devuelve la página contenido con información de tipo de archivo para objetos de datos binarios y datos binarios  <br/> |
|**piSelectionFileType** <br/> |6  <br/> |Devuelve la página contenido con selección marcado y el archivo de información de tipo de datos binarios.  <br/> |
|**piAll** <br/> |7  <br/> |Devuelve todo el contenido de página.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Cuando se pasa al método de **publicación** , especifica el formato en el que se mostrará la página publicada. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |Página publicada está en el formato .one.  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |Página publicada está en el formato onepkg.  <br/> |
|**pfMHTML** <br/> |2  <br/> |Página publicada está en el formato .mht.  <br/> |
|**pfPDF** <br/> |3  <br/> |Página publicada está en el formato .pdf.  <br/> |
|**pfXPS** <br/> |4  <br/> |Página publicada está en el formato .xps.  <br/> |
|**pfWord** <br/> |5  <br/> |Página publicada está en el formato de archivo .doc o .docx.  <br/> |
|**pfEMF** <br/> |6  <br/> |Página publicada está en el formato de metarchivo mejorado (.emf).  <br/> |
|**pfHTML** <br/> |7  <br/> |Página publicada está en el formato HTML. Este miembro es nueva en OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8  <br/> |Página publicada está en el formato de .one de 2007. Este miembro es nueva en OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Cuando se pasa al método **SetRecentResults** del objeto **IQuickFilingDialog** , especifica qué lista de resultados recientes para mostrar cuando se presenta el cuadro de diálogo de archivado rápido. Listas de resultados recientes se utilizan para seguir el conjunto de ubicaciones de OneNote que el usuario selecciona en el cuadro de diálogo de archivado rápido. Hay tres listas de resultado reciente en OneNote 2013 que realizar un seguimiento de archivado, búsqueda y vinculación de acciones. Esta enumeración es nueva en OneNote 2013. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |No establece ninguna lista resultado reciente que se va a representar.  <br/> |
|**rrtFiling** <br/> |1  <br/> |Establece la lista de resultado reciente "Archivando" que se va a representar.  <br/> |
|**rrtSearch** <br/> |2  <br/> |Establece la lista de resultado reciente "Búsqueda" que se va a representar.  <br/> |
|**rrtLinks** <br/> |3  <br/> |Establece la lista de resultado reciente "Vínculos" que se va a representar.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Cuando se pasa al método **GetSpecialLocation** , especifica la ruta de acceso de ubicación especial para obtener. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtiene la ruta de acceso a la ubicación de carpeta de carpetas de copia de seguridad.  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtiene la ruta de acceso a la ubicación de la carpeta Notas sin archivar.  <br/> |
|**slDefaultNotebookFolder** <br/> |2  <br/> |Obtiene la ruta de acceso a la ubicación de la carpeta predeterminada Bloc de notas.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Cuando se pasa al método **TreeCollapsedState** del objeto **QFD** , especifica si se debe expandir o contraer el árbol de la jerarquía. 
  
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Establece el árbol de la jerarquía expandida.  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |Establece el árbol de la jerarquía para contraída.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (actualizado para OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Cuando se pasa a uno de los métodos siguientes, especifica la versión del esquema XML de OneNote para usar:
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**Elemento**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Hace referencia al esquema de OneNote 2007.  <br/> |
|**xs2010** <br/> |1  <br/> |Hace referencia al esquema de OneNote 2010.  <br/> |
|**xs2013** <br/> |2  <br/> |Hace referencia al esquema de OneNote 2013.  <br/> |
|**xsCurrent** <br/> |2  <br/> |Hace referencia al esquema de la versión actual de OneNote.  <br/> <br/>**Nota**: no se recomienda el uso de **xsCurrent** en la mayoría de los casos, ya que puede causar problemas de compatibilidad con las futuras versiones de OneNote. En su lugar, especifique la versión del esquema que se creó la aplicación para controlar, al igual que xs2013.           |
   
## <a name="see-also"></a>Vea también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

