---
title: Interfaz de aplicación (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'La interfaz de aplicación incluye métodos ayuda recuperar, manipular y actualizar el contenido y la información de OneNote. Los métodos se encuentran en cuatro categorías generales:'
ms.openlocfilehash: 25bb1aa570f6c36aa04140d9256d277bee65152b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816032"
---
# <a name="application-interface-onenote"></a>Interfaz de aplicación (OneNote)

La interfaz de **aplicación** incluye métodos ayuda recuperar, manipular y actualizar el contenido y la información de OneNote. Los métodos se encuentran en cuatro categorías generales: 
  
- **Estructura de Bloc de notas** &ndash; Métodos para trabajar con la estructura del Bloc de notas, los referentes a descubrir, abrir, modificar, cerrar y eliminar los blocs de notas, grupos de secciones y secciones incluidos. 
    
- **Contenido de la página** &ndash; Métodos para trabajar con páginas y contenido de la página, los referentes a descubrir, modificar, guardar y eliminar contenido de la página incluidos. Contenido de la página incluye los objetos binarios, como imágenes y la entrada de lápiz y objetos de texto, como contornos. 
    
- **Navegación** &ndash; Métodos para buscar, vincular a y navegar a las páginas y objetos. 
    
- **Funcional** &ndash; Todos los otros métodos que realizan algunas acciones o establecer parámetros en OneNote. 
    
Además, la interfaz de **aplicación** incluye un número de *Propiedades* y *eventos* . 
  
## <a name="notebook-structure-methods"></a>Métodos de estructura de Bloc de notas
<a name="ON14DevRef_Application_NotebookStructure"> </a>

Los métodos descritos en esta sección permiten descubrir, abrir, modificar, cerrar y eliminación blocs de notas de OneNote, grupos de secciones y secciones.
  
### <a name="gethierarchy-method"></a>GetHierarchy (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Obtiene el Bloc de notas nodo estructura de la jerarquía, empezando en el nodo que especifique (todos los blocs de notas o un bloc de notas único, grupo de sección o sección) y extender hacia abajo en todos los descendientes en el nivel que especifique.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Parameters** <br/> | _bstrStartNodeID_ &ndash; El nodo (Bloc de notas, el grupo de sección o sección) cuyos descendientes que desee. Si se pasa una cadena nula (""), el método obtiene todos los nodos debajo del nodo raíz (es decir, todos los blocs de notas, grupos de secciones y secciones). Si especifica un bloc de notas, el grupo de la sección o el nodo de la sección, el método obtiene a sólo los descendientes de dicho nodo.  <br/><br/>_hsScope_ &ndash; El nivel de nodo descendiente más bajo que desee. Por ejemplo, si especifica las páginas, el método obtiene todos los nodos en la medida hacia abajo como el nivel de página. Si se especifica en las secciones, el método obtiene sólo los nodos de sección debajo el Bloc de notas. Para obtener más información, vea la enumeración **HierarchyScope** en el tema de [las enumeraciones](enumerations-onenote-developer-reference.md#odc_HierarchyScope) .  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; Puntero de A (parámetro de salida) a la cadena en la que desea que OneNote para escribir el resultado XML.  <br/><br/>_xsSchema_ &ndash; (Opcional) la versión del esquema XML de OneNote, del tipo **XMLSchema**, que desea que el resultado. Puede especificar si desea que el esquema XML versión 2013, 2010, 2007, o la versión actual.  <br/><br/>**Nota**: se recomienda especificar una versión de OneNote (por ejemplo, **xs2013**) en lugar de usar **xsCurrent** o déjelo en blanco, ya que esto le permitirá el complemento para que funcione con las futuras versiones de OneNote.           |
   
El método GetHierarchy devuelve que una cadena en formato de OneNote 2013 XML de forma predeterminada o puede establecer la versión del esquema XML preferida mediante el parámetro opcional _xsSchema_ . 
  
Dependiendo de los parámetros que se pasa, el método **GetHierarchy** puede devolver varias listas (por ejemplo, todos los blocs de notas, todas las secciones de todos los blocs de notas, todas las páginas de una sección determinada o todas las páginas de un bloc de notas determinada). Para cada nodo, la cadena XML devuelta proporciona propiedades (por ejemplo, el título de sección o página, identificador y hora de última modificación). 
  
No todas las combinaciones de nodo de inicio y ámbito son válidas. Por ejemplo, si especifica una sección de inicio nodo y un ámbito de Bloc de notas, **GetHierarchy** devuelve un resultado null porque es superior en la jerarquía de nodos de una sección de un bloc de notas. 
  
En el ejemplo de C# siguiente se muestra cómo usar el método **GetHierarchy** para obtener toda la jerarquía de OneNote, incluidos todos los blocs de notas, hacia abajo hasta el nivel de página. La cadena de salida copia en el Portapapeles, desde el que puede pegar la cadena en un editor de texto para su revisión. 
  
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

### <a name="updatehierarchy-method"></a>UpdateHierarchy (método)

|||
|:-----|:-----|
|**Descripción**|Modifica o actualiza la jerarquía de los blocs de notas. Por ejemplo, puede agregar secciones o grupos de sección en un bloc de notas, agregue un nuevo bloc de notas, mover secciones dentro de un bloc de notas, cambie el nombre de una sección, agregar páginas a una sección o cambiar el orden de las páginas de secciones.|
|**Sintaxis**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Parameters**| _bstrChangesXmlIn_ &ndash; Una cadena que contiene el código XML de OneNote que se especifica para realizar los cambios en la jerarquía. Por ejemplo, si desea insertar una sección nueva, puede agregar un elemento de la **sección** en la cadena XML para indicar donde desea que se agrega la nueva sección. Como alternativa, si desea cambiar el nombre de una sección existente, puede mantener el mismo identificador de sección y cambie su **nombre** de atributo en el código XML.<br/><br/>_xsSchema_ &ndash; (Opcional) el OneNote versión del esquema de la cadena _bstrChangesXmln_. Este valor opcional se utiliza para especificar la versión del esquema XML de OneNote que se encuentra en la cadena de _bstrChangesXmlIn_ . Si no se especifica este valor, OneNote se supone que el XML se encuentra en la versión de esquema _xsCurrent_. <br/><br/>**Nota**: se recomienda especificar una versión de OneNote (por ejemplo, **xs2013**) en lugar de usar **xsCurrent** o déjelo en blanco, ya que esto le permitirá el complemento para que funcione con las futuras versiones de OneNote.           |
   
Si se pasa únicamente una cadena parcial de OneNote XML para el parámetro _bstrChangesXmlIn_ , OneNote intenta deducir los cambios que desee. Por ejemplo, si se incluye un elemento de **Bloc de notas** que contiene sólo una sección, OneNote agrega la sección después de todas las secciones existentes. Sin embargo, si la operación que especifique es ambigua, el resultado puede ser difícil determinar. Por ejemplo, si un bloc de notas existente contiene cuatro secciones, y la cadena XML que pasa incluye el Bloc de notas y sólo las secciones primera y cuarta (en ese orden), OneNote puede colocar las secciones de segunda y tercer antes de la cuarta sección o después de la primera sección . 
  
No puede usar el método **UpdateHierarchy** para eliminar una parte de un bloc de notas. Es decir, pasando una cadena XML que incluye sólo una parte de una jerarquía existente no elimina las secciones que no se incluyen en la cadena. Para eliminar parte de una jerarquía, use el método **DeleteHierarchy** . 
  
El siguiente código de C#, muestra una forma de usar el método **UpdateHierarchy** para cambiar la jerarquía de OneNote, cambiando el nombre de una sección existente. Lee código XML desde un archivo de ejemplo denominado ChangeSectionName.xml en la raíz de la unidad C, lo carga en un documento XML y, a continuación, se pasa la estructura XML de dicho documento al método. 
  
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

El siguiente código XML es un fragmento del archivo ChangeSectionName.xml que el código de C# anterior se pasa al método. Cuando el código XML se pasa al método **UpdateHierarchy** , cambia el nombre de una de las secciones de la jerarquía existente (cambiando el valor del atributo **name** a mi nombre se ha cambiado sección""). A continuación, quita todas las secciones, excepto la cuyo nombre se ha cambiado. Además, el código elimina los atributos innecesarios del elemento de la **sección** destino, incluidos los atributos **lastModifiedTime**, **isCurrentlyViewed**y **color** , dejando el **nombre**, **identificador**y ** ruta de acceso** atributos intactos. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

El código XML anterior se obtuvo mediante el código que se muestra en el ejemplo para el método **GetHierarchy** , que se modifica, como se indica a continuación, para limitar el ámbito a las secciones. 
  
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

En el ejemplo de C# siguiente se muestra una aplicación de consola completa que busca en una sección denominada " `Sample_Section`", solicita al usuario que escriba un nuevo nombre para la sección y, a continuación, usa el método **UpdateHierarchy** para cambiar el nombre de la sección en el nombre que el usuario ha escrito. Antes de ejecutar el código, cambie " `Sample_Section`" en el nombre de una sección que se encuentra en la jerarquía de OneNote.
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "http://schemas.microsoft.com/office/onenote/2013/onenote";
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

### <a name="openhierarchy-method"></a>OpenHierarchy (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Se abre un grupo de secciones o una sección que especifique.  <br/> |
|**Sintaxis** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Parameters** <br/> | _bstrPath_ &ndash; La ruta de acceso que se va a abrir. Para un bloc de notas, o para un grupo de sección en un bloc de notas, _bstrPath_ puede ser una ruta de acceso de la carpeta o la ruta de acceso a un archivo de sección .one. Si especifica la ruta de acceso a un archivo de sección .one, debe incluir la extensión .one de la cadena de ruta de acceso de archivo.  <br/><br/>_bstrRelativeToObjectID_ &ndash; El identificador de OneNote del objeto primario (Bloc de notas o grupo de secciones) en la que desea que el nuevo objeto para abrir. Si el parámetro _bstrPath_ es una ruta de acceso absoluta, se puede pasar una cadena vacía ("") para _bstrRelativeToObjectID_. Como alternativa, puede pasar el identificador de objeto del Bloc de notas o sección del grupo que contiene el objeto (sección o grupo de secciones) que desea crear y, a continuación, especifique el nombre de archivo (por ejemplo, section1.one) del objeto que desea crear en el que objeto primario.  <br/><br/>_pbstrObjectID_ &ndash; (Parámetro de salida) el identificador del objeto que se devuelve de OneNote para el Bloc de notas, el grupo de sección o la sección que se abre el método **OpenHierarchy** . Este parámetro es un puntero a la cadena en la que desea que el método para escribir el identificador.  <br/><br/>_cftlfNotExist_ &ndash; (Opcional) un valor enumerado de la enumeración [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType) . Si se pasa un valor para _cftIfNotExist_, el método **OpenHierarchy** crea el grupo de la sección o el archivo de sección en la ruta de acceso especificada sólo si el archivo ya no existe.  <br/> |
   
Si especifica un grupo de sección que no está en un bloc de notas abierto, el método **OpenHierarchy** abre el grupo de sección como un bloc de notas. Si especifica una sección que no está en un bloc de notas abierto, el método **OpenHierarchy** abre la sección en el grupo de sección reciente secciones abierto. Si especifica un grupo de secciones o una sección que ya está en un bloc de notas abierto, no ocurre nada debido a que el grupo de sección o la sección ya está abierta, así como. En cualquier caso, **OpenHierarchy** devuelve el identificador de objeto para el grupo de sección, el Bloc de notas o la sección que especifique, por lo que puede usar en otras operaciones. 
  
También puede usar el método **OpenHierarchy** para crear nuevas secciones, en lugar de hacerlo mediante la importación de XML. 
  
El código siguiente muestra cómo utilizar el método **OpenHierarchy** para abrir la sección de las reuniones en el Bloc de notas de trabajo y obtener el identificador de la sección. Si la sección no existe ya, OneNote crea en la ubicación que especifique. 
  
```cs
static void OpenSection()
    {
        String strID;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.OpenHierarchy("C:\\Documents and Settings\\user\\My Documents\\OneNote Notebooks\\Work\\Meetings.one", 
        System.String.Empty, out strID, OneNote.CreateFileType.cftSection);
    }

```

### <a name="deletehierarchy-method"></a>DeleteHierarchy (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Elimina cualquier objeto hierarchy (un grupo de sección, sección o página) de la jerarquía de Bloc de notas de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Parameters** <br/> | _bstrObjectID_ &ndash; El identificador de OneNote del objeto que desea eliminar. El objeto puede ser un grupo de sección, sección o página.  <br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) modificación la fecha y hora que piensa por última vez el objeto que desea eliminar. Si se pasa un valor distinto de cero para este parámetro, OneNote continúa con la actualización sólo si el valor que se pasa coincide con la fecha y hora reales que se modificó por última vez el objeto. Pasar un valor para este parámetro ayuda a evitar que se sobrescriba accidentalmente modifica los usuarios realizados desde la última vez que se modificó el objeto.  <br/><br/>_deletePermanently_ &ndash; (Opcional) **true** para eliminar permanentemente el contenido; **false** para mover el contenido a la OneNote Papelera de reciclaje para el Bloc de notas correspondiente (el valor predeterminado). Si el Bloc de notas se encuentra en formato de OneNote 2007, no existe ningún papelera de reciclaje, por lo que el contenido se elimina de manera permanente.  <br/> |
   
### <a name="createnewpage-method"></a>CreateNewPage (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Agrega una nueva página a la sección que se especifica. La página nueva se agrega como la última página de la sección  <br/> |
|**Sintaxis** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Parameters** <br/> | _bstrSectionID_ &ndash; Una cadena que contiene el identificador de OneNote de la sección en la que desea crear la nueva página.  <br/><br/>_pbstrPageID_ &ndash; Puntero de A (parámetro de salida) a la cadena en el que el método escribe el identificador de OneNote para la página recién creada.  <br/><br/>_npsNewPageStyle_ &ndash; Un valor de la enumeración **NewPageStyle** que especifica el estilo de la página que se creará.  <br/> |
   
La API de OneNote incluye el método **CreateNewPage** su comodidad. Puede lograr el mismo resultado, con un mayor control sobre cómo se coloca la nueva página en la jerarquía, llamando al método **UpdateHierarchy** . El método **UpdateHierarchy** también le permite crear las subpáginas al mismo tiempo a medida que cree una nueva página. 
  
### <a name="closenotebook-method"></a>CloseNotebook (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Cierra el Bloc de notas especificada.  <br/> |
|**Sintaxis** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Parameters** <br/> | _bstrNotebookID_ &ndash; El identificador de OneNote del Bloc de notas que desea cerrar.  <br/><br/>_Forzar_ &ndash; (Opcional) **true** para cerrar el Bloc de notas, incluso si hay cambios en el Bloc de notas de OneNote no puede sincronizar antes de cerrarlo; en caso contrario, **false** (valor predeterminado).  <br/> |
   
Puede usar el método **CloseNotebook** para cerrar el Bloc de notas que especifique. Cuando se llama a este método, OneNote sincroniza todos los archivos sin conexión con el contenido del Bloc de notas actual, si es necesario y, a continuación, cierra el Bloc de notas especificada. Después de que devuelve el método, el Bloc de notas ya no aparece en la lista de blocs de notas abiertos en la interfaz de usuario (UI) de OneNote. 
  
### <a name="gethierarchyparent-method"></a>GetHierarchyParent (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Obtiene el identificador de OneNote para el objeto primario de un objeto de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Parameters** <br/> | _bstrObjectID_ &ndash; Una cadena que contiene el identificador de OneNote del objeto del que desea buscar el objeto primario.  <br/><br/>_pbstrParentID_ &ndash; Puntero de A (parámetro de salida) a la cadena en el que el método escribe el identificador de OneNote del objeto primario.  <br/> |
   
Si el objeto de OneNote no tiene ningún objeto primario (por ejemplo, cuando un usuario desea obtener al elemento principal de un bloc de notas), se produce una excepción.
  
### <a name="getspeciallocation-method"></a>GetSpecialLocation (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Busca la ruta de acceso a la ubicación donde OneNote almacena algunos elementos especiales, como el Bloc de notas de forma predeterminada, las copias de seguridad y notas sin archivar.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Parameters** <br/> | _slToGet_ &ndash; Uno de los valores de enumeración de [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) que especifica la ubicación de la carpeta especial a obtener.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; Puntero de A (parámetro de salida) a la cadena en la que desea que OneNote para escribir la ruta de acceso de la carpeta especial.  <br/> |
   
Puede usar este método para determinar la ubicación en el disco de la carpeta Notas sin archivar. Que es la carpeta en la que OneNote almacena las notas que se crean cuando se arrastra un elemento en OneNote, así como notas que proceden directamente de otras aplicaciones (como los que se producen cuando haga clic en **Enviar a OneNote** en Microsoft Outlook o Microsoft Internet Explorer). 
  
## <a name="page-content-methods"></a>Métodos de contenido de la página
<a name="ON14DevRef_Application_PageContent"> </a>

Los métodos descritos en esta sección permiten a descubrir, actualizar y eliminar el contenido en las páginas de los blocs de notas de OneNote, así como para publicar contenido de OneNote.
  
### <a name="getpagecontent-method"></a>GetPageContent (método)

|||
|:-----|:-----|
|**Descripción**|Obtiene todo el contenido (en formato XML de OneNote) de la página especificada.|
|**Sintaxis**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Parameters**| _bstrPageId_ &ndash; El identificador de OneNote de la página cuyo contenido se desea obtener.<br/><br/>_pbstrPageXmlOut_ &ndash; Puntero de A (parámetro de salida) a la cadena en la que desea que OneNote para escribir el resultado XML.<br/><br/>_pageInfoToExport_ &ndash; (Opcional) especifica si el método **GetPageContent** devuelve contenido binario, insertado en el código XML y de base-64 codificada. Contenido binario puede incluir, por ejemplo, imágenes y datos de entrada de lápiz. El parámetro _pageInfoToExport_ también especifica si se debe marcar la selección en el código XML que devuelve el método **GetPageContent** . Se tarda un valor enumerado de la enumeración [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo) .<br/><br/>_xsSchema_ &ndash; (Opcional) la versión del esquema XML de OneNote, del tipo **XMLSchema**, que desea que el resultado. Puede especificar si desea que el esquema XML versión 2013, 2010, 2007, o la versión actual. <br/><br/>**Nota**: se recomienda especificar una versión de OneNote (por ejemplo, **xs2013**) en lugar de usar **xsCurrent** o déjelo en blanco, ya que esto le permitirá el complemento para que funcione con las futuras versiones de OneNote.           |
   
De forma predeterminada, para evitar la longitud exceso en la cadena XML que devuelve, OneNote no incrustar contenido binario en el código XML. Por la misma razón, no marque seguridad de la selección actual con los atributos de la selección. Objetos binarios incluyen un identificador de OneNote en sus etiquetas. Para obtener un objeto binario, llame al método **GetBinaryPageContent** y pase el identificador de OneNote obtener desde el método **GetPageContent** . Utilice el método **GetPageContent** cuando no es necesario inmediatamente los datos binarios. 
  
### <a name="updatepagecontent-method"></a>UpdatePageContent (método)

|||
|:-----|:-----|
|**Descripción**|Actualiza o modifica el contenido en la página.|
|**Sintaxis**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Parameters**| _bstrPageChangesXmlIn_ &ndash; Una cadena que contiene el código XML de OneNote que incluye los cambios que desea realizar en la página.<br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) modificación la fecha y hora que piensa por última vez la página que desea actualizar. Si se pasa un valor distinto de cero para este parámetro, OneNote continúa con la actualización sólo si el valor que se pasa coincide con la fecha y hora reales que se modificó por última vez la página. Pasar un valor para este parámetro ayuda a evitar que se sobrescriba accidentalmente modifica los usuarios realizados desde la última vez que se modificó la página.<br/><br/>_xsSchema_ &ndash; (Opcional) la versión del esquema XML de OneNote, del tipo **XMLSchema**, que desea que el resultado. Puede especificar si desea que XML versión del esquema de 2013, 2010, 2007, o la versión actual. <br/><br/>**Nota**: se recomienda especificar una versión de OneNote (por ejemplo, **xs2013**) en lugar de usar **xsCurrent** o déjelo en blanco, ya que esto le permitirá el complemento para que funcione con las futuras versiones de OneNote.<br/><br/>_Forzar_ (Opcional) **true** para actualizar el contenido de la página, incluso si no hay datos desconocidos en la página de una versión posterior de OneNote; en caso contrario, **false** (valor predeterminado). |
   
Puede usar este método para modificar la página de distintas maneras. Por ejemplo, puede usar el método **UpdatePageContent** para agregar un esquema a una página, cambiar el contenido de un esquema, agregar imágenes, agregar entrada de lápiz, mover el contenido o modificar el texto en los esquemas. 
  
Como un ejemplo más específico, es posible que use el método **GetPageContent** para exportar una página existente, realizar algunos cambios en el código XML de la página y, a continuación, use el método **UpdatePageContent** para importar toda la página de nuevo. O bien, puede usar este método para agregar nuevos objetos de página, como imágenes, a la parte inferior de una página existente. 
  
Los únicos objetos que se deben incluir en el código XML que se pasa al método **UpdatePageContent** son objetos de nivel de página (por ejemplo, contornos, imágenes de la página o entrada de lápiz en la página) que han cambiado. Este método no modificar o quitar objetos de nivel de página que no se especifica en el parámetro _bstrPageChangesXmlIn_ . El método reemplaza por completo los objetos de nivel de página, como contornos, cuyos identificadores coinciden con los de los objetos que se pasa. Por consiguiente, debe especificar completamente todos los objetos de nivel de página en el código, incluidos los cambios que desea realizar en ellos y todo el contenido existente. 
  
Por ejemplo, si la página contiene un esquema y una imagen de fondo de la página, puede reemplazar el esquema y deje la imagen no modificada por completamente que especifica el esquema en el código XML, utilizando el identificador del esquema existente y, sin incluir la imagen en el código. Debido a que el esquema revisado que incluyen en el código completamente reemplaza el esquema existente, debe incluir todo el contenido del esquema.
  
Además, el método **UpdatePageContent** modifica sólo las propiedades de elemento que especifique en el parámetro _bstrPageChangesXmlIn_ . Por ejemplo, si especifica algunos, pero no todos, las propiedades del elemento **PageSettings** , las propiedades que no se especifican no se modifican. 
  
En el ejemplo siguiente se muestra cómo utilizar el método **UpdatePageContent** para cambiar el título de una página y agregar texto de ejemplo a la página. Antes de ejecutar el código, sustituya un identificador de página válido para el identificador de la página que se muestra en el código, por lo que el código funcione en su equipo. Puede obtener el identificador de página de una página mediante el método **GetHierarchy** y examinando los resultados. 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"http://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
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

### <a name="getbinarypagecontent-method"></a>GetBinaryPageContent (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Devuelve un objeto binario, como entrada de lápiz o imágenes en una página de OneNote como una cadena con codificación base-64.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Parameters** <br/> | _bstrPageID_ &ndash; El identificador de OneNote de la página que contiene el objeto binario a obtener.  <br/><br/>_bstrCallBackID_ &ndash; El identificador de OneNote del objeto binario que desea obtener. Este identificador, conocido como un **callbackID**, se encuentra en el código XML de OneNote para una página devuelta por el método **GetPageContent** .  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; Puntero de A (parámetro de salida) en una cadena en la que OneNote escribe el objeto binario como una cadena con codificación base-64.  <br/> |
   
### <a name="deletepagecontent-method"></a>DeletePageContent (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Elimina un objeto &ndash; como un objeto de **esquema**, **entrada de lápiz**o **imagen** desde una página.  <br/> |
|**Sintaxis** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Parameters** <br/> | _bstrPageID_ &ndash; El identificador de OneNote de la página que contiene el objeto que se va a eliminar.  <br/><br/>_bstrObjectID_ &ndash; El identificador de OneNote del objeto que se desea eliminar.  <br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) modificación la fecha y hora que piensa por última vez la página que contiene el contenido que desea eliminar. Si se pasa un valor distinto de cero para este parámetro, OneNote continúa con la eliminación sólo si el valor que se pasa coincide con la fecha y hora reales que se modificó por última vez la página. Si se pasa un valor para este parámetro ayuda a evitar la sobrescritura accidentalmente las ediciones realizadas por los usuarios desde la última vez que se modificó la página.  <br/><br/>_Forzar_ &ndash; (Opcional) **true** para actualizar el contenido de la página, incluso si no hay datos desconocidos en la página de una versión posterior de OneNote; en caso contrario, **false** (valor predeterminado).  <br/> |
   
### <a name="publish-method"></a>Método Publish

|||
|:-----|:-----|
|**Descripción** <br/> |Exporta la página especificada a un archivo en cualquier formato que admita de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; El identificador de OneNote de la jerarquía que se va a exportar.  <br/><br/>_bstrTargetFilePath_ &ndash; La ruta de acceso absoluta a la ubicación donde desea guardar el archivo de salida resultante. El archivo que especifique debe ser uno que ya no existe en esa ubicación.  <br/><br/>_pfPublishFormat_ &ndash; Uno de los valores de enumeración de [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) que especifica el formato en el que desea que la página publicada (por ejemplo, MHTML, PDF y así sucesivamente).  <br/><br/>_bstrCLSIDofExporter_ &ndash; El identificador de clase (CLSID) de una aplicación COM registrada que puede exportar a Microsoft Windows mejorado metarchivos (.emf). La aplicación COM debe implementar la interfaz **IMsoDocExporter** . Este parámetro se incluye para permitir que los programadores de terceros para escribir su propio código para publicar contenido de OneNote en un formato personalizado. Para obtener más información acerca de la interfaz **IMsoDocExporter** , consulte [Extending the Office 2007 Fixed-Format Export Feature](http://msdn.microsoft.com/en-us/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
En la actualidad, OneNote es compatible con los formatos de archivo siguientes:
  
- Archivos MHTML (.mht)
- Archivos de Adobe Acrobat PDF (.pdf)
- Archivos XML Paper Specification (XPS) (.xps)
- Archivos de OneNote 2013, 2010 o 2007 (.one)
- Archivos del paquete de OneNote (onepkg)
- Documentos de Microsoft Word (.doc o .docx)
- Microsoft Windows mejorado metarchivos (.emf)
- Archivos HTML (.html)
    
Este método produce exactamente los mismos resultados que obtendrá haciendo clic en **Publicar** en la interfaz de usuario y especificar el formato. 
  
## <a name="navigation-methods"></a>Métodos de exploración
<a name="ON14DevRef_Application_Navigation"> </a>

Los métodos descritos en esta sección permiten buscar, vaya a y vincular a blocs de notas de OneNote, grupos de sección, secciones, páginas y objetos page.
  
### <a name="navigateto-method"></a>NavigateTo (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Se desplaza al objeto especificado (por ejemplo, las secciones, páginas y elementos de **esquema** dentro de páginas).  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameters** <br/> | _bstrHierarchyObjectID_ &ndash; El identificador de OneNote del objeto que desee para navegar por la jerarquía de OneNote.  <br/><br/>_bstrObjectID_ &ndash; El identificador de OneNote del objeto que va a explorar a en la página de OneNote.  <br/><br/>_fNewWindow_ &ndash; (Opcional) **true** para abrir el objeto especificado en una nueva ventana de OneNote. **false** no se abre una nueva ventana de OneNote si uno está abierto.  <br/> |
   
### <a name="navigatetourl-method"></a>NavigateToUrl (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Si pasa un vínculo de OneNote (onenote: / /), se abre la ventana de OneNote a la ubicación correspondiente en OneNote. Si el vínculo es externo a OneNote (por ejemplo, http:// o file://), aparecerá un cuadro de diálogo de seguridad. Tras despido, OneNote intenta abrir el vínculo y se devuelve un error de **HResult.hrObjectDoesNotExist** .  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameters** <br/> | _bstrUrl_ &ndash; Una cadena que indica dónde se vaya a. Podría tratarse de un vínculo de OneNote, o cualquier otra dirección URL, como una ubicación de red o vínculo web.  <br/><br/>_fNewWindow_ &ndash; (Opcional) **true** para abrir la dirección URL especificada en una nueva ventana de OneNote. **false** no se abre una nueva ventana de OneNote si uno está abierto.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>GetHyperLinkToObject (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Obtiene un hipervínculo OneNote al Bloc de notas especificado, el grupo de sección, sección, página u objeto page.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; El identificador de OneNote para el Bloc de notas, el grupo de sección, sección o página para la que desea que un hipervínculo.  <br/><br/>_bstrPageContentObjectID_ &ndash; El identificador de OneNote (opcional) para el objeto dentro de la página para la que desea que un hipervínculo. Por ejemplo, el objeto puede ser un esquema o un elemento de **esquema** . Si se pasa una cadena vacía (""), el vínculo devuelto señala el Bloc de notas, grupo de sección, sección o página que especificó en el parámetro _bstrHierarchyID_ . Si se pasa una cadena no vacía para el parámetro _bstrPageContentObjectID_ , el parámetro _bstrHierarchyID_ debe ser una referencia a la página que contiene el objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; Puntero de A (parámetro de salida) en una cadena en el que el método **GetHyperlinkToObject** escribe el texto de hipervínculo de salida.  <br/> |
   
Al intentar navegar hasta el vínculo resultante, OneNote se abre y muestra el objeto especificado en el explorador.
  
### <a name="getwebhyperlinktoobject-method"></a>GetWebHyperlinktoObject (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Devuelve un hipervínculo a un objeto que se abre en el cliente Web de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; El identificador de OneNote para el Bloc de notas, la sección grupo, sección o página para la que desea que un hipervínculo de la web.  <br/><br/>_bstrPageContentObjectID_ &ndash; El identificador de OneNote (opcional) para el objeto dentro de la página para la que desea que un hipervínculo. Por ejemplo, el objeto puede ser un esquema o un elemento de **esquema** . Si se pasa una cadena vacía (""), el vínculo devuelto señala el Bloc de notas, grupo de sección, sección o página que especificó en el parámetro _bstrHierarchyID_ . Si se pasa una cadena no vacía para el parámetro _bstrPageContentObjectID_ , el parámetro _bstrHierarchyID_ debe ser una referencia a la página que contiene el objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; Puntero de A (parámetro de salida) en una cadena en el que el método **GetWebHyperlinkToObject** escribe el texto de hipervínculo de salida. Si no se puede crear un hipervínculo web para el Bloc de notas, se devuelve un valor nulo.  <br/> |
   
### <a name="findpages-method"></a>FindPages (método)

|||
|:-----|:-----|
|**Descripción**|Devuelve una lista de las páginas que coinciden con el término de consulta especificada.|
|**Sintaxis**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameters**| _bstrStartNodeID_ &ndash; El nodo (raíz, Bloc de notas, el grupo de sección o sección) por debajo del cual buscar contenido. Este parámetro establece el ámbito de la búsqueda.<br/><br/>_bstrSearchString_ &ndash; La cadena de búsqueda. Pase exactamente la misma cadena que se debe escribir en el cuadro de búsqueda en la UI de OneNote. Puede usar los operadores bit a bit, como **y** y **o**, que debe ser todas las letras mayúsculas.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; Puntero de A (parámetro de salida) en una cadena en la que desea que OneNote para escribir la cadena XML de salida. La cadena XML resultante contiene la jerarquía de Bloc de notas desde la raíz hacia abajo a y, incluso, las páginas que coinciden con la cadena de búsqueda. Por ejemplo, el método **FindPages** no lista secciones que no contienen coincide con la página en la jerarquía. Además, si sólo hay una página en una sola sección coincide con la cadena, la jerarquía devuelta incluye la ruta de acceso a esa sección y de página, pero a no hay otros elementos de la jerarquía de Bloc de notas.<br/><br/>_fIncludeUnindexedPages_ &ndash; (Opcional) **true** para buscar las páginas que no se han indizado por la búsqueda de Windows; en caso contrario, **false**.<br/><br/>_fDisplay_ &ndash; (Opcional) **true** para ejecutar también la búsqueda en la interfaz de usuario para el usuario, como si el usuario hubiera escrito a sí mismos. **false** para realizar la consulta con ningún cambio en la interfaz de usuario (el valor predeterminado).<br/><br/>_xsSchema_ &ndash; (Opcional) el OneNote versión del esquema de la cadena _pbstrHierarchyXmlOut_. Este valor opcional se utiliza para especificar la versión del esquema XML de OneNote que contenga la cadena _pbstrHierarchyXmlOut_ . Si no se especifica este valor, OneNote se supone que el XML se encuentra en la versión de esquema _xsCurrent_. <br/><br/>**Nota**: se recomienda especificar una versión de OneNote (por ejemplo, **xs2013**) en lugar de usar **xsCurrent** o déjelo en blanco, ya que esto le permitirá el complemento para que funcione con las futuras versiones de OneNote.           |
   
 **FindPages** funciona únicamente si tiene Microsoft Search 3.0 o 4.0 instalado en el equipo. Windows Vista y Windows 7 incluyen este componente. Sin embargo, si está ejecutando una versión anterior de Windows, debe instalar [Búsqueda de Windows](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para **FindPages** para que funcione. 
  
### <a name="findmeta-method"></a>FindMeta (método)

|||
|:-----|:-----|
|**Descripción**|Devuelve una lista de objetos de OneNote que contienen metadatos que coincida con el término de consulta especificada.|
|**Sintaxis**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameters**| _bstrStartNodeID_ &ndash; El nodo (raíz, Bloc de notas, el grupo de sección o sección) por debajo del cual buscar contenido. Este parámetro establece el ámbito de la búsqueda.<br/><br/>_bstrSearchStringName_ &ndash; La cadena de búsqueda. Pase en cualquier parte del nombre de metadatos. Si se pasa una cadena vacía o un valor null, todos los objetos que tienen metadatos coincidirá con la consulta.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; Puntero de A (parámetro de salida) en una cadena en la que desea que OneNote para escribir la cadena XML de salida. La cadena XML resultante contiene la jerarquía de Bloc de notas desde la raíz hacia abajo a y, incluso, las páginas que coinciden con la cadena de búsqueda. Por ejemplo, el método **FindPages** no lista secciones que no contienen coincide con la página en la jerarquía. Además, si sólo hay una página en una sola sección coincide con la cadena, la jerarquía devuelta incluye la ruta de acceso a esa sección y de página, pero a no hay otros elementos de la jerarquía de Bloc de notas.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (Opcional) **true** para buscar las páginas que no se han indizado por la búsqueda de Windows; en caso contrario, **false**.<br/><br/>_xsSchema_ &ndash; (Opcional) el OneNote versión del esquema de la cadena _pbstrHierarchyXmlOut_. Este valor opcional se utiliza para especificar la versión del esquema XML de OneNote que contenga la cadena _pbstrHierarchyXmlOut_ . Si no se especifica este valor, OneNote se supone que el XML se encuentra en la versión de esquema _xsCurrent_. <br/><br/>**Nota**: se recomienda especificar una versión de OneNote (por ejemplo, **xs2013**) en lugar de usar **xsCurrent** o déjelo en blanco, ya que esto le permitirá el complemento para que funcione con las futuras versiones de OneNote.           |
   
**FindMeta** funciona únicamente si tiene Microsoft Windows Search 3.0 o 4.0 instalado en el equipo. Windows Vista y Windows 7 incluyen este componente. Sin embargo, si está ejecutando una versión anterior de Windows, debe instalar [Búsqueda de Windows](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para **FindMeta** para que funcione. 
  
## <a name="functional-methods"></a>Métodos funcionales
<a name="ON14DevRef_Application_Functional"> </a>

Los métodos descritos en esta sección permiten realizar determinadas acciones o establezca los parámetros dentro de la aplicación de OneNote.
  
### <a name="mergefiles-method"></a>MergeFiles (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios combinar los cambios para el mismo archivo en uno. Para que los archivos se considere la misma, deben tener el mismo identificador de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Parameters** <br/> | _bstrBaseFile_ &ndash; La cadena de ruta de acceso a la ubicación del archivo .one del estado inicial del archivo.  <br/><br/>_bstrClientFile_ &ndash; La cadena de ruta de acceso a la ubicación del archivo .one del segundo conjunto de cambios que se combinarán con el archivo de base después de que se combinan los cambios del archivo de servidor con la base.  <br/><br/>_bstrServerFile_ &ndash; La cadena de ruta de acceso a la ubicación del archivo .one del primer conjunto de cambios que se combinarán con el archivo de base.  <br/><br/>_bstrTargetFile_ &ndash; La cadena de ruta de acceso a la ubicación del archivo .one del archivo con los cambios combinados.  <br/> |
   
El método **MergeFiles** se diseñó para escenarios móviles en los que pueden existir varias versiones de un archivo de OneNote. 
  
### <a name="mergesections-method"></a>MergeSections (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Combina el contenido de una sección en otro en OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Parameters** <br/> | _bstrSectionSourceId_ &ndash; El identificador de OneNote de la sección que va a combinarse.  <br/><br/>_bstrSectionDestinationId_ &ndash; El identificador de OneNote de la sección que se combinarán en. La sección de origen se combinarán en esta sección de destino.  <br/> |
   
Este método realiza la misma operación que la característica **Combinar en otra sección** que está visible cuando haga clic en una sección. 
  
### <a name="quickfiling-method"></a>QuickFiling (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Devuelve una instancia del cuadro de diálogo [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog) , que se puede utilizar para seleccionar una ubicación dentro del árbol de jerarquía de OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>SyncHierarchy (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Fuerza OneNote para sincronizar el objeto especificado con el archivo de origen en el disco.  <br/> |
|**Sintaxis** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; El ID de OneNote del objeto que se va a sincronizar.  <br/> |
   
### <a name="setfilinglocation-method"></a>SetFilingLocation (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios especificar dónde y cómo se deben archivar determinados tipos de contenido en OneNote.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Parameters** <br/> | _flToSet_ &ndash; De la ubicación de archivado para establecer el tipo de objeto.  <br/><br/>_fltToSet_ &ndash; La ubicación en la que el tipo de archivo.  <br/><br/>_bstrFilingSectionID_ &ndash; El identificador de OneNote de la sección o página en qué ubicación que desea establecer. Si no es aplicable, el usuario puede pasar en null o una cadena vacía.  <br/> |
   
Los tipos de contenido que se puede archivar incluyen los elementos de Outlook y las notas de Web de Internet Explorer que se importan a OneNote mediante el comando **Enviar a OneNote** en cada aplicación. También se puede establecer la ubicación de archivado de los elementos que se imprimen en OneNote con este método. 
  
## <a name="properties"></a>Propiedades
<a name="ON14DevRef_Application_Properties"> </a>

En esta sección se describe las propiedades de la interfaz de **aplicación** . 
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|**Windows** <br/> |Proporciona a los usuarios acceso a las ventanas abiertas de OneNote. Esta propiedad permite a los usuarios enumerar el conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana. Para obtener más información, vea [Interfaces de Windows](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Devuelve la colección **COMAddIns** de OneNote. Esta colección contiene todos los complementos COM que están disponibles para OneNote. La propiedad **Count** de la colección **COMAddins** devuelve el número de complementos COM disponibles. Para obtener más información, vea el objeto [COMAddIns](http://msdn.microsoft.com/en-us/library/office/ff865489.aspx) .  <br/> |
|**LanguageSettings** <br/> |Permite tener acceso a algunas API para cambiar la configuración de idioma común de OneNote.  <br/> |
   
## <a name="events"></a>Events
<a name="ON14DevRef_Application_Events"> </a>

En esta sección se describe los eventos de la interfaz de aplicación.
  
> [!CAUTION]
> Eventos actualmente no se pueden agregar en código administrado. 
  
### <a name="onnavigate-event"></a>OnNavigate (evento)

|||
|:-----|:-----|
|**Descripción** <br/> |Permite que un usuario asignar una función que se llamará cuando la UI de OneNote se navega fuera de la ubicación actual de OneNote.  <br/> |
|**Sintaxis** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>OnHierarchyChange (método)

|||
|:-----|:-----|
|**Descripción** <br/> |Permite que un usuario asignar una función que se llamará cada vez que los cambios de jerarquía de OneNote (por ejemplo, agregar o eliminar páginas o mover secciones). Cambios en la jerarquía se procesan por lotes, por lo que si se producen varios cambios en o cerca de la misma hora, OneNote provoca el evento de una vez.  <br/> |
|**Sintaxis** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Parameters** <br/> | _bstrActivePageID_ &ndash; Pasa el identificador de OneNote de la página activa.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

