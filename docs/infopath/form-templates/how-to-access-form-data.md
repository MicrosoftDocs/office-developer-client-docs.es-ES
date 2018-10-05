---
title: Obtener acceso a datos de formularios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form data [infopath 2007],forms [InfoPath 2007], accessing properties,form templates [InfoPath 2007], accessing properties,opening forms [InfoPath 2007],printing forms [InfoPath 2007],forms [InfoPath 2007], printing,closing forms [InfoPath 2007],InfoPath 2007, accessing form data,forms [InfoPath 2007], accessing data source,forms [InfoPath 2007], closing,forms [InfoPath 2007], opening,printing [InfoPath 2007], forms,forms [InfoPath 2007], creating
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Si desea ampliar la funcionalidad de un formulario de InfoPath, con frecuencia es preciso tener acceso mediante programación a la información sobre el documento XML subyacente del formulario, tener acceso a los datos contenidos en dicho documento o realizar alguna acción en él. El modelo de objetos de InfoPath permite obtener acceso al documento XML subyacente de un formulario y manipularlo utilizando la clase XmlForm en asociación con la clase XmlFormCollection .
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386834"
---
# <a name="access-form-data"></a>Obtener acceso a datos de formularios

Si desea ampliar la funcionalidad de un formulario de InfoPath, con frecuencia es preciso tener acceso mediante programación a la información sobre el documento XML subyacente del formulario, tener acceso a los datos contenidos en dicho documento o realizar alguna acción en él. El modelo de objetos de InfoPath permite obtener acceso al documento XML subyacente de un formulario y manipularlo utilizando la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) en asociación con la clase [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) . 
  
La clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) es una de las más útiles del modelo de objetos de InfoPath, porque proporciona gran variedad de propiedades y métodos que no sólo interaccionan con el documento XML subyacente del formulario, sino que, además, realizan muchas de las acciones disponibles en la interfaz de usuario de InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Información general sobre la clase XmlFormCollection

La clase [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) proporciona los siguientes métodos y propiedades que los programadores de formularios pueden utilizar para administrar los objetos [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) que contiene la colección. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (método)  <br/> |Crea un formulario a partir del formulario especificado.  <br/> |
|Método [New (cadena, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (sobrecarga 1)  <br/> |Crea un formulario nuevo a partir del formulario especificado, utilizando el comportamiento de modo de apertura especificado.  <br/> |
|[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (método)  <br/> |Crea un formulario a partir de la plantilla de formulario especificada.  <br/> |
|Método [NewFromFormTemplate (String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 1)  <br/> |Crea un formulario nuevo a partir de la plantilla de formulario especificada y de datos XML.  <br/> |
|Método [NewFromFormTemplate (String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 2)  <br/> |Crea un nuevo formulario basado en la plantilla de formulario con datos especificados por un objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) .  <br/> |
|Método [NewFromFormTemplate (String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 3)  <br/> |Crea un nuevo formulario basado en la plantilla de formulario con datos especificados por un objeto **XPathNavigator** usando el comportamiento de modo abierto especificado.  <br/> |
|[Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (método)  <br/> |Abre el formulario especificado.  <br/> |
|Método [Open (cadena, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (sobrecarga 1)  <br/> |Abre el formulario especificado utilizando el comportamiento de modo de apertura especificado.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx) (propiedad)  <br/> |Obtiene el número de objetos **XmlForm** contenidos en la colección.  <br/> |
|[Elemento](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx) (propiedad)  <br/> |Obtiene una referencia al objeto **XmlForm** especificado de la colección por su valor de índice.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Información general sobre la clase XmlForm

La clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) proporciona los siguientes métodos y propiedades que los programadores de formularios pueden utilizar para interactuar con el documento XML subyacente de un formulario o realizar acciones en él. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Cierra el formulario.  <br/> |
|[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) (método)  <br/> |Obtiene una referencia a una colección **Microsoft.Office.Core.WorkflowTasks** para el formulario actual.  <br/> |
|[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) (método)  <br/> |Obtiene una referencia a la colección **Microsoft.Office.Core.WorkflowTemplates** para el formulario actual.  <br/> |
|[MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (método)  <br/> |Combina el formulario actual con el formulario especificado mediante la ruta de acceso o la dirección URL.  <br/> |
|[MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (método) (sobrecarga 1)  <br/> |Combina el formulario con el formulario de destino especificado en el nodo devuelto por parámetro **XPathNavigator** que se pasa al método.  <br/> |
|[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) (método)  <br/> |Proporciona un valor personalizado para la aplicación host o la página ASPX.  <br/> |
|[Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (método)  <br/> |Imprime el contenido del formulario mientras se presenta en la vista activa del formulario.  <br/> |
|[Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (método) (sobrecarga 1)  <br/> |Imprime el contenido del formulario mientras se presenta la vista activa del formulario mostrando el cuadro de diálogo **Imprimir**.  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Guarda el formulario en la dirección URL a la que esté asociado actualmente.  <br/> |
|Método [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Guarda el formulario en la dirección URL especificada.  <br/> |
|Método [SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Establece el nombre de archivo predeterminado para el cuadro de diálogo **Guardar como**.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) (método)  <br/> |Establece la ruta de acceso predeterminada para guardar el formulario mediante el cuadro de diálogo **Guardar como**.  <br/> |
|Método [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Envía el formulario mediante la operación de envío definida en la plantilla de formulario.  <br/> |
|[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) (propiedad)  <br/> |Obtiene un objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa la vista actual del formulario.  <br/> |
|[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) (propiedad)  <br/> |Obtiene un objeto [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) asociado al formulario.  <br/> |
|[DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) (propiedad)  <br/> |Obtiene el objeto [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) asociado al formulario.  <br/> |
|[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) (propiedad)  <br/> |Obtiene un valor que indica si los datos de un formulario han sido modificados desde la última vez que se guardó.  <br/> |
|[Errores](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) (propiedad)  <br/> |Obtiene una referencia a la [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) que está asociada con un formulario.  <br/> |
|[Extensión](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) (propiedad)  <br/> |Obtiene un [objeto System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) para obtener acceso a las funciones y variables globales contenidas en el archivo de código del formulario principal de un formulario mediante [System.Reflection](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx).  <br/> |
|Propiedad [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Obtiene una referencia a una bolsa de propiedades de tipo [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) que los formularios compatibles con exploradores pueden usar para conservar la información de estado de distintas sesiones en el servidor.  <br/> |
|[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) (propiedad)  <br/> |Obtiene un objeto [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) que puede usar el código que se ejecuta en una instancia hospedada de InfoPath para tener acceso al modelo de objetos de la aplicación de hospedaje.  <br/> |
|[Hospedado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) (propiedad)  <br/> |Obtiene información sobre si InfoPath está hospedada como control en otra aplicación.  <br/> |
|[Nombre de host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) (propiedad)  <br/> |Obtiene el nombre de la aplicación que hospeda a InfoPath como control.  <br/> |
|[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) (propiedad)  <br/> |Obtiene un objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa el origen de datos principal del formulario.  <br/> |
|[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) (propiedad)  <br/> |Obtiene una referencia a un objeto [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) que puede usarse para resolver, agregar o quitar espacios de nombres utilizados en el formulario.  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) (propiedad)  <br/> |Obtiene un valor que especifica si un formulario es nuevo.  <br/> |
|[Permiso](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) (propiedad)  <br/> |Obtiene una referencia a un objeto [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) asociado al formulario.  <br/> |
|[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) (propiedad)  <br/> |Obtiene una referencia al objeto [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) que representa la conexión de datos que está asociada con el formulario.  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) (propiedad)  <br/> |Obtiene un valor que indica si una plantilla de formulario es de sólo lectura o está bloqueada.  <br/> |
|[Recuperado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) (propiedad)  <br/> |Obtiene un valor que indica si un formulario se guardó la última vez mediante una operación de guardado de Autorrecuperación.  <br/> |
|[Sesión iniciada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) (propiedad)  <br/> |Obtiene un valor que indica si un formulario se ha firmado digitalmente mediante firmas digitales.  <br/> |
|[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) (propiedad)  <br/> |Obtiene una referencia a la colección [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) que está asociada con un formulario.  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) (propiedad)  <br/> |Obtiene una referencia a la [colección TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) que está asociada con una plantilla de formulario.  <br/> |
|[Plantilla](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) (propiedad)  <br/> |Obtiene una referencia al objeto [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) que representa el manifiesto (.xsf) de la plantilla de formulario asociada al formulario.  <br/> |
|[URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx) (propiedad)  <br/> |Obtiene el identificador uniforme de recursos (URI) de un formulario.  <br/> |
|[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) (propiedad)  <br/> |Obtiene o establece el usuario actual del nombre del rol del formulario.  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) (propiedad)  <br/> |Obtiene una referencia al objeto de [colección ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) asociado con la plantilla de formulario.  <br/> |
|Propiedad [XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Obtiene el valor del atributo **xml:lang** del documento XML subyacente del formulario.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Uso de la clase XmlFormCollection

Se puede tener acceso a la clase **XmlFormCollection** a través de la propiedad [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . En una plantilla de formulario creada con el modelo de objetos proporcionado por los miembros del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) puede usar la palabra clave **this** (C#) o **Me** (Visual Basic) en el código para tener acceso a la clase **Application** y a sus miembros. 
  
En el ejemplo siguiente se usa la propiedad **XmlForms** de la clase **Application** para crear una variable de objeto denominada myForms que hace referencia al objeto **XDocumentsCollection** de la instancia de InfoPath que se está ejecutando. Esta variable se utiliza después para mostrar el número de formularios que hay abiertos. 
  
```cs
// Create variable for accessing the XmlFormCollection.
XmlFormCollection myForms = this.Application.XmlForms;
// Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count);
```

```vb
// Create variable for accessing the XmlFormCollection.
Dim myForms As XmlFormCollection = Me.Application.XmlForms
' Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count)
```

La variable myForms también puede usarse para crear nuevos formularios (usando uno de los métodos **New** o **NewFromTemplate**) o para abrir formularios existentes (usando uno de los métodos **Open**). 
  
## <a name="using-the-xmlform-class"></a>Uso de la clase XmlForm

En una plantilla de formulario de código administrado creada con el modelo de objetos proporcionado por los miembros del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , puede usar la palabra clave **this** (C#) o **Me** (Visual Basic) en el código de formulario para tener acceso a los miembros de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) directamente (sin necesidad de una variable de objeto que establezca una referencia a la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ). 
  
### <a name="accessing-a-forms-property-values"></a>Acceso a los valores de propiedad de un formulario

En el ejemplo siguiente se utiliza la palabra clave **this** o **Me** para tener acceso a las propiedades **New**, **ReadOnly**, **Signed** y **Uri** de la clase **XmlForm** y mostrar los valores devueltos para el formulario activo en un cuadro de mensaje. 
  
```cs
MessageBox.Show(
   "Is new: " + this.New + System.Environment.NewLine +
   "Is read-only: " + this.ReadOnly + System.Environment.NewLine +
   "Is signed: " + this.Signed + System.Environment.NewLine +
   "Form URI: " + this.Uri);
```

```vb
MessageBox.Show( _
   "Is new: " &amp; Me.New &amp; System.Environment.NewLine &amp; _
   "Is read-only: " &amp; Me.ReadOnly &amp; System.Environment.NewLine + _
   "Is signed: " &amp; Me.Signed &amp; System.Environment.NewLine &amp; _
   "Form URI: " &amp; this.Uri)
```

### <a name="accessing-a-forms-data-source"></a>Acceso al origen de datos de un formulario

Una propiedad clave de la clase **XmlForm** con respecto a los datos del formulario es la propiedad **MainDataSource**, que devuelve una referencia al objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa los datos XML subyacentes del formulario activo, al que también se denomina origen de datos principal o primario del formulario. La clase **DataSource** proporciona el método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , que crea un objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) colocado en la raíz del documento XML subyacente del formulario. Las propiedades y los métodos de la clase **XPathNavigator** pueden después emplearse para desplazarse y modificar los datos XML subyacentes del formulario. 
  
En el ejemplo siguiente se usa la propiedad **MainDataSource** de la clase **XmlForm**para crear un objeto **XPathNavigator** situado en la raíz del origen de datos principal del formulario. La propiedad **OuterXml** de la clase **XPathNavigator** se usa posteriormente para mostrar todos los contenidos de un documento XML subyacente de un formulario. 
  
```cs
// Get outer XML of the underlying XML document.
string myDoc = this.MainDataSource.CreateNavigator.OuterXml.ToString();
// Display XML.
MessageBox.Show(myDoc);
```

```vb
' Get outer XML of the underlying XML document.
Dim myDoc As String myDoc = _
   Me.MainDataSource.CreateNavigator.OuterXml.ToString()
' Display XML.
MessageBox.Show(myDoc)
```

> [!NOTE]
> [!NOTA] Como InfoPath trata la propiedad **MainDataSource** como una propiedad predeterminada del objeto **XmlForm** al que se tiene acceso cuando se usa la palabra clave **this** o **Me**, puede omitirla de la línea de código usada para crear el objeto **XPathNavigator**. 
  
Para obtener más información acerca de la clase **XPathNavigator** en la lógica empresarial de una plantilla formulario de InfoPath, vea [trabajar con las clases XPathNavigator y XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Obtener acceso a los datos desde el archivo de plantilla del formulario

Es posible tener acceso a la información sobre la plantilla asociada con un formulario, incluidos el archivo de definición del formulario (.xsf ) y los datos XML de origen que contiene, usando la clase **XmlForm**. A esta información se tiene acceso mediante la propiedad [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) , que a su vez devuelve una referencia a un objeto [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) que representa la platilla de formulario asociado con el formulario activo. 
  
En el ejemplo siguiente, el primer cuadro de mensaje muestra parte de los datos que están disponibles mediante la clase **Template**, como la ubicación de identificador uniforme de recursos (URI) (utilizando la propiedad [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) ), el identificador de caché (usando la [CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) propiedad) y su número de versión (usando la propiedad [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) ). El cuadro de mensaje siguiente usa la propiedad [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) de la clase **Template** para crear un objeto **XPathNavigator** que se usa para mostrar el origen XML del archivo de definición de formulario (.xsf). 
  
```cs
// Display form template properties.
MessageBox.Show(
   "Cache ID: " + this.Template.CacheId + System.Environment.NewLine +
   "URI: " + this.ReadOnly + System.Environment.NewLine +
   "Version: " + this.Signed, "Form Template Properties");
// Display form definition file XML.
MessageBox.Show(this.Template.Manifest.OuterXml, 
   "Form Definition File XML");
```

```vb
' Display form template properties.
MessageBox.Show( _
   "Cache ID: " &amp; Me.Template.CacheId &amp; System.Environment.NewLine &amp;
   "URI: " &amp; Me.ReadOnly &amp; System.Environment.NewLine &amp;
   "Version: " &amp; Me.Signed, "Form Template Properties")
' Display form definition file XML.
MessageBox.Show(Me.Template.Manifest.OuterXml, _
   "Form Definition File XML")
```


