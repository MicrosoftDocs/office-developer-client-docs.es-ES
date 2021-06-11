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
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="3a9c4-105">Trabajar con las clases XPathNavigator y XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="3a9c4-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="3a9c4-p102">Para obtener acceso a los datos XML y manipularlos en los orígenes de datos de la plantilla de formulario, muchos miembros del modelo de objetos de código administrado proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) crean (o se les pasa) una instancia de la clase **XPathNavigator** del espacio de nombres **System.Xml.XPath**. Una vez que se tiene acceso a un objeto **XPathNavigator** devuelto por un miembro del modelo de objetos de InfoPath, se pueden usar las propiedades y los métodos de la clase **XPathNavigator** para trabajar con los datos.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p102">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace. After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="3a9c4-p103">El miembro usado con más frecuencia del espacio de nombres **Microsoft.Office.InfoPath** que usa la clase **XPathNavigator** es el método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) de la clase [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , que permite trabajar con los datos almacenados, representados por un objeto **DataSource**. El método **CreateNavigator** crea un objeto **XPathNavigator** colocado en la raíz del origen de datos representado por el objeto **DataSource**.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p103">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object. The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="3a9c4-110">[!SUGERENCIA] Si está familiarizado con el uso de MSXML5 para trabajar con datos en Microsoft InfoPath 2003, puede considerar el método **CreateNavigator** como un reemplazo de la propiedad **DOM** de **DataObject**.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="3a9c4-111">Uso de la clase XPathNavigator para obtener acceso al origen de datos principal del formulario</span><span class="sxs-lookup"><span data-stu-id="3a9c4-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="3a9c4-p104">Para obtener acceso al origen de datos principal del formulario, llame al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directamente desde la palabra clave **this** (C#) o **Me** (Visual Basic). En el ejemplo siguiente se usa el método **CreateNavigator** para crear un objeto **XPathNavigator** colocado en la raíz del origen de datos principal y, a continuación, se usa la propiedad **OuterXml** de la clase **XPathNavigator** para mostrar el XML devuelto en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p104">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword. The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
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
> <span data-ttu-id="3a9c4-114">[!NOTA] Al llamar al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directamente desde la palabra clave **this** o **Me**, se obtiene el mismo resultado que si se llama al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) mediante la propiedad [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) (  `this.MainDataSource.CreateNavigator()`) o pasando una cadena vacía a la propiedad [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (  `this.DataSources[""].CreateNavigator()`).</span><span class="sxs-lookup"><span data-stu-id="3a9c4-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="3a9c4-115">Selección y configuración de los nodos XML para campos en el origen de datos principal</span><span class="sxs-lookup"><span data-stu-id="3a9c4-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="3a9c4-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="3a9c4-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="3a9c4-p105">Para seleccionar el nodo XML único para un campo en un origen de datos, use el método **SelectSingleNode(String,IXmlNamespaceResolver)** de la clase **XPathNavigator**. Si desea trabajar con un conjunto de campos o grupos de repetición, use el método **Select(String,IXmlNamespaceResolver)** de la clase **XPathNavigator**. Este método devuelve un objeto **XPathNodeIterator** que representa una colección de nodos.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p105">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class. If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class. This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="3a9c4-120">Selección y configuración del valor de un único nodo</span><span class="sxs-lookup"><span data-stu-id="3a9c4-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="3a9c4-p106">El método **SelectSingleNode** sobrecargado que debe usar tiene un parámetro  _xpath_ que toma una expresión XPath como cadena y un parámetro  _resolver_ que toma un objeto **XmlNamespaceManager** para resolver los prefijos de espacio de nombres. Para seleccionar un único nodo en el origen de datos principal del formulario, pase una expresión XPath que especifique el campo o el grupo que desea seleccionar para el parámetro  _xpath_, junto con el objeto **XmlNamespaceManager** devuelto por la propiedad [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) del objeto **XmlForm**. El objeto **XmlNamespaceManager** devuelto se inicializa en el momento de carga con todos los espacios de nombres definidos por el archivo de definición de formulario (.xsf) de la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p106">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes. To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object. The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="3a9c4-p107">[!SUGERENCIA] La manera más sencilla de crear una expresión XPath para seleccionar un nodo en el origen de datos del formulario consiste en hacer clic con el botón secundario en el campo o grupo del panel de tareas **Campos** y elegir **Copiar XPath**. Para crear y probar expresiones XPath editadas manualmente para obtener acceso a los nodos de un esquema XML complejo o muy anidado, agregue un control **Cuadro de expresión** al formulario, especifique la expresión XPath para el control y obtenga una vista previa del formulario para mostrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="3a9c4-p108">En el siguiente ejemplo se usa el método **SelectSingleNode** para seleccionar el único nodo para el campo  `EmailAlias`. A continuación, se usa el método **SetValue** de la clase **XPathNavigator** y la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la clase [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para establecer el valor del campo en el alias del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p108">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field. Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
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

<span data-ttu-id="3a9c4-128">Para obtener información acerca del procedimiento para crear expresiones XPath, vea el tema sobre referencia de XPath en MSDN y el artículo de [recomendación de W3C del Lenguaje de rutas XML (XPath), versión 1.0](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="3a9c4-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="3a9c4-129">Configuración del valor de un nodo que tiene el atributo xsi:nil</span><span class="sxs-lookup"><span data-stu-id="3a9c4-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="3a9c4-p109">Con algunos tipos de datos, al intentar establecer el valor de un campo en blanco mediante programación, se produce el error "La validación del esquema encontró errores que no son de tipo de datos". Normalmente, este error se produce porque el atributo [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) del elemento está establecido en **true**. Si se examina el elemento XML subyacente para el campo en blanco del formulario, se puede ver este valor de configuración. Por ejemplo, el fragmento XML para el siguiente campo Fecha en blanco tiene el atributo **xsi:nil** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p109">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors." Typically the cause of this error is that the element has the [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**. If you examine the underlying XML element for the blank field in the form, you can see this setting. For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="3a9c4-p110">Si el atributo **xsi:nil** está establecido en **true**, significa que el elemento está presente pero no tiene ningún valor, es decir, es nulo. Si intenta establecer mediante programación el valor de dicho nodo, InfoPath mostrará el mensaje "La validación del esquema encontró errores que no son de tipo de datos" porque el elemento está marcado actualmente como nulo. InfoPath establece el atributo **xsi:nil** en **true** para los campos nulo de los siguientes tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p110">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null . If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null . InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="3a9c4-137">**Whole Number (integer)**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="3a9c4-138">**Decimal (double)**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="3a9c4-139">**Date (date)**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-139">**Date (date)**</span></span>
    
- <span data-ttu-id="3a9c4-140">**Time (time)**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-140">**Time (time)**</span></span>
    
- <span data-ttu-id="3a9c4-141">**Date and Time (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="3a9c4-p111">Para evitar este error, debe probarse el código para el atributo **xsi:nil** y, si está presente, quitarlo antes de configurar el valor del nodo. La siguiente subrutina toma un objeto **XpathNavigator** colocado en el nodo que desea configurar, busca el atributo **nil** y, si lo encuentra, lo elimina.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p111">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node. The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
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

<span data-ttu-id="3a9c4-144">Se puede llamar a esta subrutina antes de intentar configurar un campo de un tipo de datos que podría tener el atributo **xsi:nil**, como se muestra en el siguiente ejemplo que configura un campo Fecha.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
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
> <span data-ttu-id="3a9c4-p112">[!NOTA] Aunque la implementación del objeto **XPathNavigator** en InfoPath expone el método **SetTypedValue** (que se usa para configurar un nodo mediante un valor de un tipo específico), InfoPath no implementa dicho método. En su lugar, debe usar el método **SetValue** y pasar un valor de cadena del formato correcto para el tipo de datos del nodo.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p112">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method. You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="3a9c4-147">Selección y configuración de un conjunto de nodos de repetición</span><span class="sxs-lookup"><span data-stu-id="3a9c4-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="3a9c4-p113">Para especificar un conjunto de campos o grupos de repetición que sean de un número indeterminado, use el método **Select** de la clase **XPathNavigator**. Este método devuelve un objeto XPathNodeIterator que puede usarse para procesar una iteración en la colección de nodos especificada.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p113">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class. This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="3a9c4-150">En el ejemplo siguiente se supone que la plantilla de formulario contiene un control **Lista con viñetas** o un control de repetición similar, enlazado a un elemento de repetición denominado  `field1`.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="3a9c4-151">La expresión XPath del campo se pasa al método **Select** y el **XPathNodeIterator** devuelto se asigna a la variable  `nodes`.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="3a9c4-152">A continuación, se usa el método MoveNext para procesar una iteración en la colección de nodos, y la propiedad Current para devolver un objeto **XPathNavigator** colocado en el nodo actual.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="3a9c4-153">Por último, use la **propiedad Value** para recuperar y mostrar el valor de cada campo de repetición.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
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

<span data-ttu-id="3a9c4-p115">En el ejemplo anterior se trabaja con valores de cadena en el campo de repetición especificado. Sin embargo, si el campo contiene valores numéricos, se puede usar un código similar para procesar una iteración en los valores del campo para que realicen operaciones aritméticas, como calcular el total o el promedio de los valores.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="3a9c4-156">Del mismo modo, en lugar de usar la propiedad **Value** para recuperar el valor de cada instancia del campo de repetición, puede usar el método **SetValue** para procesar una iteración en los campos y configurar sus valores, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="3a9c4-157">Uso de la clase XPathNavigator para obtener acceso a un origen de datos externo</span><span class="sxs-lookup"><span data-stu-id="3a9c4-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="3a9c4-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="3a9c4-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="3a9c4-p116">Para obtener acceso a un origen de datos externo asociado al formulario, pase el nombre del origen de datos a la propiedad [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Para crear una conexión a un nuevo origen de datos externo o para ver una lista de los nombres de las conexiones existentes a orígenes de datos externos, haga clic en **Conexiones de datos** en la ficha **Datos** de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p116">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="3a9c4-p117">En el siguiente ejemplo de código se muestra cómo crear un objeto **XPathNavigator** colocado en la raíz de un origen de datos externo denominado "CityList", mediante el método **CreateNavigator**, y se usa la propiedad **OuterXml** de la clase **XPathNavigator** para mostrar el XML devuelto en un cuadro de mensaje. En este ejemplo de código se supone que se ha creado una conexión de datos a una lista de nombres de ciudad que está almacenada en un origen de datos externo, como un documento XML o una lista de SharePoint, y se le ha asignado el nombre "CityList" a esta conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-p117">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box. This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
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

<span data-ttu-id="3a9c4-163">Una vez que se tiene acceso a un objeto **XPathNavigator** colocado en la raíz de un origen de datos externo, puede usar miembros de la clase **XPathNavigator**, como los métodos **SelectSingleNode** y **SetValue**, para trabajar con los datos que contiene.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="3a9c4-164">Miembros del modelo de objetos de InfoPath que usan las clases XPathNavigator y XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="3a9c4-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="3a9c4-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="3a9c4-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="3a9c4-166">En la tabla siguiente se ofrece un resumen de todos los miembros del espacio de nombres **Microsoft.Office.InfoPath** que usan la clase **XPathNavigator** para obtener acceso a los datos XML y manipularlos o enviarlos.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="3a9c4-167">**Clase primaria**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-167">**Parent Class**</span></span>|<span data-ttu-id="3a9c4-168">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a9c4-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="3a9c4-170">[BuildSqlFromXmlNodes (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="3a9c4-172">[BuildSqlFromXmlNodes (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3a9c4-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="3a9c4-174">[Source (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3a9c4-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="3a9c4-176">[Context (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-177">DataSource</span><span class="sxs-lookup"><span data-stu-id="3a9c4-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="3a9c4-178">[CreateNavigator (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="3a9c4-179">[GetNamedNodeProperty (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="3a9c4-180">[SetNamedNodeProperty (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="3a9c4-182">[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="3a9c4-184">[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="3a9c4-186">[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-187">FormError</span><span class="sxs-lookup"><span data-stu-id="3a9c4-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="3a9c4-188">[Site (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="3a9c4-190">[Agregar métodos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-191">FormTemplate</span><span class="sxs-lookup"><span data-stu-id="3a9c4-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="3a9c4-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="3a9c4-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="3a9c4-194">[Xml (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="3a9c4-196">[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-197">Signature</span><span class="sxs-lookup"><span data-stu-id="3a9c4-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="3a9c4-198">[SignatureBlockXmlNode (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="3a9c4-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="3a9c4-200">[SignatureContainer (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-201">View</span><span class="sxs-lookup"><span data-stu-id="3a9c4-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="3a9c4-202">[Métodos GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="3a9c4-203">[Métodos SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="3a9c4-204">[Métodos SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="3a9c4-206">[Execute (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="3a9c4-207">[GenerateDataSetDiffGram (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="3a9c4-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="3a9c4-209">[OldParent (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="3a9c4-210">[Site (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="3a9c4-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="3a9c4-212">[Propiedad MainDataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) que devuelve un objeto **DataSource** que, a su vez, proporciona el método **CreateNavigator** para crear un objeto **XPathNavigator** situado en la raíz del documento XML subyacente del formulario (origen de datos principal).</span><span class="sxs-lookup"><span data-stu-id="3a9c4-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="3a9c4-213">[MergeForm (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="3a9c4-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="3a9c4-215">[Método NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="3a9c4-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3a9c4-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="3a9c4-217">[Métodos ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="3a9c4-218">Además de los miembros del modelo de objetos de InfoPath que devuelven o aceptan un objeto **XPathNavigator**, los métodos siguientes devuelven una instancia de la clase **XPathNodeIterator** del espacio de nombres **System.Xml.XPath** para recorrer en iteración los nodos XML de los elementos especificados o seleccionados en una vista.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="3a9c4-219">**Clase primaria**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-219">**Parent Class**</span></span>|<span data-ttu-id="3a9c4-220">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="3a9c4-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a9c4-221">View</span><span class="sxs-lookup"><span data-stu-id="3a9c4-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="3a9c4-222">[Métodos GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="3a9c4-223">[Método GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a9c4-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="3a9c4-224">Uso de las clases XPathNavigator y XPathNodeIterator para trabajar con los datos seleccionados en una vista</span><span class="sxs-lookup"><span data-stu-id="3a9c4-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="3a9c4-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="3a9c4-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="3a9c4-226">En el ejemplo siguiente, se usan los miembros de las clases **XPathNavigator** y **XPathNodeIterator** para trabajar con los datos en la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a9c4-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="3a9c4-227">El método **CreateNavigator** de la clase **DataSource** se usa para crear una variable del objeto **XPathNavigator** denominada repeatingTableRow1, que de manera predeterminada se sitúa en la raíz del documento XML subyacente del formulario (el origen de datos principal).</span><span class="sxs-lookup"><span data-stu-id="3a9c4-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="3a9c4-228">El método **SelectSingleNode** de la clase **XPathNavigator** se usa para mover la posición del objeto **XPathNavigator** a la primera fila de un control **Tabla extensible** enlazado al grupo2 en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="3a9c4-229">La variable del objeto repeatingTableRow1 se pasa al método **SelectNodes** de la clase **View** para seleccionar los nodos de esa fila.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="3a9c4-230">Se declara una variable del objeto **XPathNodeIterator** denominada selectedNodes y el método **GetSelectedNodes** de la clase **View** se usa para rellenar el objeto **XPathNodeIterator** con los nodos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="3a9c4-231">La propiedad **Count** de la clase **XPathNodeIterator** se usa para mostrar el número de nodos que contiene la variable del objeto selectedNodes.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="3a9c4-232">Se usa un bucle For/Each para recorrer en iteración los nodos de la variable del objeto selectedNodes y mostrar información sobre cada nodo usando las propiedades **Name**, **InnerXml** y **Value** de la clase **XPathNavigator**.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
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

<span data-ttu-id="3a9c4-233">Para obtener más información sobre cómo trabajar con datos XML desde plantillas de formulario de InfoPath, vea el tema sobre cómo trabajar con datos XML usando la clase XPathNavigator en plantillas de formulario de InfoPath 2007.</span><span class="sxs-lookup"><span data-stu-id="3a9c4-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

