---
title: Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Los proyectos de plantillas de formulario que trabajan con el modelo de objetos de InfoPath 2003 utilizan Microsoft XML Core Services (MSXML) 5.0 para Microsoft Office internamente para trabajar con XML. En el código administrado, suele ser más fácil utilizar la compatibilidad con XML que ofrece el espacio de nombres System.Xml de la biblioteca de clases de .NET Framework. MSXML y System.Xml no pueden intercambiar objetos de forma nativa, así que, cada vez que necesite pasar datos XML entre InfoPath y otro código administrado, tendrá que convertirlos. Puede intercambiar datos XML entre objetos System.Xml y el código de formularios de InfoPath mediante las técnicas que se describen en este tema.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437402"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="8b687-107">Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="8b687-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="8b687-p102">Los proyectos de plantillas de formulario que trabajan con el modelo de objetos de InfoPath 2003 utilizan Microsoft XML Core Services (MSXML) 5.0 para Microsoft Office internamente para trabajar con XML. En el código administrado, suele ser más fácil utilizar la compatibilidad con XML que ofrece el espacio de nombres **System.Xml** de la biblioteca de clases de .NET Framework. MSXML y **System.Xml** no pueden intercambiar objetos de forma nativa, así que, cada vez que necesite pasar datos XML entre InfoPath y otro código administrado, tendrá que convertirlos. Puede intercambiar datos XML entre objetos **System.Xml** y el código de formularios de InfoPath mediante las técnicas que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="8b687-p102">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML. In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library. MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted. You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="8b687-112">Para usar los miembros del espacio de nombres **System.Xml** en un proyecto de código administrado que use el modelo de objetos de InfoPath 2003, debe agregar una referencia a **System.Xml** en la ficha **.NET** del cuadro de diálogo **Agregar referencia** en Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="8b687-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="8b687-113">**Notas**</span><span class="sxs-lookup"><span data-stu-id="8b687-113">**Notes**</span></span>
  
- <span data-ttu-id="8b687-114">Para consultar información de referencia acerca de MSXML, vea el SDK de MSXML.</span><span class="sxs-lookup"><span data-stu-id="8b687-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="8b687-115">Los miembros del modelo de objetos de MSXML que se ajustan mediante el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) no se pueden asignar a delegados en el código de formulario de las plantillas de formulario con código administrado.</span><span class="sxs-lookup"><span data-stu-id="8b687-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="8b687-p103">Si actualiza el código de la plantilla de formulario para usar el modelo de objetos que proporcionan los miembros del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , **System.Xml** se usa de forma nativa. Sin embargo, al hacerlo, debe convertir manualmente todo el código para usar el nuevo modelo de objetos. Para convertir la plantilla de forma que use el nuevo modelo de objetos, en la categoría **Programación** del cuadro de diálogo **Opciones de formulario**, haga clic en **Actualizar modelo de objetos**.</span><span class="sxs-lookup"><span data-stu-id="8b687-p103">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively. However, when doing so, you must manually convert all of your code to use the new object model. To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="8b687-119">Cargar un modelo de objetos de documentos (DOM) XML completo de System.Xml</span><span class="sxs-lookup"><span data-stu-id="8b687-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="8b687-120">En el ejemplo de código siguiente, se muestra cómo cargar un DOM XML completo tomado del código de **System.Xml** mediante el método [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) de InfoPath y los miembros de Microsoft XML Core Services que se ajustan mediante miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8b687-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="8b687-p104">En el siguiente ejemplo es necesaria una directiva **using** o **Imports** para el **System.Xml** en la sección de declaraciones del módulo de código del formulario. Además, como el método **Load** de la clase **XmlDocument** requiere **System.Security.Permissions.FileIOPermission**, debe configurar el nivel de seguridad de la plantilla de formulario como **Plena confianza** usando la categoría **Seguridad y confianza** del cuadro de diálogo **Opciones de formulario**.</span><span class="sxs-lookup"><span data-stu-id="8b687-p104">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module. Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
```cs
// Create a System.Xml XmlDocument and load an XML file.
XmlDocument doc = new XmlDocument();
doc.Load("c:\\temp\\MyFile.xml");
// Create an MSXML DOM object.
IXMLDOMDocument newDoc = thisXDocument.CreateDOM();
// Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml);
```

```vb
' Create a System.Xml XmlDocument and load an XML file.
Dim doc As XmlDocument = New XmlDocument()
doc.Load("c:\temp\MyFile.xml");
' Create an MSXML DOM object.
Dim newDoc As IXMLDOMDocument = thisXDocument.CreateDOM()
' Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml)
```

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="8b687-123">Cargar un único nodo de System.Xml</span><span class="sxs-lookup"><span data-stu-id="8b687-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="8b687-p105">En el ejemplo de código siguiente se muestra una función que demuestra cómo clonar un único nodo de **System.Xml**. **XmlElement** mediante el método MSXML **createNode** ajustado.</span><span class="sxs-lookup"><span data-stu-id="8b687-p105">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**. **XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="8b687-126">En el siguiente ejemplo es necesaria una directiva **using** o **Imports** para **System.Xml** en la sección de declaraciones del módulo de código del formulario.</span><span class="sxs-lookup"><span data-stu-id="8b687-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
```cs
// This function takes a System.Xml XmlElement object and 
// an MSXML IXMLDOMDocument object, and returns an MSXML 
// IXMLDOMNode object that is a copy of the XmlElement object.
public IXMLDOMNode CloneSystemXmlElementToMsxml(
   XmlElement systemXmlElement, IXMLDOMDocument msxmlDocument)
{
   IXMLDOMNode msxmlResultNode;
   // Create a new element from the MSXML DOM using the same 
   // namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(
      DOMNodeType.NODE_ELEMENT, 
      systemXmlElement.Name, 
      systemXmlElement.NamespaceURI);
   // Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString();
   return msxmlResultNode;
}
```

```vb
' This function takes a System.Xml XmlElement object and 
' an MSXML IXMLDOMDocument object, and returns an MSXML 
' IXMLDOMNode object that is a copy of the XmlElement object.
Public Function CloneSystemXmlElementToMsxml(_
   XmlElement systemXmlElement, _
   IXMLDOMDocument msxmlDocument) As IXMLDOMNode
   Dim msxmlResultNode As IXMLDOMNode
   ' Create a new element from the MSXML DOM using the same 
   ' namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(_
      DOMNodeType.NODE_ELEMENT, _
      systemXmlElement.Name, _
      systemXmlElement.NamespaceURI)
   ' Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString()
   Return msxmlResultNode
End Function
```


