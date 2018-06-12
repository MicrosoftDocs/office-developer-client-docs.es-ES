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
# <a name="rich-text-and-web-services"></a>Texto enriquecido y servicios web

Microsoft InfoPath admite enlazar un control **Cuadro de texto enriquecido** en un formulario a un elemento XML recibido desde un servicio web, así como enviar datos desde un control de cuadro de texto enriquecido a un elemento XML a través de un servicio web. El elemento debe tener el formato de Lenguaje de marcado de hipertexto extensible (XHTML). Por ejemplo, los esquemas para un elemento llamado  `MyRichTextElement` que contiene texto enriquecido tendría la siguiente definición de esquema XML: 
  
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

Antes de poder vincular un control **Cuadro de texto enriquecido** al elemento XHTML, el elemento se debe ajustar con un nodo contenedor; este nodo contenedor puede pertenecer a cualquier espacio de nombres arbitrario. El nodo contenedor puede tener el siguiente aspecto: 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

Este tema describe el proceso de creación de un servicio web que puede enviar y recibir XHTML y cómo usar InfoPath para el vínculo con los parámetros del servicio web. Este tema no proporciona instrucciones detalladas sobre cómo crear este servicio web. Se supone que ya está familiarizado con el trabajo con servicios web.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Cómo diseñar un servicio web para recibir y enviar XHTML

El servicio web de ejemplo almacena los datos XHTML que envía y recibe en un archivo XML del servidor. Este archivo tiene el nombre out.xml, actúa como origen de datos que almacena los datos XHTML. Existen dos métodos web que se mostrarán para que una aplicación cliente pueda tener interfaz con el origen de datos XHTML:  `getXhtml` y  `setXhtml`. El método de servicio web  `getXhtml` devuelve un **XmlNode** que contiene el XHTML que se puede enlazar a un control de texto con formato enriquecido de InfoPath. El método del servicio web  `setXhtml` acepta un **XmlNode** como datos para almacenar en el archivo out.xml. 
  
> [!NOTE]
> [!NOTA] Estos métodos web requieren instrucciones **using** que hagan referencia a los espacios de nombres **System.IO** y **System.Xml**. 
  
El método de servicio web  `getXhtml` intenta cargar los datos XML devueltos del archivo out.xml en la carpeta Datos de la unidad C. Si no puede hacerlo porque que no encuentra el archivo o porque no contiene un XML válido, el método devolverá un elemento HTML **DIV** que haga referencia al espacio de nombres XHTML. 
  
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

El método de servicio web  `setXhtml` acepta el formato XHTML de un control **Cuadro de texto enriquecido** en un formulario de InfoPath. Puesto que los servicios web no admiten una lista de nodos, cuando se envía un campo de texto enriquecido que contiene varias líneas a un servicio web, éste sólo acepta la primera línea y omite el resto. 
  
El método de ejemplo  `setXhtml` supone que recibirá un nodo XML de nivel superior que, en la mayoría de los casos, estará incluido en un elemento **DIV**. Si el XML recibido no contiene un elemento de ajuste, por ejemplo cuando el texto dentro del control de **Cuadro de texto enriquecido** no tiene formato, este método lo detectará mediante la comprobación de que la propiedad **NodeType** indique que el XML pasado es un nodo de texto. Si el XML es un nodo de texto, el método crea un elemento **DIV** y copia los contenidos del nodo de texto en **DIV** para que **DIV** contenga un nodo de texto secundario con el texto que se envió al servicio web. El XML recibido por este método se escribe en el archivo out.xml en la carpeta Datos de la unidad C. 
  
> [!NOTE]
> [!NOTA] El método  `setXhtml` de ejemplo fue escrito para aceptar datos XHTML de cualquier tamaño. En la práctica, siempre se debe comprobar cuántos datos se están enviando y definir un límite superior para la cantidad de datos que se pueden enviar. 
  
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>Cómo crear un formulario de InfoPath que intercambie datos con el servicio web de ejemplo

Para crear un formulario con el que probar el servicio web de ejemplo, realice los siguientes pasos.
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>Para crear un formulario que se conecte al servicio web de ejemplo

1. Abra el diseñador de formularios de InfoPath.
    
2. En la ficha **Nuevo**, haga doble clic en **Servicio web** en **Plantillas de formulario avanzadas**.
    
3. En el cuadro de diálogo **Asistente para la conexión de datos**, seleccione **Recibir datos** y, a continuación, haga clic en **Siguiente**.
    
4. Escriba la dirección del servicio web que contiene los métodos de ejemplo del servicio web y, a continuación, haga clic en **Siguiente**. 
    
5. Para el método de recepción, seleccione **getXhtml** como la operación y, a continuación, haga clic en **Siguiente**.
    
6. El método de servicio web **getXHTML** no tiene parámetros, por lo tanto, haga clic en **Siguiente**.
    
7. Haga clic en **Finalizar**.
    
8. En la ficha **Datos**, en el grupo **Acciones de envío**, haga clic en **A otras ubicaciones** y, a continuación, en **Servicio web** para usar el mismo servicio web para enviar datos. 
    
9. Escriba la dirección del servicio web que contiene los métodos de ejemplo del servicio web y haga clic en **Siguiente**.
    
10. Para el método de envío, seleccione **setXhtml** como la operación y haga clic en **Siguiente**.
    
11. Haga clic en **Modificar**, expanda la carpeta **dataFields**, expanda la carpeta **s0:getXhtmlResponse**, expanda la carpeta **getXhtmlResult**, seleccione el elemento **MyRichTextElement** y, a continuación, haga clic en **Siguiente**.
    
12. Haga clic en **Finalizar**.
    
13. En el panel de tareas **Campos**, expanda la carpeta **dataFields**. 
    
14. Expanda las carpetas **s0:getXhtmlResponse** y **getXhtmlResult**, y después arrastre el elemento **MyRichTextElement** al formulario. InfoPath reconocerá que el elemento **MyRichTextElement** es un elemento XHTML y usará un control de cuadro de texto enriquecido para enlazarse a él. 
    
15. Guarde o publique el formulario.
    
Para probar el formulario, ábralo, escriba contenido de texto enriquecido como imágenes, tablas y texto con formato. Haga clic en **Enviar** en la cinta para almacenar el contenido de texto enriquecido en el archivo out.xml del servidor. Haga clic en **Consulta** en la ficha **Ver** y haga clic en el botón del formulario **Ejecutar consulta**. El control **Cuadro de texto enriquecido** debe mostrar el contenido XHTML del archivo out.xml. Si el campo de texto enriquecido contiene varias líneas, el servicio web sólo aceptará la primera línea e ignorará el resto. 
  

