---
title: Habilitar combinación personalizada de formularios de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: La característica Combinar formularios del editor de Microsoft InfoPath está diseñada para combinar los datos de varios formularios en un único formulario.
ms.openlocfilehash: e0e6bfc074829f262d7eef3cf7bf6a86c3b2253b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815859"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="be2c4-103">Habilitar combinación personalizada de formularios de InfoPath</span><span class="sxs-lookup"><span data-stu-id="be2c4-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="be2c4-104">La característica **Combinar formularios** del editor de Microsoft InfoPath está diseñada para combinar los datos de varios formularios en un único formulario.</span><span class="sxs-lookup"><span data-stu-id="be2c4-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="be2c4-105">Esto es también conocida como agregación de datos.</span><span class="sxs-lookup"><span data-stu-id="be2c4-105">This is also known as data aggregation.</span></span> <span data-ttu-id="be2c4-106">Si se habilita la combinación de formularios, puede haga clic en la pestaña **archivo** , haga clic en **Guardar &amp; enviar**, haga clic en **La combinación de formularios** en **importación &amp; vínculo**y, a continuación, haga clic en el botón de **La combinación de formularios** para seleccionar uno o varios formularios para combinar con la formulario abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="be2c4-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="be2c4-107">El formulario que está actualmente abierto es el formulario de destino y los formularios seleccionados en el cuadro de diálogo **Combinar formularios** se conocen como los formularios de origen.</span><span class="sxs-lookup"><span data-stu-id="be2c4-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="be2c4-p102">La agregación de datos que tiene lugar con la combinación de formularios puede incluir todos los datos que contienen los formularios de origen y de destino, o solo una parte de los datos originales. Las operaciones predeterminadas son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p102">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data. The default operations are the following.</span></span>
  
- <span data-ttu-id="be2c4-p103">Para elementos extensibles, los datos se insertan en una ubicación coincidente en el documento de destino. Esto ocurre cuando el atributo **MaxOccurs** del elemento de destino es mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p103">For repeating elements, data is inserted at a matching location in the target document. This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="be2c4-112">Para elementos no extensibles (es decir, para elementos en los que **MaxOccurs** es "1"), los atributos de los elementos de origen se agregan a los atributos existentes del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="be2c4-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="be2c4-113">Crear una transformación personalizada</span><span class="sxs-lookup"><span data-stu-id="be2c4-113">Creating a Custom Transform</span></span>

<span data-ttu-id="be2c4-p104">La operación predeterminada cuando se combinan formularios funciona correctamente con formularios basados en el mismo esquema XML. Sin embargo, en algunas circunstancias, es posible que desee combinar formularios basados en esquemas diferentes o invalidar la operación de combinación predeterminada para formularios basados en el mismo esquema. En estos escenarios, puede crear una transformación XSL (XSLT), que contiene instrucciones de agregación para la operación de combinación. La transformación se aplica durante la combinación para crear un documento DOM que contiene la información que se va a importar, junto con anotaciones que especifican cómo incorporar esta información en el documento de destino. Estas anotaciones son atributos XML del espacio de nombres  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p104">The default operation when merging forms works well for forms that are based on the same XML schema. In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema. For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation. The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document. These annotations are XML attributes in the namespace  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="be2c4-p105">Los atributos XML y sus valores sirven como instrucciones de agregación sobre cómo cada nodo se combina con el documento XML de destino. Estos atributos se describen en las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p105">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document. These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="be2c4-121">select</span><span class="sxs-lookup"><span data-stu-id="be2c4-121">select</span></span>

<span data-ttu-id="be2c4-122">El atributo **agg:select** contiene una expresión XPath absoluta que identifica el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="be2c4-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="be2c4-123">insert</span><span class="sxs-lookup"><span data-stu-id="be2c4-123">insert</span></span>

<span data-ttu-id="be2c4-p106">Un valor de "insert" para el atributo **agg:action** instruye a InfoPath para que inserte el elemento de origen como elemento secundario del elemento de destino que se especifica mediante el atributo **agg:select**. Los elementos secundarios del elemento de origen se incluyen en la operación de inserción. El atributo **selectChild** permite seleccionar una cierta ubicación para la operación de inserción de nodo. El atributo **order** se usa para especificar si los elementos de origen se insertan antes o después de los elementos de destino existentes. El valor predeterminado si el atributo **order** no está presente es "after".</span><span class="sxs-lookup"><span data-stu-id="be2c4-p106">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute. The children of the source element are included in the insert operation. The **selectChild** attribute lets you select a certain location for the insert node operation. The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after. The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="be2c4-129">replace</span><span class="sxs-lookup"><span data-stu-id="be2c4-129">replace</span></span>

<span data-ttu-id="be2c4-130">Un valor de "replace" para el atributo **agg:action** instruye a InfoPath para que reemplace todos los elementos de destino a los que hace referencia el atributo **select** con el elemento de origen.</span><span class="sxs-lookup"><span data-stu-id="be2c4-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="be2c4-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="be2c4-131">mergeAttributes</span></span>

<span data-ttu-id="be2c4-132">Si el valor del atributo **agg:action** es "mergeAttributes", los atributos del elemento de origen se combinan con los atributos de los elementos de destino a los que hace referencia el atributo **select**.</span><span class="sxs-lookup"><span data-stu-id="be2c4-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="be2c4-133">delete</span><span class="sxs-lookup"><span data-stu-id="be2c4-133">delete</span></span>

<span data-ttu-id="be2c4-134">Si el valor del atributo es **agg:action** "delete", los elementos de destino a los que hace referencia el atributo **select** se eliminan del documento de destino.</span><span class="sxs-lookup"><span data-stu-id="be2c4-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="be2c4-p107">Junto con los atributos especificados en el espacio de nombres  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`, se usa el espacio de nombres  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` para denotar un objeto XSL que implementa la interfaz **IXMLDOMDocument**. Uno de los miembros más útiles de esta interfaz es el método **get-documentElement**.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p107">In conjunction with the attributes specified in the  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**. One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="be2c4-137">get-documentElement</span><span class="sxs-lookup"><span data-stu-id="be2c4-137">get-documentElement</span></span>

<span data-ttu-id="be2c4-p108">La función **target:get-documentElement** proporciona acceso al Modelo de objeto de documento del documento de destino. Se puede usar para cambiar el modo en que funciona la operación de combinación en los contenidos actuales del documento de destino.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p108">The **target:get-documentElement** function provides access to the Document Object Model of the destination document. It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="be2c4-140">Pasos para crear una combinación personalizada</span><span class="sxs-lookup"><span data-stu-id="be2c4-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="be2c4-p109">Seleccione los tipos de documentos XML de origen de los que desea combinar datos. Recopile una muestra representativa de cada tipo de documento de origen.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p109">Select the kinds of XML source documents from which you want to merge data. Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="be2c4-p110">Derive el esquema XML para cada tipo de documento XML de origen para un formulario de InfoPath existente. Este paso se realiza fácilmente mediante la exportación del esquema con el comando **Exportar archivos de origen** de la pestaña **Publicar** de Backstage. Para los documentos XML que no se crearon en InfoPath, puede usar una herramienta como Microsoft Visual Studio para crear un esquema desde el documento XML de muestra, o puede crear un formulario de muestra desde el documento XML en InfoPath y, a continuación, exportar el esquema que InfoPath deriva desde la estructura del documento.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p110">Derive the XML schema for each kind of XML source document for an existing InfoPath form. This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage. For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="be2c4-p111">Identifique los datos que desea combinar de cada tipo de documento XML de origen. Este paso depende casi completamente de los requisitos de los formularios de origen y de destino. En algunos casos, es posible que desee copiar todos los datos del formulario de origen. En otros, podría querer copiar solo uno o dos elementos del documento XML subyacente del formulario. Cuando identifique los datos que desea combinar, preste especial atención a los documentos de origen y de destino para asegurar que los elementos se asignen lógicamente entre ambos formularios.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p111">Identify the data that you want to merge from each kind of XML source document. This step will depend almost entirely on the requirements of both your source and destination forms. For some forms, you may want to copy all of the data from the source form. For others, you may want only one or two elements from the form's underlying XML document. When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="be2c4-p112">Cree una transformación XSL para cada tipo de documento XML de origen. Cuando configure la combinación de los formularios, este paso llevará la mayor cantidad de tiempo. El objetivo de la transformación XSL es convertir el documento XML de origen a un formato que se pueda combinar con el formulario de destino. Cuando diseñe la transformación, decida si desea usar la combinación desde rutas de ubicación XML o desde las instrucciones de agregación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p112">Create an XSL transform for each kind of XML source document. When configuring the merging of your forms, this step will take the most time. The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form. When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="be2c4-p113">Visual Studio es una herramienta conveniente para crear transformaciones XSL. Visual Studio proporciona color de sintaxis y un esquema del documento. Además proporciona, automáticamente, etiquetas de cierre para los elementos XLS, que pueden ayudar a disminuir la escritura redundante y los errores de ortografía difíciles de encontrar. También puede crear transformaciones XSL con un editor de texto como Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p113">Visual Studio is a convenient tool for creating XSL transforms. Visual Studio provides syntax coloring and a document outline. It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors. You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="be2c4-159">Comience con la transformación de identidad, que es simplemente una transformación XSL que genera el mismo archivo XML que se introduce:</span><span class="sxs-lookup"><span data-stu-id="be2c4-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="http://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="http://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    <span data-ttu-id="be2c4-p114">A continuación, agregue secciones de plantilla invalidantes a los elementos a los que desea agregar un control especial. Por ejemplo, esta plantilla cambia un elemento  `<src:Task>` por un elemento  `<my:field1>` y establece el valor del atributo **agg:action** en "replace".</span><span class="sxs-lookup"><span data-stu-id="be2c4-p114">Then add overriding template sections for the elements you want to add special handling for. For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="be2c4-p115">Agregue los archivos de la transformación XSL y los archivos de esquema de la plantilla de formulario. Luego de derivar esquemas para cada tipo de documento de origen y crear una transformación XSL para convertir cada tipo de documento de manera que InfoPath pueda combinar los datos, agréguelos como recursos al formulario. Haga clic en **Archivos de recursos** en la pestaña **Datos** y, a continuación, en **Agregar** en el cuadro de diálogo **Archivos de recursos**; busque el archivo de esquema o de transformación XSL y, a continuación, haga clic en **Aceptar**. Realice esta operación para cada archivo de esquema y de transformación XSL que creó.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p115">Add the XSL transform files and schema files in the form template. After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form. Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**. Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="be2c4-p116">Si los esquemas que agrega usan el atributo **targetNamespace**, debe agregar un elemento de propiedad al archivo .xsf del formulario para que InfoPath conozca el espacio de nombres del esquema. Para obtener acceso a este archivo, haga clic en la pestaña **Archivo**, en **Publicar** y, a continuación, en **Exportar archivos de origen**. Seleccione una ubicación para los archivos y, a continuación, haga clic en **Aceptar**. Luego cierre la plantilla de formulario de InfoPath que está diseñando.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p116">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema. To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**. Select a location for the files, and then click **OK**. Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="be2c4-p117">Vaya a la ubicación que especificó para los archivos extraídos y encuentre el archivo con extensión de nombre de archivo .xsf. Por lo general se llama manifest.xsf. Abra el archivo en Bloc de notas, busque la etiqueta  `<xsf:file>` que corresponde al esquema y agregue un elemento de propiedad "espacio de nombres" para especificar el **targetNamespace** como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="be2c4-p117">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension. Usually, this file is called manifest.xsf. Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="be2c4-173">El último paso para preparar el formulario para que admita la combinación personalizada es la actualización del elemento **importParameters** en el archivo .xsf asociado al formulario.</span><span class="sxs-lookup"><span data-stu-id="be2c4-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="be2c4-174">Primero, busque la etiqueta  `<xsf:importParameters>` en el archivo .xsf.</span><span class="sxs-lookup"><span data-stu-id="be2c4-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="be2c4-175">Para cada par de transformación XSL/esquema que ha creado para el formulario, agregue un elemento **xsf: importSource** al elemento **xsf: importParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span><span class="sxs-lookup"><span data-stu-id="be2c4-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="be2c4-176">El atributo **name** del elemento **xsf: importSource** contiene el nombre de la plantilla de formulario que se puede encontrar en un documento XML de origen.</span><span class="sxs-lookup"><span data-stu-id="be2c4-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="be2c4-177">Por lo general, puede dejarlo vacío.</span><span class="sxs-lookup"><span data-stu-id="be2c4-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="be2c4-178">El atributo **schema** contiene el nombre de un archivo de esquema que ha agregado a la plantilla de formulario en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="be2c4-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="be2c4-179">Por último, el atributo **transform** contiene el nombre de la transformación XSL que desea usar para convertir los formularios que conforman el esquema.</span><span class="sxs-lookup"><span data-stu-id="be2c4-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="be2c4-180">Puede usar una transformación personalizada con el evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) o sola.</span><span class="sxs-lookup"><span data-stu-id="be2c4-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="be2c4-181">Crear una combinación personalizada en código</span><span class="sxs-lookup"><span data-stu-id="be2c4-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="be2c4-182">La combinación personalizada con código se admite mediante el uso del controlador de eventos [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , con el correspondiente atributo **useScriptHandler** del elemento **importParameters** en el archivo .xsf asociado al formulario.</span><span class="sxs-lookup"><span data-stu-id="be2c4-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="be2c4-183">Para habilitar el evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) en el código administrado, active la casilla **Combinar usando código personalizado** y haga clic en el botón **Editar** en la categoría **Avanzadas** del cuadro de diálogo **Opciones de formulario** disponible en Backstage.</span><span class="sxs-lookup"><span data-stu-id="be2c4-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

