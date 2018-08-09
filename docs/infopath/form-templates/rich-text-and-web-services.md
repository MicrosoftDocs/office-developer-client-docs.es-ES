---
title: Texto enriquecido y servicios web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath admite enlazar un control Cuadro de texto enriquecido en un formulario a un elemento XML recibido desde un servicio web, así como enviar datos desde un control de cuadro de texto enriquecido a un elemento XML a través de un servicio web. El elemento debe tener el formato de Lenguaje de marcado de hipertexto extensible (XHTML). Por ejemplo, los esquemas para un elemento llamado MyRichTextElement que contiene texto enriquecido tendría la siguiente definición de esquema XML:'
ms.openlocfilehash: 07a7a3dbc0f054160adce54e316b01797feacd8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815964"
---
# <a name="rich-text-and-web-services"></a><span data-ttu-id="4e140-105">Texto enriquecido y servicios web</span><span class="sxs-lookup"><span data-stu-id="4e140-105">Rich Text and Web Services</span></span>

<span data-ttu-id="4e140-p102">Microsoft InfoPath admite enlazar un control **Cuadro de texto enriquecido** en un formulario a un elemento XML recibido desde un servicio web, así como enviar datos desde un control de cuadro de texto enriquecido a un elemento XML a través de un servicio web. El elemento debe tener el formato de Lenguaje de marcado de hipertexto extensible (XHTML). Por ejemplo, los esquemas para un elemento llamado  `MyRichTextElement` que contiene texto enriquecido tendría la siguiente definición de esquema XML:</span><span class="sxs-lookup"><span data-stu-id="4e140-p102">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service. The element must adhere to the Extensible HyperText Markup Language (XHTML) format. For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

<span data-ttu-id="4e140-p103">Antes de poder vincular un control **Cuadro de texto enriquecido** al elemento XHTML, el elemento se debe ajustar con un nodo contenedor; este nodo contenedor puede pertenecer a cualquier espacio de nombres arbitrario. El nodo contenedor puede tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="4e140-p103">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace. The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="4e140-p104">Este tema describe el proceso de creación de un servicio web que puede enviar y recibir XHTML y cómo usar InfoPath para el vínculo con los parámetros del servicio web. Este tema no proporciona instrucciones detalladas sobre cómo crear este servicio web. Se supone que ya está familiarizado con el trabajo con servicios web.</span><span class="sxs-lookup"><span data-stu-id="4e140-p104">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters. This topic does not provide detailed instructions on how to create such a Web service. It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="4e140-114">Cómo diseñar un servicio web para recibir y enviar XHTML</span><span class="sxs-lookup"><span data-stu-id="4e140-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="4e140-p105">El servicio web de ejemplo almacena los datos XHTML que envía y recibe en un archivo XML del servidor. Este archivo tiene el nombre out.xml, actúa como origen de datos que almacena los datos XHTML. Existen dos métodos web que se mostrarán para que una aplicación cliente pueda tener interfaz con el origen de datos XHTML:  `getXhtml` y  `setXhtml`. El método de servicio web  `getXhtml` devuelve un **XmlNode** que contiene el XHTML que se puede enlazar a un control de texto con formato enriquecido de InfoPath. El método del servicio web  `setXhtml` acepta un **XmlNode** como datos para almacenar en el archivo out.xml.</span><span class="sxs-lookup"><span data-stu-id="4e140-p105">The example Web service stores the XHTML data that it sends and receives in an XML file on the server. This file that is named out.xml, acts as a data source that stores the XHTML data. There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`. The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control. The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e140-120">[!NOTA] Estos métodos web requieren instrucciones **using** que hagan referencia a los espacios de nombres **System.IO** y **System.Xml**.</span><span class="sxs-lookup"><span data-stu-id="4e140-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="4e140-121">El método de servicio web  `getXhtml` intenta cargar los datos XML devueltos del archivo out.xml en la carpeta Datos de la unidad C. Si no puede hacerlo porque que no encuentra el archivo o porque no contiene un XML válido, el método devolverá un elemento HTML **DIV** que haga referencia al espacio de nombres XHTML.</span><span class="sxs-lookup"><span data-stu-id="4e140-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "http://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "http://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"http://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

<span data-ttu-id="4e140-p106">El método de servicio web  `setXhtml` acepta el formato XHTML de un control **Cuadro de texto enriquecido** en un formulario de InfoPath. Puesto que los servicios web no admiten una lista de nodos, cuando se envía un campo de texto enriquecido que contiene varias líneas a un servicio web, éste sólo acepta la primera línea y omite el resto.</span><span class="sxs-lookup"><span data-stu-id="4e140-p106">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form. Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="4e140-p107">El método de ejemplo  `setXhtml` supone que recibirá un nodo XML de nivel superior que, en la mayoría de los casos, estará incluido en un elemento **DIV**. Si el XML recibido no contiene un elemento de ajuste, por ejemplo cuando el texto dentro del control de **Cuadro de texto enriquecido** no tiene formato, este método lo detectará mediante la comprobación de que la propiedad **NodeType** indique que el XML pasado es un nodo de texto. Si el XML es un nodo de texto, el método crea un elemento **DIV** y copia los contenidos del nodo de texto en **DIV** para que **DIV** contenga un nodo de texto secundario con el texto que se envió al servicio web. El XML recibido por este método se escribe en el archivo out.xml en la carpeta Datos de la unidad C.</span><span class="sxs-lookup"><span data-stu-id="4e140-p107">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element. If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node. If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service. The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e140-p108">[!NOTA] El método  `setXhtml` de ejemplo fue escrito para aceptar datos XHTML de cualquier tamaño. En la práctica, siempre se debe comprobar cuántos datos se están enviando y definir un límite superior para la cantidad de datos que se pueden enviar.</span><span class="sxs-lookup"><span data-stu-id="4e140-p108">The sample  `setXhtml` method was written to accept XHTML data of any size. In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="4e140-130">Cómo crear un formulario de InfoPath que intercambie datos con el servicio web de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e140-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="4e140-131">Para crear un formulario con el que probar el servicio web de ejemplo, realice los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="4e140-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="4e140-132">Para crear un formulario que se conecte al servicio web de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e140-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="4e140-133">Abra el diseñador de formularios de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4e140-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="4e140-134">En la ficha **Nuevo**, haga doble clic en **Servicio web** en **Plantillas de formulario avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="4e140-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="4e140-135">En el cuadro de diálogo **Asistente para la conexión de datos**, seleccione **Recibir datos** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="4e140-136">Escriba la dirección del servicio web que contiene los métodos de ejemplo del servicio web y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="4e140-137">Para el método de recepción, seleccione **getXhtml** como la operación y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="4e140-138">El método de servicio web **getXHTML** no tiene parámetros, por lo tanto, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="4e140-139">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="4e140-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="4e140-140">En la ficha **Datos**, en el grupo **Acciones de envío**, haga clic en **A otras ubicaciones** y, a continuación, en **Servicio web** para usar el mismo servicio web para enviar datos.</span><span class="sxs-lookup"><span data-stu-id="4e140-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="4e140-141">Escriba la dirección del servicio web que contiene los métodos de ejemplo del servicio web y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="4e140-142">Para el método de envío, seleccione **setXhtml** como la operación y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="4e140-143">Haga clic en **Modificar**, expanda la carpeta **dataFields**, expanda la carpeta **s0:getXhtmlResponse**, expanda la carpeta **getXhtmlResult**, seleccione el elemento **MyRichTextElement** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4e140-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="4e140-144">Haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="4e140-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="4e140-145">En el panel de tareas **Campos**, expanda la carpeta **dataFields**.</span><span class="sxs-lookup"><span data-stu-id="4e140-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="4e140-p109">Expanda las carpetas **s0:getXhtmlResponse** y **getXhtmlResult**, y después arrastre el elemento **MyRichTextElement** al formulario. InfoPath reconocerá que el elemento **MyRichTextElement** es un elemento XHTML y usará un control de cuadro de texto enriquecido para enlazarse a él.</span><span class="sxs-lookup"><span data-stu-id="4e140-p109">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form. InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="4e140-148">Guarde o publique el formulario.</span><span class="sxs-lookup"><span data-stu-id="4e140-148">Save or publish the form.</span></span>
    
<span data-ttu-id="4e140-p110">Para probar el formulario, ábralo, escriba contenido de texto enriquecido como imágenes, tablas y texto con formato. Haga clic en **Enviar** en la cinta para almacenar el contenido de texto enriquecido en el archivo out.xml del servidor. Haga clic en **Consulta** en la ficha **Ver** y haga clic en el botón del formulario **Ejecutar consulta**. El control **Cuadro de texto enriquecido** debe mostrar el contenido XHTML del archivo out.xml. Si el campo de texto enriquecido contiene varias líneas, el servicio web sólo aceptará la primera línea e ignorará el resto.</span><span class="sxs-lookup"><span data-stu-id="4e140-p110">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text. Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server. Click **Query** on the **View** tab, and then click the **Run Query** button on the form. The **Rich Text Box** control should display the XHTML content from the out.xml file. If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

