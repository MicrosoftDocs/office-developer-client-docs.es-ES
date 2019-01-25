---
title: Interfaz de la aplicación (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'La interfaz de la aplicación incluye métodos que ayudan a recuperar, manipular y actualizar información y contenido de OneNote. Los métodos se encuentran en cuatro categorías generales:'
localization_priority: Priority
ms.openlocfilehash: 20b2fc42711aaf4f1b407efb2c70057bd88a9046
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708000"
---
# <a name="application-interface-onenote"></a>Interfaz de la aplicación (OneNote)

La interfaz de la **aplicación** incluye métodos que ayudan a recuperar, manipular y actualizar información y contenido de OneNote. Los métodos se encuentran en cuatro categorías generales: 
  
- **Estructura de bloc de notas** &ndash; Métodos para trabajar con la estructura del bloc de notas, incluidos aquellos que permiten detectar, abrir, modificar, cerrar y eliminar los blocs de notas, secciones y grupos de secciones. 
    
- **Contenido de página** &ndash; Métodos para trabajar con páginas y contenido de páginas, incluidos aquellos que permiten detectar, modificar, guardar y eliminar contenido de la página. El contenido de la página incluye objetos binarios, como imágenes y escritura en lápiz y objetos de texto, como esquemas. 
    
- **Navegación** &ndash; Métodos para realizar búsquedas, vinculaciones y desplazamientos en relación con páginas y objetos. 
    
- **Funcional** &ndash; Todos los demás métodos que realizan determinadas acciones o establecen parámetros en OneNote. 
    
Además, la interfaz de la **aplicación** incluye una serie de *propiedades* y *eventos*. 
  
## <a name="notebook-structure-methods"></a>Métodos de estructura del Bloc de notas
<a name="ON14DevRef_Application_NotebookStructure"> </a>

Los métodos descritos en esta sección te permiten descubrir, abrir, modificar, cerrar y eliminar blocs de notas, secciones y grupos de secciones de OneNote.
  
### <a name="gethierarchy-method"></a>Método GetHierarchy

|||
|:-----|:-----|
|**Descripción** <br/> |Obtiene la estructura de jerarquía del nodo del bloc de notas, empezando desde el nodo que especificas (todos los blocs de notas o un único bloc de notas, grupo de secciones o sección) y siguiendo hacia abajo a todos los descendientes en el nivel que especifiques.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Parámetros** <br/> | _bstrStartNodeID_ &ndash; El nodo (bloc de notas, grupo de sección o sección) cuyos descendientes deseas. Si pasas una cadena nula (""), el método obtiene todos los nodos debajo del nodo raíz (es decir, todos los blocs de notas, grupos de secciones y secciones). Si especificas un bloc de notas, grupo de sección o nodo de sección, el método obtiene solo descendientes de ese nodo.  <br/><br/>_hsScope_ &ndash; El nivel más bajo de nodo descendiente que deseas. Por ejemplo, si especificas páginas, el método obtiene todos los nodos hasta el nivel de la página. Si especificas secciones, el método obtiene solo los nodos de sección debajo del bloc de notas. Para obtener más información, consulta la enumeración **HierarchyScope** en el tema [Enumeraciones](enumerations-onenote-developer-reference.md#odc_HierarchyScope).  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; (parámetro de salida) Un puntero para la cadena en la que deseas que OneNote escriba el resultado de XML.  <br/><br/>_xsSchema_ &ndash; (opcional) La versión del esquema XML de OneNote, del tipo **XMLSchema**, que quieres que sea el resultado. Puedes especificar si deseas el esquema XML versión 2013, 2010, 2007 o la versión actual.  <br/><br/>**NOTA**: Te recomendamos que especifiques una versión de OneNote (como **xs2013**) en lugar de usar **xsCurrent** o dejar en blanco, ya que esto le permitirá a tu complemento trabajar con versiones futuras de OneNote.           |
   
El método de GetHierarchy devuelve una cadena en formato XML de OneNote 2013 de forma predeterminada, o bien puedes establecer la versión del esquema XML preferida utilizando el parámetro _xsSchema_ opcional. 
  
Dependiendo de los parámetros que pases, el método **GetHierarchy** puede devolver varias listas (por ejemplo, todos los blocs de notas, todas las secciones en todos los blocs de notas, todas las páginas de una sección determinada o todas las páginas dentro de un bloc de notas determinado). Para cada nodo, la cadena XML devuelta proporciona propiedades (por ejemplo, el título de sección o página, la identificación y la última modificación). 
  
No todas las combinaciones de nodo inicial y ámbito son válidas. Por ejemplo, si especificas un nodo inicial de sección y un ámbito de bloc de notas, **GetHierarchy** devuelve un resultado nulo porque un bloc de notas es superior en la jerarquía de nodos a una sección. 
  
El siguiente ejemplo C# muestra cómo usar el método **GetHierarchy** para obtener toda la jerarquía de OneNote, incluidos todos los blocs de notas, hasta el nivel de la página. Copia la cadena de salida en el Portapapeles, desde donde puedes pegar la cadena en un editor de texto para revisarla. 
  
```cs
static void GetEntireHierarchy()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(null, 
            OneNote.HierarchyScope.hsPages, out strXML);
        Clipboard.SetText(strXML);
        MessageBox.Show("The XML has been copied to the clipboard");
    }

```

### <a name="updatehierarchy-method"></a>Método UpdateHierarchy

|||
|:-----|:-----|
|**Descripción**|Modifica o actualiza la jerarquía de los blocs de notas. Por ejemplo, puedes agregar secciones o grupos de secciones en un bloc de notas, agregar un bloc de notas nuevo, mover secciones dentro de un bloc de notas, cambiar el nombre de una sección, agregar páginas a una sección o cambiar el orden de las páginas dentro de las secciones.|
|**Sintaxis**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Parámetros**| _bstrChangesXmlIn_ &ndash; Una cadena que contiene el código XML de OneNote que especifica los cambios de jerarquía que se deben realizar. Por ejemplo, si deseas insertar una nueva sección, puedes agregar un elemento **Sección** en la cadena XML para indicar dónde quieres que se agregue la nueva sección. Como alternativa, si deseas cambiar el nombre de una sección existente, puedes mantener el mismo identificador de sección y cambiar su atributo **nombre** en el código XML.<br/><br/>_xsSchema_ &ndash; (opcional) La versión del esquema de OneNote de la cadena _bstrChangesXmln_. Este valor opcional se usa para especificar la versión del esquema XML de OneNote en la que se encuentra la cadena _bstrChangesXmlIn_. Si no se especifica este valor, OneNote supondrá que el archivo XML se encuentra en la versión del esquema _xsCurrent_. <br/><br/>**NOTA**: Te recomendamos que especifiques una versión de OneNote (como **xs2013**) en lugar de usar **xsCurrent** o dejar en blanco, ya que esto le permitirá a tu complemento trabajar con versiones futuras de OneNote.           |
   
Si pasas solo una cadena parcial de XML de OneNote para el parámetro _bstrChangesXmlIn_, OneNote intentará deducir los cambios que deseas. Por ejemplo, si incluyes un elemento **Bloc de notas** que contiene solo una sección, OneNote agrega la sección después de las secciones existentes. Sin embargo, si la operación que especificas es ambigua, puede ser difícil determinar el resultado. Por ejemplo, si un bloc de notas existente contiene cuatro secciones, y la cadena XML que pasas incluye el bloc de notas y solo las secciones cuarta y primera (en ese orden), OneNote puede colocar la segunda y tercera sección antes de la cuarta sección o después de la primera. 
  
No puedes usar el método **UpdateHierarchy** para eliminar parte de un bloc de notas. Es decir, pasar una cadena XML que incluya solo una parte de una jerarquía existente no elimina secciones que no se incluyen en la cadena. Para eliminar parte de una jerarquía, usa el método **DeleteHierarchy**. 
  
El siguiente código C# muestra una forma de usar el método **UpdateHierarchy** para cambiar la jerarquía de OneNote, mediante la modificación del nombre de una sección existente. Lee el código XML desde un archivo de ejemplo denominado ChangeSectionName.xml en la raíz de la unidad C, lo carga en un documento XML y luego pasa la estructura XML de ese documento al método. 
  
```cs
static void UpdateExistingHierarchy()
    {
        OneNote.Application onApplication = new OneNote.Application();
        
        // Get the XML from the file.
        XmlTextReader reader = new XmlTextReader("C:\\ChangeSectionName.xml");
        reader.WhitespaceHandling = WhitespaceHandling.None;
        XmlDocument xmlDocIn = new XmlDocument();
        xmlDocIn.Load(reader);
        
        // Update the hierarchy.
        onApplication.UpdateHierarchy(xmlDocIn.OuterXml,
        OneNote.XMLSchema.xs2007);   
    }

```

El siguiente código XML es un fragmento del archivo ChangeSectionName.xml que el anterior código C# pasa al método. Cuando el archivo XML se pasa al método **UpdateHierarchy**, cambia el nombre de una de las secciones en la jerarquía existente (al cambiar el valor del atributo **nombre** a "Mi sección con nombre nuevo"). A continuación, quita todas las secciones excepto aquella cuyo nombre cambió. Además, el código quita atributos innecesarios del elemento de destino **Sección**, incluidos los atributos **lastModifiedTime**, **isCurrentlyViewed**y **color**, dejando solo los atributos **nombre**, **ID** y **ruta** intactos. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="https://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

Se obtuvo el código XML anterior mediante el código que se muestra en el ejemplo del método **GetHierarchy**, que se modifica, como se indica a continuación, para limitar el ámbito de las secciones. 
  
```cs
static void GetAllSections()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(System.String.Empty, 
            OneNote.HierarchyScope.hsSections, out strXML);
        Clipboard.SetText(strXML.ToString());
        MessageBox.Show("The XML has been copied to the Clipboard");
    }

```

El siguiente ejemplo C# muestra una aplicación de consola completa que busca una sección denominada " `Sample_Section`", solicita al usuario que escriba un nuevo nombre para la sección y, después, usa el método **UpdateHierarchy** para cambiar el nombre de sección por el nombre que escribió el usuario. Antes de ejecutar el código, cambia " `Sample_Section`" por el nombre de una sección existente en tu jerarquía de OneNote.
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "https://schemas.microsoft.com/office/onenote/2013/onenote";
        string outputXML;
        Application onApplication = new Application();
        onApplication.GetHierarchy(null, HierarchyScope.hsSections, out outputXML);
        // Load a new XmlDocument.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.LoadXml(outputXML);
        XmlNamespaceManager nsmgr = new XmlNamespaceManager(xmlDoc.NameTable);
            nsmgr.AddNamespace("one", strNamespace);
        // Search for the section named "Sample_Section".
        XmlNode xmlNode = xmlDoc.SelectSingleNode("//one:Section[@name='Sample_Section']", nsmgr);
        // Prompt for a new section title.
        System.Console.Write("Please enter a new title for the section: ");
        string input = System.Console.ReadLine();
        xmlNode.Attributes["name"].Value = input; 
        // Update the section with the new title.
        onApp.UpdateHierarchy(xmlNode.OuterXml);
        System.Console.Write("Done!\n");
    }

```

### <a name="openhierarchy-method"></a>Método OpenHierarchy

|||
|:-----|:-----|
|**Descripción** <br/> |Abre un grupo de sección o sección que especificas.  <br/> |
|**Sintaxis** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Parámetros** <br/> | _bstrPath_ &ndash; La ruta que deseas abrir. Para un bloc de notas, o para un grupo de secciones en un bloc de notas, _bstrPath_ puede ser una ruta a una carpeta o la ruta a un archivo de sección .one. Si especificas la ruta a un archivo de sección .one, debes incluir la extensión .one en la cadena de ruta del archivo.  <br/><br/>_bstrRelativeToObjectID_ &ndash; La id. de OneNote del objeto primario (grupo del bloc de notas o sección) donde deseas que se abra el nuevo objeto. Si el parámetro _bstrPath_ es una ruta absoluta, puedes pasar una cadena vacía ("") para _bstrRelativeToObjectID_. Como alternativa, puedes pasar la id. del objeto del grupo de bloc de notas o sección que debe contener el objeto (sección o grupo de secciones) que deseas crear y, a continuación, especificar el nombre de archivo (por ejemplo, section1.one) del objeto que deseas crear bajo ese objeto primario.  <br/><br/>_pbstrObjectID_ &ndash; (parámetro de salida) La id. del objeto que OneNote devuelve para el bloc de notas, grupo de sección o sección que abre el método **OpenHierarchy**. Este parámetro es un puntero de la cadena en la que deseas que el método escriba la id.  <br/><br/>_cftlfNotExist_ &ndash; (opcional) Un valor enumerado de la enumeración [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType). Si pasas un valor para _cftIfNotExist_, el método **OpenHierarchy** crea el archivo de sección o grupo de secciones en la ruta especificada solo si el archivo todavía no existe.  <br/> |
   
Si especificas un grupo de secciones que no está en un bloc de notas abierto, el método **OpenHierarchy** abre el grupo de secciones como un bloc de notas. Si especificas un grupo de secciones que no está en un bloc de notas abierto, el método **OpenHierarchy** abre la sección en el grupo de sección Secciones Abiertas Recientemente. Si especificas un grupo de secciones o sección que ya está en un bloc de notas abierto, no sucede nada porque la sección o grupo de secciones ya están abiertos también. En cualquier caso, **OpenHierarchy** devuelve la id. de objeto del grupo de sección, bloc de notas o sección que especifiques, para que puedes usarlos en otras operaciones. 
  
También puedes usar el método **OpenHierarchy** para crear secciones nuevas, en lugar de hacerlo mediante la importación de XML. 
  
El código siguiente muestra cómo usar el método **OpenHierarchy** para abrir la sección de Reuniones en el bloc de notas de trabajo y obtener la id. de la sección. Si todavía no existe la sección, OneNote la crea en la ubicación que especifiques. 
  
```cs
static void OpenSection()
    {
        String strID;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.OpenHierarchy("C:\\Documents and Settings\\user\\My Documents\\OneNote Notebooks\\Work\\Meetings.one", 
        System.String.Empty, out strID, OneNote.CreateFileType.cftSection);
    }

```

### <a name="deletehierarchy-method"></a>Método DeleteHierarchy

|||
|:-----|:-----|
|**Descripción** <br/> |Elimina cualquier objeto de jerarquía (un grupo de secciones, sección o página) de la jerarquía del bloc de notas de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Parámetros** <br/> | _bstrObjectID_ &ndash; La id. de OneNote del objeto que deseas eliminar. El objeto puede ser un grupo de secciones, sección o página.  <br/><br/>_dateExpectedLastModified_ &ndash; (opcional) La fecha y hora en que crees que se modificó por última vez el objeto que deseas eliminar. Si pasas un valor distinto de cero para este parámetro, OneNote lleva a cabo la actualización solo si el valor que se pasa coincide con la fecha y hora reales en que se modificó por última vez el objeto. Pasar un valor para este parámetro impide sobrescribir accidentalmente ediciones realizadas por los usuarios desde la última vez que se modificó el objeto.  <br/><br/>_deletePermanently_ &ndash; (opcional) **verdadero** para eliminar permanentemente el contenido; **falso** para mover el contenido a la papelera de reciclaje de OneNote para el bloc de notas correspondiente (predeterminado). Si el bloc de notas está en formato de OneNote 2007, no existe una papelera de reciclaje, por lo que el contenido se elimina de forma permanente.  <br/> |
   
### <a name="createnewpage-method"></a>Método CreateNewPage

|||
|:-----|:-----|
|**Descripción** <br/> |Agrega una nueva página a la sección que especifiques. La página nueva se agregará como la última página de la sección  <br/> |
|**Sintaxis** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Parámetros** <br/> | _bstrSectionID_ &ndash; Una cadena que contiene la id. de OneNote de la sección donde deseas crear la nueva página.  <br/><br/>_pbstrPageID_ &ndash; (parámetro de salida) Un puntero de la cadena en la que el método escribe la id. de OneNote para la página recién creada.  <br/><br/>_npsNewPageStyle_ &ndash; Un valor de la enumeración **NewPageStyle** que especifica el estilo de la página que se debe crear.  <br/> |
   
La API de OneNote incluye el método **CreateNewPage** como comodidad. Puedes lograr el mismo resultado, con mayor control sobre el lugar que ocupa la página nueva en la jerarquía, mediante una llamada al método **UpdateHierarchy**. El método **UpdateHierarchy** también te permite crear subpáginas al mismo tiempo que creas una nueva página. 
  
### <a name="closenotebook-method"></a>Método CloseNotebook

|||
|:-----|:-----|
|**Descripción** <br/> |Cierra el bloc de notas especificado.  <br/> |
|**Sintaxis** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Parámetros** <br/> | _bstrNotebookID_ &ndash; La id. de OneNote del bloc de notas que quieres cerrar.  <br/><br/>_forzar_ &ndash; (opcional) **verdadero** para cerrar el bloc de notas, incluso si hay cambios en el bloc de notas que OneNote no puede sincronizar antes de cerrar; en caso contrario, **falso** (predeterminado).  <br/> |
   
Puedes usar el método **CloseNotebook** para cerrar el bloc de notas que especifiques. Cuando llamas a este método, OneNote sincroniza los archivos sin conexión con el contenido del bloc de notas actual, si es necesario y, a continuación, cierra el bloc de notas especificado. Cuando regresa el método, el bloc de notas ya no aparece en la lista de blocs de notas abiertos en la interfaz de usuario (IU) de OneNote. 
  
### <a name="gethierarchyparent-method"></a>Método GetHierarchyParent

|||
|:-----|:-----|
|**Descripción** <br/> |Obtiene la id. de OneNote para el objeto primario de un objeto de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Parámetros** <br/> | _bstrObjectID_ &ndash; Una cadena que contiene la id. de OneNote del objeto del que desea encontrar un objeto primario.  <br/><br/>_pbstrParentID_ &ndash; (parámetro de salida) Un puntero de la cadena en la que el método escribe la id. de OneNote para el objeto primario.  <br/> |
   
Si el objeto de OneNote no tiene ningún objeto primario (por ejemplo, cuando un usuario desea obtener el elemento primario de un bloc de notas), se produce una excepción.
  
### <a name="getspeciallocation-method"></a>Método GetSpecialLocation

|||
|:-----|:-----|
|**Descripción** <br/> |Busca la ruta a la ubicación donde OneNote almacena determinados elementos especiales, como copias de seguridad, notas sin archivar y el bloc de notas predeterminado.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Parámetros** <br/> | _slToGet_ &ndash; Uno de los valores de enumeración [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) que especifica la ubicación de carpeta especial que se debe obtener.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; (parámetro de salida) Un puntero de la cadena en la que deseas que OneNote escriba la ruta de la carpeta especial.  <br/> |
   
Puedes usar este método para determinar la ubicación en disco de la carpeta Notas sin archivar. Es la carpeta en la que OneNote almacena las notas que se crean al arrastrar un elemento en OneNote, así como las notas que se incluyen directamente desde otras aplicaciones (como las que se generan al hacer clic en **Enviar a OneNote** en Microsoft Outlook o Microsoft Internet Explorer). 
  
## <a name="page-content-methods"></a>Métodos de contenido de página
<a name="ON14DevRef_Application_PageContent"> </a>

Los métodos descritos en esta sección te permiten descubrir, actualizar y eliminar el contenido en las páginas de los blocs de notas de OneNote, así como publicar contenido en OneNote.
  
### <a name="getpagecontent-method"></a>Método GetPageContent

|||
|:-----|:-----|
|**Descripción**|Obtiene todo el contenido (en formato XML de OneNote) de la página especificada.|
|**Sintaxis**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Parámetros**| _bstrPageId_ &ndash; La id. de OneNote de la página cuyo contenido que deseas obtener.<br/><br/>_pbstrPageXmlOut_ &ndash; (parámetro de salida) Un puntero para la cadena en la que deseas que OneNote escriba el resultado de XML.<br/><br/>_pageInfoToExport_ &ndash; (opcional) Especifica si el método **GetPageContent** devuelve contenido binario, incrustado en el código XML y codificado con base 64. El contenido binario puede incluir, por ejemplo, imágenes y datos de entrada de lápiz. El parámetro _pageInfoToExport_ también especifica si se debe marcar la selección en el código XML que devuelve el método **GetPageContent**. Toma un valor enumerado de la enumeración [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo).<br/><br/>_xsSchema_ &ndash; (opcional) La versión del esquema XML de OneNote, del tipo **XMLSchema**, que quieres que sea el resultado. Puedes especificar si deseas el esquema XML versión 2013, 2010, 2007 o la versión actual. <br/><br/>**NOTA**: Te recomendamos que especifiques una versión de OneNote (como **xs2013**) en lugar de usar **xsCurrent** o dejar en blanco, ya que esto le permitirá a tu complemento trabajar con versiones futuras de OneNote.           |
   
De forma predeterminada, para evitar el exceso de longitud de la cadena XML que devuelve, OneNote no inserta contenido binario en el código XML. Por el mismo motivo, no marca la selección actual con los atributos de la selección. Los objetos binarios incluyen una id. de OneNote en sus etiquetas. Para obtener un objeto binario, llamas al método **GetBinaryPageContent** y pasas la id. de OneNote que obtienes del método **GetPageContent**. Usas el método **GetPageContent** cuando no necesitas los datos binarios inmediatamente. 
  
### <a name="updatepagecontent-method"></a>Método UpdatePageContent

|||
|:-----|:-----|
|**Descripción**|Actualiza o modifica el contenido en la página.|
|**Sintaxis**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Parámetros**| _bstrPageChangesXmlIn_ &ndash; Una cadena que contiene el código XML de OneNote que incluye los cambios que deseas realizar en la página.<br/><br/>_dateExpectedLastModified_ &ndash; (opcional) La fecha y hora en la que crees que se modificó por última vez la página que deseas actualizar. Si pasas un valor distinto de cero para este parámetro, OneNote lleva a cabo la actualización solo si el valor que se pasa coincide con la fecha y hora reales en que se modificó por última vez la página. Pasar un valor para este parámetro impide sobrescribir accidentalmente ediciones realizadas por los usuarios desde la última vez que se modificó la página.<br/><br/>_xsSchema_ &ndash; (opcional) La versión del esquema XML de OneNote, del tipo **XMLSchema**, que quieres que sea el resultado. Puedes especificar si deseas el esquema XML versión 2013, 2010, 2007, o la versión actual. <br/><br/>**NOTA**: Te recomendamos que especifiques una versión de OneNote (como **xs2013**) en lugar de usar **xsCurrent** o dejar en blanco, ya que esto le permitirá a tu complemento trabajar con versiones futuras de OneNote.<br/><br/>_forzar_(opcional) **verdadero** para actualizar el contenido de la página, incluso si hay datos desconocidos en la página de una versión futura de OneNote; en caso contrario, **falso** (predeterminado). |
   
Puedes usar este método para modificar la página de varias formas. Por ejemplo, puedes usar el método **UpdatePageContent** para agregar un esquema a una página, cambiar el contenido de un esquema, agregar imágenes, agregar entradas de lápiz, mover contenido o modificar texto en contornos. 
  
Como un ejemplo más específico, puedes usar el método **GetPageContent** para exportar una página existente, realizar algunos cambios en el código XML de la página y, después, usar el método **UpdatePageContent** para importar toda la página nuevamente. O bien, puedes usar este método para agregar nuevos objetos de página, como imágenes, en la parte inferior de una página existente. 
  
Los únicos objetos que debes incluir en el código XML que pasas al método **UpdatePageContent** son objetos de nivel de página (por ejemplo, esquemas, imágenes en la página o entrada de lápiz en la página) que cambiaron. Este método no modifica ni quita objetos de nivel de página que no se especifican en el parámetro _bstrPageChangesXmlIn_. El método reemplaza por completo los objetos de nivel de página, como esquemas cuyas id. coinciden con las de los objetos que pasas. Por lo tanto, debes especificar completamente todos los objetos de nivel de página en tu código, incluidos los contenidos existentes y los cambios que deseas hacerles. 
  
Por ejemplo, si tu página contiene un esquema y una imagen de fondo de página, puedes reemplazar el esquema y dejar la imagen sin modificar al especificar el esquema en el código XML, usando la id. del esquema existente y no incluyendo la imagen en el código. Como el esquema revisado que incluyes en el código reemplaza completamente el esquema existente, debes incluir todo el contenido del esquema.
  
Además, el método **UpdatePageContent** modifica solo propiedades de elementos que especificas en el parámetro _bstrPageChangesXmlIn_. Por ejemplo, si especificas algunas (pero no todas) las propiedades del elemento **PageSettings**, las propiedades que no se especifican permanecen sin cambios. 
  
El ejemplo siguiente muestra cómo usar el método **UpdatePageContent** para cambiar el título de una página y agregar texto de ejemplo a la página. Antes de ejecutar el código, sustituye una id. de página válida para la id. de la página que se muestra en el código, para que el código funcione en tu equipo. Para obtener la id. de la página, usa el método **GetHierarchy** y examina los resultados. 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"https://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
            ID=\"{3428B7BB-EF39-4B9C-A167-3FAE20630C37}{1}{B0}\">" +
            "    <one:PageSettings RTL=\"false\" color=\"automatic\">" +
            "        <one:PageSize>" +
            "            <one:Automatic/>" +
            "        </one:PageSize>" +
            "        <one:RuleLines visible=\"false\"/>" +
            "    </one:PageSettings>" +
            "    <one:Title style=\"font-family:Calibri;
                 font-size:17.0pt\" lang=\"en-US\">" +
            "        <one:OE alignment=\"left\">" +
            "            <one:T>" +
            "                <![CDATA[My Sample Page]]>" +
            "            </one:T>" +
            "        </one:OE>" +
            "    </one:Title>" +
            "    <one:Outline >" +
            "        <one:Position x=\"120\" y=\"160\"/>" +
            "        <one:Size width=\"120\" height=\"15\"/>" +
            "        <one:OEChildren>" +
            "            <one:OE alignment=\"left\">" +
            "                <one:T>" +
            "                    <![CDATA[Sample Text]]>" +
            "                </one:T>" +
            "            </one:OE>" +
            "        </one:OEChildren>" +
            "    </one:Outline>" +
            "</one:Page>";
        // Update the page content.
        onApplication.UpdatePageContent(strImportXML, System.DateTime.MinValue);
    }

```

### <a name="getbinarypagecontent-method"></a>Método GetBinaryPageContent

|||
|:-----|:-----|
|**Descripción** <br/> |Devuelve un objeto binario, como entradas en lápiz o imágenes, en una página de OneNote como una cadena codificada con base 64.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Parámetros** <br/> | _bstrPageID_ &ndash; La id. de OneNote de la página que contiene el objeto binario que se debe obtener.  <br/><br/>_bstrCallBackID_ &ndash; La id. de OneNote del objeto binario que deseas obtener. Esta id., conocida como **callbackID**, está en el código XML de OneNote de una página devuelta por el método **GetPageContent**.  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; (parámetro de salida) Un puntero de una cadena en la que OneNote escribe el objeto binario como una cadena codificada con base 64.  <br/> |
   
### <a name="deletepagecontent-method"></a>Método DeletePageContent

|||
|:-----|:-----|
|**Descripción** <br/> |Elimina un objeto &ndash; como **Esquema**, **Lápiz** o **Imagen** de una página.  <br/> |
|**Sintaxis** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Parámetros** <br/> | _bstrPageID_ &ndash; La id. de OneNote de la página que contiene el objeto binario que se debe eliminar.  <br/><br/>_bstrObjectID_ &ndash; La id. de OneNote del objeto que deseas eliminar.  <br/><br/>_dateExpectedLastModified_ &ndash; (opcional) La fecha y hora en que crees que se modificó por última vez la página con contenido que deseas eliminar. Si pasas un valor distinto de cero para este parámetro, OneNote lleva a cabo la eliminación solo si el valor que se pasa coincide con la fecha y hora reales en que se modificó por última vez la página. Pasar el valor por este parámetro impide sobrescribir accidentalmente ediciones realizadas por los usuarios desde la última vez que se modificó la página.  <br/><br/>_forzar_ &ndash; (opcional) **verdadero** para actualizar el contenido de la página, incluso si hay datos desconocidos en la página de una versión futura de OneNote; en caso contrario, **falso** (predeterminado).  <br/> |
   
### <a name="publish-method"></a>Método Publish

|||
|:-----|:-----|
|**Descripción** <br/> |Exporta la página que especificas a un archivo en cualquier formato compatible con OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Parámetros** <br/> | _bstrHierarchyID_ &ndash; La id. de OneNote de la jerarquía que deseas exportar.  <br/><br/>_bstrTargetFilePath_ &ndash; La ruta absoluta a la ubicación donde quieres guardar el archivo de salida resultante. El archivo que especifiques no debe ser uno que ya exista en esa ubicación.  <br/><br/>_pfPublishFormat_ &ndash; Uno de los valores de enumeración [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) que especifica el formato en que deseas que esté la página publicada (por ejemplo, MHTML, PDF, etc.).  <br/><br/>_bstrCLSIDofExporter_ &ndash; La id. de clase (CLSID) de una aplicación COM registrada que puede exportar metarchivos Microsoft Windows mejorados (.emf). La aplicación COM debe implementar la interfaz **IMsoDocExporter**. Este parámetro se incluye para permitir que los desarrolladores de terceros escriban su propio código para publicar contenido de OneNote en un formato personalizado. Para más información sobre la interfaz **IMsoDocExporter**, consulta [Ampliar la característica de exportación de formato fijo de Office 2007](https://msdn.microsoft.com/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
Actualmente, OneNote admite los siguientes formatos de archivo:
  
- Archivos MHTML (.mht)
- Archivos PDF de Adobe Acrobat (.pdf)
- Archivos XML Paper Specification (XPS) (.xps)
- Archivos OneNote 2013, 2010 o 2007 (.one)
- Archivos OneNote Package (onepkg)
- Documentos de Microsoft Word (.doc o .docx)
- Metarchivos Microsoft Windows mejorados (.emf)
- Archivos HTML (.html)
    
Este método produce los mismos resultados que obtendrías al hacer clic en **Publicar** en la IU y especificar el formato. 
  
## <a name="navigation-methods"></a>Métodos de navegación
<a name="ON14DevRef_Application_Navigation"> </a>

Los métodos descritos en esta sección te permiten buscar, desplazarte y vincularte a los blocs de notas, grupos de secciones, secciones, páginas y objetos de la página de OneNote.
  
### <a name="navigateto-method"></a>Método NavigateTo

|||
|:-----|:-----|
|**Descripción** <br/> |Se dirige a un objeto (por ejemplo, secciones, páginas y elementos de **Esquema** dentro de las páginas).  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parámetros** <br/> | _bstrHierarchyObjectID_ &ndash; La id. de OneNote del objeto al que deseas desplazarte en la jerarquía de OneNote.  <br/><br/>_bstrObjectID_ &ndash; La id. de OneNote del objeto al que deseas desplazarte en la página de OneNote.  <br/><br/>_fNewWindow_ &ndash; (opcional) **verdadero** Abre un objeto especificado en una nueva ventana de OneNote. **falso** No se abre una nueva ventana de OneNote si ya hay una abierta.  <br/> |
   
### <a name="navigatetourl-method"></a>Método NavigateToUrl

|||
|:-----|:-----|
|**Descripción** <br/> |Si se pasó un vínculo de OneNote (onenote://), se abrirá la ventana de OneNote en la ubicación correspondiente en OneNote. Si el vínculo es externo a OneNote (como https:// o file://), aparecerá un cuadro de diálogo de seguridad. Tras el descarte, OneNote intenta abrir el vínculo y se devuelve un error **HResult.hrObjectDoesNotExist**.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parámetros** <br/> | _bstrUrl_ &ndash; Una cadena que indica hacia dónde ir. Esta podría ser un vínculo de OneNote o cualquier otra dirección URL, como una ubicación de red o vínculo web.  <br/><br/>_fNewWindow_ &ndash; (opcional) **verdadero** Abre una dirección URL especificada en una nueva ventana de OneNote. **falso** No se abre una nueva ventana de OneNote si ya hay una abierta.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>Método GetHyperLinkToObject

|||
|:-----|:-----|
|**Descripción** <br/> |Obtiene un hipervínculo de OneNote para el bloc de notas especificado, grupo de secciones, sección, página u objeto de página.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parámetros** <br/> | _bstrHierarchyID_ &ndash; La id. de OneNote para el bloc de notas, grupo de secciones, sección o página para el que deseas un hipervínculo.  <br/><br/>_bstrPageContentObjectID_ &ndash; (opcional) La id. de OneNote del objeto dentro de la página para el que deseas un hipervínculo. Por ejemplo, el objeto puede ser un esquema o elemento de **Esquema**. Si pasas una cadena vacía (""), el vínculo devuelto apunta al bloc de notas, grupo de secciones, sección o página que se especificaste en el parámetro _bstrHierarchyID_. Si pasas una cadena no vacía para el parámetro _bstrPageContentObjectID_, el parámetro _bstrHierarchyID_ debe ser una referencia a la página que contiene el objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (parámetro de salida) Puntero de una cadena en la que el método **GetHyperlinkToObject** escribe el texto del hipervínculo de salida.  <br/> |
   
Cuando intentas ir al vínculo resultante, OneNote se abre y muestra el objeto especificado en el navegador.
  
### <a name="getwebhyperlinktoobject-method"></a>Método GetWebHyperlinktoObject

|||
|:-----|:-----|
|**Descripción** <br/> |Devuelve un hipervínculo a un objeto que se abre en el cliente web de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parámetros** <br/> | _bstrHierarchyID_ &ndash; La id. de OneNote para el bloc de notas, grupo de secciones, sección o página para el que deseas un hipervínculo web.  <br/><br/>_bstrPageContentObjectID_ &ndash; (opcional) La id. de OneNote del objeto dentro de la página para el que deseas un hipervínculo. Por ejemplo, el objeto puede ser un esquema o elemento de **Esquema**. Si pasas una cadena vacía (""), el vínculo devuelto apunta al bloc de notas, grupo de secciones, sección o página que especificaste en el parámetro _bstrHierarchyID_. Si pasas una cadena no vacía para el parámetro _bstrPageContentObjectID_, el parámetro _bstrHierarchyID_ debe ser una referencia a la página que contiene el objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (parámetro de salida) Puntero de una cadena en la que la que el método **GetWebHyperlinkToObject** escribe el texto de hipervínculo de salida. Si no se puede crear un hipervínculo web para el bloc de notas, se devuelve un valor nulo.  <br/> |
   
### <a name="findpages-method"></a>Método FindPages

|||
|:-----|:-----|
|**Descripción**|Devuelve una lista de páginas que coinciden con el término de consulta especificado.|
|**Sintaxis**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parámetros**| _bstrStartNodeID_ &ndash; El nodo (raíz, bloc de notas, grupo de sección o sección) debajo del cual se debe buscar contenido. Este parámetro establece el alcance de la búsqueda.<br/><br/>_bstrSearchString_ &ndash; La cadena de búsqueda. Pasa exactamente la misma cadena que escribirías en el cuadro de búsqueda de la IU de OneNote. Puedes usar operadores bit a bit, como **Y** y **O**, que deben estar en mayúsculas.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (parámetro de salida) Un puntero a una cadena en la que deseas que OneNote escriba la cadena de resultado de XML. La cadena XML resultante contiene la jerarquía de bloc de notas desde la raíz hacia abajo, e incluso las páginas que coinciden con la cadena de búsqueda. Por ejemplo, el método **FindPages** no enumera las secciones que no tengan página coincidentes en la jerarquía. Además, si solo hay una página en una única sección que coincide con la cadena, la jerarquía devuelta incluye la ruta a esa página y sección, pero a ninguna otra parte de la jerarquía del bloc de notas.<br/><br/>_fIncludeUnindexedPages_ &ndash; (opcional) **verdadero** para las páginas de búsqueda que no fueron indexadas por Windows Search; en caso contrario, **falso**.<br/><br/>_fDisplay_ &ndash; (opcional) **verdadero** para ejecutar la búsqueda en la IU para el usuario, del mismo modo que si el usuario lo hubiera escrito por su cuenta. **falso** para realizar la consulta sin cambios en la IU (predeterminado).<br/><br/>_xsSchema_ &ndash; (opcional) La versión del esquema de OneNote de la cadena _pbstrHierarchyXmlOut_. Este valor opcional se usa para especificar la versión del esquema XML de OneNote que contiene la cadena _pbstrHierarchyXmlOut_. Si no se especifica este valor, OneNote supondrá que el archivo XML se encuentra en la versión del esquema _xsCurrent_. <br/><br/>**NOTA**: Te recomendamos que especifiques una versión de OneNote (como **xs2013**) en lugar de usar **xsCurrent** o dejar en blanco, ya que esto le permitirá a tu complemento trabajar con versiones futuras de OneNote.           |
   
 **FindPages** funciona únicamente si tienes Búsqueda de Microsoft 3.0 o 4.0 instalado en tu equipo. Windows Vista y Windows 7 incluyen este componente. Sin embargo, si estás ejecutando una versión anterior de Windows, tendrás que instalar [Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para **FindPages** para trabajar. 
  
### <a name="findmeta-method"></a>Método FindMeta

|||
|:-----|:-----|
|**Descripción**|Devuelve una lista de objetos de OneNote que contienen metadatos que coinciden con el término de consulta especificado.|
|**Sintaxis**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parámetros**| _bstrStartNodeID_ &ndash; El nodo (raíz, bloc de notas, grupo de sección o sección) debajo del cual se debe buscar contenido. Este parámetro establece el alcance de la búsqueda.<br/><br/>_bstrSearchStringName_ &ndash; La cadena de búsqueda. Pasar cualquier parte del nombre de metadatos. Si pasas una cadena vacía o un valor nulo, todos los objetos que tengan metadatos coincidirán con la consulta.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (parámetro de salida) Un puntero a una cadena en la que deseas que OneNote escriba la cadena de resultado de XML. La cadena XML resultante contiene la jerarquía del bloc de notas desde la raíz hacia abajo, e incluso las páginas que coinciden con la cadena de búsqueda. Por ejemplo, el método **FindPages** no enumera las secciones que no tengan página coincidentes en la jerarquía. Además, si solo hay una página en una única sección que coincide con la cadena, la jerarquía devuelta incluye la ruta a esa página y sección, pero a ninguna otra parte de la jerarquía del bloc de notas.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (opcional) **verdadero** para las páginas de búsqueda que no fueron indexadas por Windows Search; en caso contrario, **falso**.<br/><br/>_xsSchema_ &ndash; (opcional) La versión del esquema de OneNote de la cadena _pbstrHierarchyXmlOut_. Este valor opcional se usa para especificar la versión del esquema XML de OneNote que contiene la cadena _pbstrHierarchyXmlOut_. Si no se especifica este valor, OneNote supondrá que el archivo XML se encuentra en la versión del esquema _xsCurrent_. <br/><br/>**NOTA**: Te recomendamos que especifiques una versión de OneNote (como **xs2013**) en lugar de usar **xsCurrent** o dejar en blanco, ya que esto le permitirá a tu complemento trabajar con versiones futuras de OneNote.           |
   
**FindMeta** funciona únicamente si tienes Microsoft Windows Search 3.0 o 4.0 instalado en tu equipo. Windows Vista y Windows 7 incluyen este componente. Sin embargo, si estás ejecutando una versión anterior de Windows, tendrás que instalar [Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para **FindMeta** para trabajar. 
  
## <a name="functional-methods"></a>Métodos de funciones
<a name="ON14DevRef_Application_Functional"> </a>

Los métodos descritos en esta sección te permiten realizar ciertas acciones o establecer parámetros dentro de la aplicación de OneNote.
  
### <a name="mergefiles-method"></a>Método MergeFiles

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios combinar los cambios del mismo archivo en uno. Para que los archivos puedan considerarse iguales, deben tener la misma id. de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Parámetros** <br/> | _bstrBaseFile_ &ndash; La cadena de ruta a la ubicación del archivo .one del estado inicial del archivo.  <br/><br/>_bstrClientFile_ &ndash; La cadena de ruta a la ubicación del archivo .one del segundo conjunto de cambios que se combinarán con el archivo de base después de que los cambios de archivo del servidor se combinan con la base.  <br/><br/>_bstrServerFile_ &ndash; La cadena de ruta a la ubicación del archivo .one del primer conjunto de cambios que se combinarán con el archivo de base.  <br/><br/>_bstrBaseFile_ &ndash; La cadena de ruta a la ubicación del archivo .one con los cambios combinados.  <br/> |
   
El método **MergeFiles** se diseñó para escenarios móviles en los que pueden existir varias versiones de un archivo OneNote. 
  
### <a name="mergesections-method"></a>Método MergeSections

|||
|:-----|:-----|
|**Descripción** <br/> |Combina el contenido de una sección con otra en OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Parámetros** <br/> | _bstrSectionSourceId_ &ndash; La id. de OneNote de la sección que se va a combinar.  <br/><br/>_bstrSectionSourceId_ &ndash; La id. de OneNote de la sección con la que se va a combinar. La sección de origen se combinará con esta sección de destino.  <br/> |
   
Este método realiza la misma operación que la característica **Combinar en otra sección**que está visible cuando haces clic con el botón derecho en una sección. 
  
### <a name="quickfiling-method"></a>Método QuickFiling

|||
|:-----|:-----|
|**Descripción** <br/> |Devuelve una instancia del cuadro de diálogo [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog), que se puede usar para seleccionar una ubicación dentro del árbol de la jerarquía de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>Método SyncHierarchy

|||
|:-----|:-----|
|**Descripción** <br/> |Fuerza a OneNote a sincronizar un objeto específico con el archivo de origen en el disco.  <br/> |
|**Sintaxis** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Parámetros** <br/> | _bstrHierarchyID_ &ndash; La id. de OneNote del objeto que debe sincronizarse.  <br/> |
   
### <a name="setfilinglocation-method"></a>Método SetFilingLocation

|||
|:-----|:-----|
|**Descripción** <br/> |Los usuarios pueden especificar dónde y cómo se deben archivar determinados tipos de contenido en OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Parámetros** <br/> | _flToSet_ &ndash; El tipo de objeto de la ubicación de archivado que se debe establecer.  <br/><br/>_fltToSet_ &ndash; La ubicación en la que se debe archivar el tipo.  <br/><br/>_bstrFilingSectionID_ &ndash; La id. de OneNote de la sección o página en la que deseas establecer la ubicación. Si no es aplicable, el usuario puede pasar un valor nulo o una cadena vacía.  <br/> |
   
Los tipos de contenido que se puede archivar incluyen los elementos de Outlook y notas web de Internet Explorer que se importan a OneNote a través del comando **Enviar a OneNote** en cada aplicación. Con este método, también se puede establecer la ubicación de archivado de elementos que se imprimen en OneNote. 
  
## <a name="properties"></a>Propiedades
<a name="ON14DevRef_Application_Properties"> </a>

Esta sección describe las propiedades de la interfaz de la **Aplicación**. 
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|**Windows** <br/> |Proporciona a los usuarios acceso a ventanas de OneNote abiertas. Esta propiedad permite a los usuarios enumerar el conjunto de ventanas de OneNote y modificar algunas propiedades de la ventana. Para obtener más información, consulta [Interfaces de Windows](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Devuelve la colección **COMAddIns** de OneNote. Esta colección contiene todos los complementos COM que están disponibles para OneNote. La propiedad **Recuento** de la colección **COMAddins** devuelve el número de complementos COM disponibles. Para obtener más información, consulta el objeto [COMAddIns](https://msdn.microsoft.com/library/office/ff865489.aspx).  <br/> |
|**LanguageSettings** <br/> |Te permite tener acceso a algunas API para cambiar la configuración de idioma común de OneNote.  <br/> |
   
## <a name="events"></a>Eventos
<a name="ON14DevRef_Application_Events"> </a>

Esta sección describe los eventos de la interfaz de la Aplicación.
  
> [!CAUTION]
> Los eventos actualmente no se pueden agregar en código administrado. 
  
### <a name="onnavigate-event"></a>Evento OnNavigate

|||
|:-----|:-----|
|**Descripción** <br/> |Permite al usuario asignar una función que se puede llamar cuando la IU de OneNote se desplazó fuera de la ubicación actual de OneNote.  <br/> |
|**Sintaxis** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>Método OnHierarchyChange

|||
|:-----|:-----|
|**Descripción** <br/> |Permite al usuario asignar una función que se puede llamar cada vez que cambie la jerarquía de OneNote (por ejemplo, agregar o eliminar páginas o mover secciones). Los cambios en la jerarquía se realizan por lotes, por lo que si ocurren varios cambios a la vez o casi a la vez, OneNote eleva el evento una vez.  <br/> |
|**Sintaxis** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Parámetros** <br/> | _bstrActivePageID_ &ndash; Pasa la id. de OneNote de la página activa.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

