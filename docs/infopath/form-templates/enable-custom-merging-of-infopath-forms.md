---
title: Habilitar combinación personalizada de formularios de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: La característica Combinar formularios del editor de Microsoft InfoPath está diseñada para combinar los datos de varios formularios en un único formulario.
ms.openlocfilehash: 598c44bfe63a31237bf82ceb2212b001fbe7cc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386918"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>Habilitar combinación personalizada de formularios de InfoPath

La característica **Combinar formularios** del editor de Microsoft InfoPath está diseñada para combinar los datos de varios formularios en un único formulario. Esto es también conocida como agregación de datos. Si se habilita la combinación de formularios, puede haga clic en la pestaña **archivo** , haga clic en **Guardar &amp; enviar**, haga clic en **La combinación de formularios** en **importación &amp; vínculo**y, a continuación, haga clic en el botón de **La combinación de formularios** para seleccionar uno o varios formularios para combinar con la formulario abierto actualmente. El formulario que está actualmente abierto es el formulario de destino y los formularios seleccionados en el cuadro de diálogo **Combinar formularios** se conocen como los formularios de origen.
  
La agregación de datos que tiene lugar con la combinación de formularios puede incluir todos los datos que contienen los formularios de origen y de destino, o solo una parte de los datos originales. Las operaciones predeterminadas son las siguientes.
  
- Para elementos extensibles, los datos se insertan en una ubicación coincidente en el documento de destino. Esto ocurre cuando el atributo **MaxOccurs** del elemento de destino es mayor que 1. 
    
- Para elementos no extensibles (es decir, para elementos en los que **MaxOccurs** es "1"), los atributos de los elementos de origen se agregan a los atributos existentes del elemento de destino. 
    
## <a name="creating-a-custom-transform"></a>Crear una transformación personalizada

La operación predeterminada cuando se combinan formularios funciona correctamente con formularios basados en el mismo esquema XML. Sin embargo, en algunas circunstancias, es posible que desee combinar formularios basados en esquemas diferentes o invalidar la operación de combinación predeterminada para formularios basados en el mismo esquema. En estos escenarios, puede crear una transformación XSL (XSLT), que contiene instrucciones de agregación para la operación de combinación. La transformación se aplica durante la combinación para crear un documento DOM que contiene la información que se va a importar, junto con anotaciones que especifican cómo incorporar esta información en el documento de destino. Estas anotaciones son atributos XML del espacio de nombres  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.
  
Los atributos XML y sus valores sirven como instrucciones de agregación sobre cómo cada nodo se combina con el documento XML de destino. Estos atributos se describen en las siguientes secciones.
  
### <a name="select"></a>select

El atributo **agg:select** contiene una expresión XPath absoluta que identifica el elemento de destino. 
  
### <a name="insert"></a>insert

Un valor de "insert" para el atributo **agg:action** instruye a InfoPath para que inserte el elemento de origen como elemento secundario del elemento de destino que se especifica mediante el atributo **agg:select**. Los elementos secundarios del elemento de origen se incluyen en la operación de inserción. El atributo **selectChild** permite seleccionar una cierta ubicación para la operación de inserción de nodo. El atributo **order** se usa para especificar si los elementos de origen se insertan antes o después de los elementos de destino existentes. El valor predeterminado si el atributo **order** no está presente es "after". 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

Un valor de "replace" para el atributo **agg:action** instruye a InfoPath para que reemplace todos los elementos de destino a los que hace referencia el atributo **select** con el elemento de origen. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

Si el valor del atributo **agg:action** es "mergeAttributes", los atributos del elemento de origen se combinan con los atributos de los elementos de destino a los que hace referencia el atributo **select**. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>delete

Si el valor del atributo es **agg:action** "delete", los elementos de destino a los que hace referencia el atributo **select** se eliminan del documento de destino. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

Junto con los atributos especificados en el espacio de nombres  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`, se usa el espacio de nombres  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` para denotar un objeto XSL que implementa la interfaz **IXMLDOMDocument**. Uno de los miembros más útiles de esta interfaz es el método **get-documentElement**.
  
### <a name="get-documentelement"></a>get-documentElement

La función **target:get-documentElement** proporciona acceso al Modelo de objeto de documento del documento de destino. Se puede usar para cambiar el modo en que funciona la operación de combinación en los contenidos actuales del documento de destino. 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>Pasos para crear una combinación personalizada

1. Seleccione los tipos de documentos XML de origen de los que desea combinar datos. Recopile una muestra representativa de cada tipo de documento de origen.
    
2. Derive el esquema XML para cada tipo de documento XML de origen para un formulario de InfoPath existente. Este paso se realiza fácilmente mediante la exportación del esquema con el comando **Exportar archivos de origen** de la pestaña **Publicar** de Backstage. Para los documentos XML que no se crearon en InfoPath, puede usar una herramienta como Microsoft Visual Studio para crear un esquema desde el documento XML de muestra, o puede crear un formulario de muestra desde el documento XML en InfoPath y, a continuación, exportar el esquema que InfoPath deriva desde la estructura del documento. 
    
3. Identifique los datos que desea combinar de cada tipo de documento XML de origen. Este paso depende casi completamente de los requisitos de los formularios de origen y de destino. En algunos casos, es posible que desee copiar todos los datos del formulario de origen. En otros, podría querer copiar solo uno o dos elementos del documento XML subyacente del formulario. Cuando identifique los datos que desea combinar, preste especial atención a los documentos de origen y de destino para asegurar que los elementos se asignen lógicamente entre ambos formularios.
    
4. Cree una transformación XSL para cada tipo de documento XML de origen. Cuando configure la combinación de los formularios, este paso llevará la mayor cantidad de tiempo. El objetivo de la transformación XSL es convertir el documento XML de origen a un formato que se pueda combinar con el formulario de destino. Cuando diseñe la transformación, decida si desea usar la combinación desde rutas de ubicación XML o desde las instrucciones de agregación de InfoPath.
    
    Visual Studio es una herramienta conveniente para crear transformaciones XSL. Visual Studio proporciona color de sintaxis y un esquema del documento. Además proporciona, automáticamente, etiquetas de cierre para los elementos XLS, que pueden ayudar a disminuir la escritura redundante y los errores de ortografía difíciles de encontrar. También puede crear transformaciones XSL con un editor de texto como Bloc de notas.
    
    Comience con la transformación de identidad, que es simplemente una transformación XSL que genera el mismo archivo XML que se introduce:
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="https://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="https://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="https://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
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

    A continuación, agregue secciones de plantilla invalidantes a los elementos a los que desea agregar un control especial. Por ejemplo, esta plantilla cambia un elemento  `<src:Task>` por un elemento  `<my:field1>` y establece el valor del atributo **agg:action** en "replace". 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Agregue los archivos de la transformación XSL y los archivos de esquema de la plantilla de formulario. Luego de derivar esquemas para cada tipo de documento de origen y crear una transformación XSL para convertir cada tipo de documento de manera que InfoPath pueda combinar los datos, agréguelos como recursos al formulario. Haga clic en **Archivos de recursos** en la pestaña **Datos** y, a continuación, en **Agregar** en el cuadro de diálogo **Archivos de recursos**; busque el archivo de esquema o de transformación XSL y, a continuación, haga clic en **Aceptar**. Realice esta operación para cada archivo de esquema y de transformación XSL que creó.
    
    Si los esquemas que agrega usan el atributo **targetNamespace**, debe agregar un elemento de propiedad al archivo .xsf del formulario para que InfoPath conozca el espacio de nombres del esquema. Para obtener acceso a este archivo, haga clic en la pestaña **Archivo**, en **Publicar** y, a continuación, en **Exportar archivos de origen**. Seleccione una ubicación para los archivos y, a continuación, haga clic en **Aceptar**. Luego cierre la plantilla de formulario de InfoPath que está diseñando.
    
    Vaya a la ubicación que especificó para los archivos extraídos y encuentre el archivo con extensión de nombre de archivo .xsf. Por lo general se llama manifest.xsf. Abra el archivo en Bloc de notas, busque la etiqueta  `<xsf:file>` que corresponde al esquema y agregue un elemento de propiedad "espacio de nombres" para especificar el **targetNamespace** como se muestra en el siguiente ejemplo. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. El último paso para preparar el formulario para que admita la combinación personalizada es la actualización del elemento **importParameters** en el archivo .xsf asociado al formulario. 

    Primero, busque la etiqueta  `<xsf:importParameters>` en el archivo .xsf. Para cada par de transformación XSL/esquema que ha creado para el formulario, agregue un elemento **xsf: importSource** al elemento **xsf: importParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`. 
    
    El atributo **name** del elemento **xsf: importSource** contiene el nombre de la plantilla de formulario que se puede encontrar en un documento XML de origen. Por lo general, puede dejarlo vacío. El atributo **schema** contiene el nombre de un archivo de esquema que ha agregado a la plantilla de formulario en el paso anterior. Por último, el atributo **transform** contiene el nombre de la transformación XSL que desea usar para convertir los formularios que conforman el esquema. 
    
    Puede usar una transformación personalizada con el evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) o sola. 
    
## <a name="creating-a-custom-merge-in-code"></a>Crear una combinación personalizada en código

La combinación personalizada con código se admite mediante el uso del controlador de eventos [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , con el correspondiente atributo **useScriptHandler** del elemento **importParameters** en el archivo .xsf asociado al formulario. 

Para habilitar el evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) en el código administrado, active la casilla **Combinar usando código personalizado** y haga clic en el botón **Editar** en la categoría **Avanzadas** del cuadro de diálogo **Opciones de formulario** disponible en Backstage. 
  

