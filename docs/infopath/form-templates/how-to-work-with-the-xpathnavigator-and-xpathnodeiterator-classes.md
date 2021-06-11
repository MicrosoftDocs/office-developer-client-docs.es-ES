---
title: Trabajar con las clases XPathNavigator y XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- xpathnodeiterator class [infopath 2007],XPathNavigator class [InfoPath 2007],form XML data [InfoPath 2007], accessing,XML DOM [InfoPath 2007],converting MSXML5 script [InfoPath 2007],MSXML5 script [InfoPath 2007], converting
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Para obtener acceso a los datos XML y manipularlos en los orígenes de datos de la plantilla de formulario, muchos miembros del modelo de objetos de código administrado proporcionado por el espacio de nombres Microsoft.Office.InfoPath crean (o se les pasa) una instancia de la clase XPathNavigator del espacio de nombres System.Xml.XPath. Una vez que se tiene acceso a un objeto XPathNavigator devuelto por un miembro del modelo de objetos de InfoPath, se pueden usar las propiedades y los métodos de la clase XPathNavigator para trabajar con los datos.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303552"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Trabajar con las clases XPathNavigator y XPathNodeIterator

Para obtener acceso a los datos XML y manipularlos en los orígenes de datos de la plantilla de formulario, muchos miembros del modelo de objetos de código administrado proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) crean (o se les pasa) una instancia de la clase **XPathNavigator** del espacio de nombres **System.Xml.XPath**. Una vez que se tiene acceso a un objeto **XPathNavigator** devuelto por un miembro del modelo de objetos de InfoPath, se pueden usar las propiedades y los métodos de la clase **XPathNavigator** para trabajar con los datos. 
  
El miembro usado con más frecuencia del espacio de nombres **Microsoft.Office.InfoPath** que usa la clase **XPathNavigator** es el método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) de la clase [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , que permite trabajar con los datos almacenados, representados por un objeto **DataSource**. El método **CreateNavigator** crea un objeto **XPathNavigator** colocado en la raíz del origen de datos representado por el objeto **DataSource**. 
  
> [!TIP]
> [!SUGERENCIA] Si está familiarizado con el uso de MSXML5 para trabajar con datos en Microsoft InfoPath 2003, puede considerar el método **CreateNavigator** como un reemplazo de la propiedad **DOM** de **DataObject**. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Uso de la clase XPathNavigator para obtener acceso al origen de datos principal del formulario

Para obtener acceso al origen de datos principal del formulario, llame al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directamente desde la palabra clave **this** (C#) o **Me** (Visual Basic). En el ejemplo siguiente se usa el método **CreateNavigator** para crear un objeto **XPathNavigator** colocado en la raíz del origen de datos principal y, a continuación, se usa la propiedad **OuterXml** de la clase **XPathNavigator** para mostrar el XML devuelto en un cuadro de mensaje. 
  
```cs
XPathNavigator myNavigator = 
   this.CreateNavigator();
MessageBox.Show("Main data source XML: " +
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.CreateNavigator()
MessageBox.Show("Main data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

> [!NOTE]
> [!NOTA] Al llamar al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directamente desde la palabra clave **this** o **Me**, se obtiene el mismo resultado que si se llama al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) mediante la propiedad [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) (  `this.MainDataSource.CreateNavigator()`) o pasando una cadena vacía a la propiedad [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (  `this.DataSources[""].CreateNavigator()`). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Selección y configuración de los nodos XML para campos en el origen de datos principal
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Para seleccionar el nodo XML único para un campo en un origen de datos, use el método **SelectSingleNode(String,IXmlNamespaceResolver)** de la clase **XPathNavigator**. Si desea trabajar con un conjunto de campos o grupos de repetición, use el método **Select(String,IXmlNamespaceResolver)** de la clase **XPathNavigator**. Este método devuelve un objeto **XPathNodeIterator** que representa una colección de nodos. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Selección y configuración del valor de un único nodo

El método **SelectSingleNode** sobrecargado que debe usar tiene un parámetro  _xpath_ que toma una expresión XPath como cadena y un parámetro  _resolver_ que toma un objeto **XmlNamespaceManager** para resolver los prefijos de espacio de nombres. Para seleccionar un único nodo en el origen de datos principal del formulario, pase una expresión XPath que especifique el campo o el grupo que desea seleccionar para el parámetro  _xpath_, junto con el objeto **XmlNamespaceManager** devuelto por la propiedad [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) del objeto **XmlForm**. El objeto **XmlNamespaceManager** devuelto se inicializa en el momento de carga con todos los espacios de nombres definidos por el archivo de definición de formulario (.xsf) de la plantilla de formulario. 
  
> [!TIP]
> [!SUGERENCIA] La manera más sencilla de crear una expresión XPath para seleccionar un nodo en el origen de datos del formulario consiste en hacer clic con el botón secundario en el campo o grupo del panel de tareas **Campos** y elegir **Copiar XPath**. Para crear y probar expresiones XPath editadas manualmente para obtener acceso a los nodos de un esquema XML complejo o muy anidado, agregue un control **Cuadro de expresión** al formulario, especifique la expresión XPath para el control y obtenga una vista previa del formulario para mostrar los resultados. 
  
En el siguiente ejemplo se usa el método **SelectSingleNode** para seleccionar el único nodo para el campo  `EmailAlias`. A continuación, se usa el método **SetValue** de la clase **XPathNavigator** y la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la clase [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para establecer el valor del campo en el alias del usuario actual. 
  
```cs
XPathNavigator emailAlias = 
   this.CreateNavigator().SelectSingleNode(
      "/my:myFields/my:EmailAlias", NamespaceManager);
emailAlias.SetValue(this.Application.User.UserName.ToString());
```

```vb
Dim emailAlias As XPathNavigator = _
   Me.CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:EmailAlias", NamespaceManager)
emailAlias.SetValue(Me.Application.User.UserName.ToString())
```

Para obtener información acerca del procedimiento para crear expresiones XPath, vea el tema sobre referencia de XPath en MSDN y el artículo de [recomendación de W3C del Lenguaje de rutas XML (XPath), versión 1.0](https://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Configuración del valor de un nodo que tiene el atributo xsi:nil

Con algunos tipos de datos, al intentar establecer el valor de un campo en blanco mediante programación, se produce el error "La validación del esquema encontró errores que no son de tipo de datos". Normalmente, este error se produce porque el atributo [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) del elemento está establecido en **true**. Si se examina el elemento XML subyacente para el campo en blanco del formulario, se puede ver este valor de configuración. Por ejemplo, el fragmento XML para el siguiente campo Fecha en blanco tiene el atributo **xsi:nil** establecido en **true**.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Si el atributo **xsi:nil** está establecido en **true**, significa que el elemento está presente pero no tiene ningún valor, es decir, es nulo. Si intenta establecer mediante programación el valor de dicho nodo, InfoPath mostrará el mensaje "La validación del esquema encontró errores que no son de tipo de datos" porque el elemento está marcado actualmente como nulo. InfoPath establece el atributo **xsi:nil** en **true** para los campos nulo de los siguientes tipos de datos: 
  
- **Whole Number (integer)**
    
- **Decimal (double)**
    
- **Date (date)**
    
- **Time (time)**
    
- **Date and Time (dateTime)**
    
Para evitar este error, debe probarse el código para el atributo **xsi:nil** y, si está presente, quitarlo antes de configurar el valor del nodo. La siguiente subrutina toma un objeto **XpathNavigator** colocado en el nodo que desea configurar, busca el atributo **nil** y, si lo encuentra, lo elimina. 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "https://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "https://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

Se puede llamar a esta subrutina antes de intentar configurar un campo de un tipo de datos que podría tener el atributo **xsi:nil**, como se muestra en el siguiente ejemplo que configura un campo Fecha. 
  
```cs
// Access the main data source.
XPathNavigator myForm = this.CreateNavigator();
// Select the field.
XPathNavigator myDate = myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager);
// Check for and remove the "nil" attribute.
DeleteNil(myDate);
// Build the current date in the proper format. (yyyy-mm-dd)
string curDate = DateTime.Today.Year + "-" + DateTime.Today.Month + 
   "-" + DateTime.Today.Day;
// Set the value of the myDate field.
myDate.SetValue(strCurDate);
```

```vb
' Access the main data source.
Dim myForm As XPathNavigator = Me.CreateNavigator()
' Select the field.
Dim myDate As XPathNavigator = _
   myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager)
' Check for and remove the "nil" attribute.
DeleteNil(myDate)
' Build the current date in the proper format. (yyyy-mm-dd)
Dim curDate As String = DateTime.Today.Year + "-" + _
   DateTime.Today.Month + "-" + DateTime.Today.Day
' Set the value of the myDate field.
myDate.SetValue(strCurDate)
```

> [!NOTE]
> [!NOTA] Aunque la implementación del objeto **XPathNavigator** en InfoPath expone el método **SetTypedValue** (que se usa para configurar un nodo mediante un valor de un tipo específico), InfoPath no implementa dicho método. En su lugar, debe usar el método **SetValue** y pasar un valor de cadena del formato correcto para el tipo de datos del nodo. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Selección y configuración de un conjunto de nodos de repetición

Para especificar un conjunto de campos o grupos de repetición que sean de un número indeterminado, use el método **Select** de la clase **XPathNavigator**. Este método devuelve un objeto XPathNodeIterator que puede usarse para procesar una iteración en la colección de nodos especificada. 
  
En el ejemplo siguiente se supone que la plantilla de formulario contiene un control **Lista con viñetas** o un control de repetición similar, enlazado a un elemento de repetición denominado  `field1`. La expresión XPath del campo se pasa al método **Select** y el **XPathNodeIterator** devuelto se asigna a la variable  `nodes`. A continuación, se usa el método MoveNext para procesar una iteración en la colección de nodos, y la propiedad Current para devolver un objeto **XPathNavigator** colocado en el nodo actual. Por último, use la **propiedad Value** para recuperar y mostrar el valor de cada campo de repetición. 
  
```cs
string message = String.Empty;
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
while (nodes.MoveNext())
{
    message += nodes.Current.Value + System.Environment.NewLine;
}
MessageBox.Show(message);
```

```vb
Dim message As String = String.Empty
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Do While nodes.MoveNext
    message += nodes.Current.Value &amp; System.Environment.NewLine
Loop
MessageBox.Show(message)
```

En el ejemplo anterior se trabaja con valores de cadena en el campo de repetición especificado. Sin embargo, si el campo contiene valores numéricos, se puede usar un código similar para procesar una iteración en los valores del campo para que realicen operaciones aritméticas, como calcular el total o el promedio de los valores.
  
Del mismo modo, en lugar de usar la propiedad **Value** para recuperar el valor de cada instancia del campo de repetición, puede usar el método **SetValue** para procesar una iteración en los campos y configurar sus valores, como se muestra en el ejemplo siguiente. 
  
```cs
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
int myInt = 1;
while (nodes.MoveNext())
{
   nodes.Current.SetValue(myInt.ToString());
   myInt = myInt + 1;
}
```

```vb
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Dim myInt As Integer = 1
Do While nodes.MoveNext
   nodes.Current.SetValue(myInt.ToString())
   myInt = myInt + 1
Loop
```

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>Uso de la clase XPathNavigator para obtener acceso a un origen de datos externo
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Para obtener acceso a un origen de datos externo asociado al formulario, pase el nombre del origen de datos a la propiedad [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Para crear una conexión a un nuevo origen de datos externo o para ver una lista de los nombres de las conexiones existentes a orígenes de datos externos, haga clic en **Conexiones de datos** en la ficha **Datos** de la cinta de opciones. 
  
En el siguiente ejemplo de código se muestra cómo crear un objeto **XPathNavigator** colocado en la raíz de un origen de datos externo denominado "CityList", mediante el método **CreateNavigator**, y se usa la propiedad **OuterXml** de la clase **XPathNavigator** para mostrar el XML devuelto en un cuadro de mensaje. En este ejemplo de código se supone que se ha creado una conexión de datos a una lista de nombres de ciudad que está almacenada en un origen de datos externo, como un documento XML o una lista de SharePoint, y se le ha asignado el nombre "CityList" a esta conexión de datos. 
  
```cs
XPathNavigator myNavigator = 
   this.DataSources["CityList"].CreateNavigator();
MessageBox.Show("External data source XML: " + 
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.DataSources("CityList").CreateNavigator()
MessageBox.Show("External data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

Una vez que se tiene acceso a un objeto **XPathNavigator** colocado en la raíz de un origen de datos externo, puede usar miembros de la clase **XPathNavigator**, como los métodos **SelectSingleNode** y **SetValue**, para trabajar con los datos que contiene. 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Miembros del modelo de objetos de InfoPath que usan las clases XPathNavigator y XPathNodeIterator
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

En la tabla siguiente se ofrece un resumen de todos los miembros del espacio de nombres **Microsoft.Office.InfoPath** que usan la clase **XPathNavigator** para obtener acceso a los datos XML y manipularlos o enviarlos. 
  
|**Clase primaria**|**Miembro**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |[BuildSqlFromXmlNodes (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[Source (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Context (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |
||[GetNamedNodeProperty (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||[SetNamedNodeProperty (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[Site (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Agregar métodos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) (propiedad)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[Xml (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[SignatureBlockXmlNode (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[SignatureContainer (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[Métodos GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[Métodos SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||[Métodos SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)  <br/> |
||[GenerateDataSetDiffGram (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[OldParent (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)  <br/> |
||[Site (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Propiedad MainDataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) que devuelve un objeto **DataSource** que, a su vez, proporciona el método **CreateNavigator** para crear un objeto **XPathNavigator** situado en la raíz del documento XML subyacente del formulario (origen de datos principal).  <br/> |
||[MergeForm (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Método NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[Métodos ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |
   
Además de los miembros del modelo de objetos de InfoPath que devuelven o aceptan un objeto **XPathNavigator**, los métodos siguientes devuelven una instancia de la clase **XPathNodeIterator** del espacio de nombres **System.Xml.XPath** para recorrer en iteración los nodos XML de los elementos especificados o seleccionados en una vista. 
  
|**Clase primaria**|**Miembro**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[Métodos GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[Método GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Uso de las clases XPathNavigator y XPathNodeIterator para trabajar con los datos seleccionados en una vista
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

En el ejemplo siguiente, se usan los miembros de las clases **XPathNavigator** y **XPathNodeIterator** para trabajar con los datos en la secuencia siguiente: 
  
1. El método **CreateNavigator** de la clase **DataSource** se usa para crear una variable del objeto **XPathNavigator** denominada repeatingTableRow1, que de manera predeterminada se sitúa en la raíz del documento XML subyacente del formulario (el origen de datos principal).
    
2. El método **SelectSingleNode** de la clase **XPathNavigator** se usa para mover la posición del objeto **XPathNavigator** a la primera fila de un control **Tabla extensible** enlazado al grupo2 en el origen de datos. 
    
3. La variable del objeto repeatingTableRow1 se pasa al método **SelectNodes** de la clase **View** para seleccionar los nodos de esa fila. 
    
4. Se declara una variable del objeto **XPathNodeIterator** denominada selectedNodes y el método **GetSelectedNodes** de la clase **View** se usa para rellenar el objeto **XPathNodeIterator** con los nodos seleccionados. 
    
5. La propiedad **Count** de la clase **XPathNodeIterator** se usa para mostrar el número de nodos que contiene la variable del objeto selectedNodes. 
    
6. Se usa un bucle For/Each para recorrer en iteración los nodos de la variable del objeto selectedNodes y mostrar información sobre cada nodo usando las propiedades **Name**, **InnerXml** y **Value** de la clase **XPathNavigator**. 
    
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   this.CreateNavigator().SelectSingleNode(
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
// Get selected nodes.
XPathNodeIterator selectedNodes = 
   CurrentView.GetSelectedNodes();
// Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString());
// Loop through collection and display information.
foreach (XPathNavigator selectedNode in selectedNodes)
{
   MessageBox.Show(selectedNode.Name);
   MessageBox.Show(selectedNode.InnerXml);
   MessageBox.Show(selectedNode.Value);
}
```

```vb
' Create XPathNavigator and specify XPath for nodes.
Dim repeatingTableRow1 As XPathNavigator  = _
   Me.CreateNavigator().SelectSingleNode( _
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager)
' Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1)
' Get selected nodes.
Dim selectedNodes As XPathNodeIterator = _
   CurrentView.GetSelectedNodes()
' Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString())
' Loop through collection and display information.
Dim selectedNode As XPathNavigator
For Each selectedNode In selectedNodes
   MessageBox.Show(selectedNode.Name)
   MessageBox.Show(selectedNode.InnerXml)
   MessageBox.Show(selectedNode.Value)
Next
```

Para obtener más información sobre cómo trabajar con datos XML desde plantillas de formulario de InfoPath, vea el tema sobre cómo trabajar con datos XML usando la clase XPathNavigator en plantillas de formulario de InfoPath 2007.
  

