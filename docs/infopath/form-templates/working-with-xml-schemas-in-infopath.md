---
title: Trabajo con esquemas XML en InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Las plantillas de formulario que se crean con Microsoft InfoPath usan un esquema XML (XSD) para llevar a cabo la validación estructural y de datos en el XML que entra, se modifica y sale de un formulario de InfoPath. Todas las plantillas de formulario creadas en el diseñador de formularios de InfoPath contienen por lo menos un archivo de esquema XSD (.xsd) que se usa para la validación en tiempo de ejecución.
ms.openlocfilehash: 6921a2206c098992a0a24e85c263992a0e2c98b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815992"
---
# <a name="working-with-xml-schemas-in-infopath"></a>Trabajo con esquemas XML en InfoPath

Las plantillas de formulario que se crean con Microsoft InfoPath usan un esquema XML (XSD) para llevar a cabo la validación estructural y de datos en el XML que entra, se modifica y sale de un formulario de InfoPath. Todas las plantillas de formulario creadas en el diseñador de formularios de InfoPath contienen por lo menos un archivo de esquema XSD (.xsd) que se usa para la validación en tiempo de ejecución.
  
> [!NOTE]
> [!NOTA] La información que se presenta en este tema se aplica a las plantillas de formulario diseñadas para su uso en el editor de InfoPath. Las plantillas de formulario compatibles con el explorador tienen requisitos de esquema XSD más estrictos. Para obtener más información, vea la documentación sobre los esquemas XML en plantillas de formulario compatibles con el explorador disponible en MSDN. 
  
## <a name="using-externally-authored-xml-schemas"></a>Uso de esquemas XML creados externamente

Para cargar un archivo de esquema XSD que no se haya creado en InfoPath, siga estos pasos.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Para crear una plantilla de formulario basada en un esquema externo

1. En Backstage, haga clic en **Nuevo**, haga clic en **XML o Esquema** bajo **Plantillas de formulario avanzadas** y, por último, haga clic en **Diseñar este formulario**.
    
2. En el **Asistente del origen de datos**, especifique el archivo de esquema XSD que desea usar y haga clic en **Siguiente** para completar las páginas restantes del asistente. 
    
## <a name="unsupported-xsd-constructs"></a>Construcciones XSD no admitidas

En las secciones siguientes se describen las construcciones XSD que InfoPath no puede controlar en tiempo de ejecución. Evite estas construcciones cuando cree una plantilla de formulario en el diseñador de formularios de InfoPath.
  
## <a name="entity-and-entities-types"></a>Tipos ENTITY y ENTITIES

Los tipos **ENTITY** y **ENTITIES** requieren una definición de tipo de documento (DTD) para validación que no es compatible con InfoPath. InfoPath no permite diseñar una plantilla de formulario basada en tal esquema y muestra un mensaje de error en el que recomienda cambiar el tipo **ENTITY** por el tipo **NCName** del que deriva **ENTITY**. 
  
> [!NOTE]
>  [!NOTA] Si crea manualmente una plantilla de formulario de InfoPath fuera del modo de diseño y la plantilla usa un XSD que incluye los tipos **ENTITY** y **ENTITIES**, la plantilla funcionará en tiempo de ejecución si el archivo Template.xml contiene la definición de tipo de documento necesaria para estos tipos. 
  
## <a name="required-xsdany-element"></a>Elemento xsd:any obligatorio

La aparición de un elemento comodín **xsd:any**, es decir, la aparición de un elemento **xsd:any** con un valor del atributo **minOccurs** mayor que cero ("se requiere alguno"), evita que InfoPath cree de manera determinista una instancia válida para este fragmento del esquema. InfoPath debe poder crear una instancia válida cuando genere un formulario que usa este fragmento del esquema. Como parte de la ejecución del **Asistente del origen de datos**, los esquemas con elementos **xsd:any** necesarios exigen que se elija qué elemento del esquema se desea usar en lugar del elemento **xsd:any** obligatorio. 
  
## <a name="elements-with-an-abstract-complex-type"></a>Elementos con un tipo complejo abstracto

El modo de diseño de InfoPath admite diseñar una plantilla de formulario basada en esquemas que usen tipos complejos abstractos. Por ejemplo, si un elemento denominado  `shippingAddress` tiene un tipo complejo abstracto denominado  `address` que tiene dos derivaciones,  `USAddress` y  `CanadianAddress`, InfoPath trata cualquier instancia de  `shippingAddress` como una elección entre  `shippingAddress` con el tipo  `USAddress` y  `shippingAddress` con el tipo  `CanadianAddress`. En este ejemplo, si los esquemas proporcionados no contienen tipos que deriven de la dirección, entonces InfoPath solicita un esquema adicional que satisfaga este requisito. 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>Construcciones XSD con funcionalidad reducida

En las secciones siguientes se describen las construcciones XSD que tienen funcionalidad reducida cuando se usan para crear plantillas de formulario en el diseñador de formularios de InfoPath.
  
## <a name="substitution-groups"></a>Grupos de sustitución

Todos los miembros del grupo de sustitución aparecen en el panel de tareas **Campos**. InfoPath representa las posibilidades de sustitución como una opción de todos los grupos de sustitución (incluido el elemento definitorio, si no es abstracto). Si no hay grupos de sustitución para un elemento abstracto, InfoPath solicita que se proporcione un esquema que contenga al menos un elemento que sea un grupo de sustitución. 
  
## <a name="unbounded-choice-elements"></a>Elementos de opciones no enlazados

En el fragmento de esquema siguiente se muestra un elemento de opciones no enlazado:
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

InfoPath muestra elementos de opciones extensibles como opciones extensibles en el panel de tareas **Campos**. Hay un control **Grupo de opciones extensible** que se puede usar para representar la lista heterogénea definida por el elemento de opciones extensible en el XSD. 
  
## <a name="repeating-sequence"></a>Secuencia extensible

En el fragmento de esquema siguiente se muestra una secuencia extensible:
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

Siempre que la secuencia extensible contenga un elemento obligatorio, InfoPath carga el XSD sin modificarlo y permite enlazar controles de sección extensibles con la secuencia extensible.
  
## <a name="choice-of-model-groups"></a>Opción de grupos de modelos

En el fragmento de esquema siguiente se muestra el elemento de opción que contiene varios grupos de modelos:
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

El modo de diseño de InfoPath admite construcciones XSD sin necesidad de efectuar ninguna modificación en el diseñador de formularios. Al no modificar el significado del esquema, InfoPath simplifica la construcción de opción anterior en una opción única equivalente contraída en el panel de tareas **Campos**. 
  
## <a name="optional-sibling-with-same-qualified-name"></a>Elemento opcional del mismo nivel con el mismo nombre completo

En el fragmento de esquema siguiente se muestra un elemento del mismo nivel opcional con el mismo nombre completo (`QName`):
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

Las expresiones **XPath** de estos nodos pueden ser complejas porque cada posible instancia XML debe estar justificada en el diseñador de formularios de InfoPath. InfoPath no expone aquellas partes del esquema en las que pueda tener dificultades al crear los enlaces **XPath** correctos. Se muestran advertencias sobre las partes del esquema que se omiten. 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>Construcciones XSD con significado especial en InfoPath

En las secciones siguientes se describen las construcciones XSD que tienen significado especial cuando se usan para crear una plantilla de formulario en modo de diseño. En estas secciones se describe cómo se usan loas construcciones en el esquema para habilitar algunos comportamientos.
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>Agregar nuevos grupos y campos de elementos con el panel de tareas Campos

Puede construir el esquema de manera que se pueda usar el panel de tareas **Campos** para agregar nuevos campos y grupos de elementos en tiempo de ejecución. Para ello, declare un elemento del esquema con un elemento **xsd:any** opcional, no enlazado, que especifique el atributo de espacio de nombres con el comodín **##any**. A continuación, en modo de diseño, puede usar el panel de tareas **Campos** para agregar nuevos grupos y campos de elementos a ese elemento. Por ejemplo, podría agregar nuevo contenido al elemento siguiente: 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>Agregar nuevos campos de atributos con el panel de tareas Campos

Al igual que en el caso de los elementos, puede declarar un atributo con un elemento **anyAttribute** que tenga el atributo de espacio de nombres especificado como el comodín **##any**. En tiempo de diseño, puede usar el panel de tareas **Campos** para agregar nuevo contenido a ese atributo del esquema. 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>Almacenar firmas XML en orígenes de datos

Para permitir que los usuarios firmen digitalmente un formulario en tiempo de ejecución, el esquema del origen de datos debe declarar un elemento denominado firma para almacenar la información de las firmas XML (firma digital) que se crea cuando un usuario firma el formulario. Esta declaración se hace con el elemento **xsd:any** con el atributo de espacio de nombres especificado como espacio de nombres de firmas XML con un carácter de comodín, del modo siguiente: "http://www.w3c.org/2000/09/xmldsig#" 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a>Enlazar un campo a un control de cuadro de texto enriquecido

 Los controles de **Cuadro de texto enriquecido** en InfoPath generan XHTML genérico; por lo tanto, en el esquema se debe especificar que son válidos cualquier cantidad de texto y de nodos XHTML en el XML de la instancia del formulario. Se consigue hacer esta especificación con la siguiente construcción XSD: 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="http://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> [!NOTA] InfoPath nunca modifica el contenido del archivo de esquema (.xsd), pero se puede inferir lógicamente un subconjunto del mismo para fines de diseño. El archivo de esquema permanece inalterado dentro de la plantilla de formulario tanto en tiempo de diseño como en tiempo de ejecución. 
  
## <a name="debugging-common-xsd-errors"></a>Depurar errores de XSD habituales

Si en el diseñador de formularios de InfoPath carga archivos XSD creados externamente, es posible que reciba alguno de estos dos mensajes de error: mensajes de error de MSXML o mensajes de error de InfoPath. Los mensajes de error de MSXML aparecen en la sección **Detalles** del cuadro de diálogo de mensajes de error de InfoPath y siempre comienzan con una referencia al nombre o la ruta de acceso del archivo de esquema que causa el error. Algunas construcciones de esquema XSD válidos no se admiten en InfoPath; éstas se comentan en la sección Construcciones XSD no admitidas. En las secciones siguientes se describen algunos errores habituales que pueden provocar que los esquemas no se carguen correctamente en InfoPath. 
  
## <a name="the-xsd-namespace-declaration"></a>Declaración del espacio de nombres XSD

Al igual que todos los estándares W3C, los esquemas XML (XSD) completaron un largo proceso de revisión antes de ser recomendados. Hubo muchos borradores de trabajo y se escribieron muchos archivos XSD basados en estos estándares en desarrollo. Durante este proceso, Microsoft creó un lenguaje de esquema propio al que denominó XDR (XML-Data Reduced) y que se incluyó con MSXML 3.0. Desde el lanzamiento de MSXML 4.0, Microsoft XML Core Services admite la recomendación completa de XSD. Muchos programas de creación de esquemas no esperaron a que XSD se convirtiera en una recomendación completa. Las versiones anteriores de estos programas pueden producir archivos XSD obsoletos que la infraestructura de MSXML 5.0, de la que depende InfoPath, no admite.
  
Para asegurar que un archivo XSD admite la recomendación XSD completa, debe contener la siguiente declaración de espacio de nombres XML en la etiqueta \<schema\>:
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

Al igual que todas las declaraciones de espacios de nombres XML, el prefijo XML (en este caso "xsd") puede ser cualquier cadena de prefijo válida. Algunos prefijos habituales que se pueden ver en la práctica son "xsd", "xs" y "" (sin prefijo). Por lo general, MSXML informa de un error referente a que la raíz no está adecuadamente definida si falta esta declaración del espacio de nombres.
  
## <a name="importing-and-including-schemas"></a>Importar e incluir esquemas

Los esquemas XSD son extensibles y pueden importar e incluir otros esquemas. En general, se debe importar un esquema si el esquema especificado en el atributo **targetNamespace** es distinto del esquema actual. Se debería incluir si el esquema especificado en el atributo **targetNamespace** es el mismo que el esquema actual. 
  
La semántica para importar e incluir esquemas es la siguiente:
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

Si falta el atributo **schemaLocation** (como sucede con algunos convertidores), MSXML devuelve un error porque no encuentra el archivo. Si recibe este error, compruebe también que otros usuarios de la plantilla de formulario pueden tener acceso al recurso o ubicación especificados en el atributo schemaLocation. Lógicamente, se producirán errores si el atributo **schemaLocation** hace referencia a un servidor o directorio que está averiado o no existe, o si los usuarios no tienen permisos de acceso. Asegúrese también de examinar todos los esquemas importados e incluidos para comprobar que son válidos. 
  
> [!NOTE]
> [!NOTA] Los errores causados por problemas con el atributo **schemaLocation** son problemáticos solo cuando InfoPath importa primero los esquemas; es decir, cuando se comienza a diseñar un formulario basado en un esquema existente. Después de esto, InfoPath trabaja con versiones almacenadas en memoria caché de los archivos de esquema que están en la plantilla del formulario. 
  
Un atributo de espacio de nombres vacío se permite cuando se importa un esquema que no especifica un atributo **targetNamespace**. En general, el espacio de nombres del esquema importado debe coincidir con el **targetNamespace** especificado en el esquema que se desea importar. 
  
## <a name="nondeterministic-schemas"></a>Esquemas no deterministas

La infraestructura de MSXML 5.0 de la que depende InfoPath detecta y devuelve errores para advertir de esquemas no deterministas, pero el mensaje de error resultante no proporciona un número de línea que indique qué parte del esquema está generando el error. En esta sección se comenta por qué es importante para los archivos de esquema XSD ser deterministas y lo que significa ser no determinista. También se muestran algunos errores comunes que conviene evitar.
  
Los esquemas XSD existen con el fin de validar la estructura de datos XML y la semántica de tipos. Para llevar a cabo esta tarea, el sistema de validación (en este caso, MSXML 5.0) debe asignar los nodos XML a las declaraciones XSD. Sin esta asignación, el sistema de validación no puede llevar a cabo su tarea. Si se puede garantizar la asignación, entonces el esquema es determinista. Si hay una única instancia XML que imposibilita esta asignación, entonces el esquema es no determinista.
  
En el ejemplo siguiente el esquema es no determinista:
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

Para explicar por qué este segmento de XSD es no determinista, supongamos que tiene el siguiente fragmento de XML que desea validar con este esquema:
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

En este fragmento de XML, no está claro si el elemento  *\<file_path\>*  es el nodo obligatorio de esta primera parte de la declaración de opción o el opcional de la segunda parte de la declaración de opción. Esta distinción es importante por las razones siguientes: 
  
1. Si el fragmento de XML se valida frente a la primera parte de la declaración de opción, entonces el XML es valido para el esquema.
    
2. Si el fragmento de XML se valida frente a la segunda parte de la declaración de opción, entonces el esquema no es valido porque falta el nodo \<URI\> obligatorio. 
    
Algunos sistemas de validación de XSD caen en el error de validar frente a este esquema porque existe una ruta de acceso válida. MSXML es más estricto y devuelve un error en el que indica que el esquema es no determinista.
  
A continuación, se ofrecen unos cuantos ejemplos más de esquemas no deterministas. El primero se ocupa de elementos opcionales. Estos casos proceden a menudo de convertidores XDR a XSD por las diferencias en la cardinalidad predeterminada de los dos lenguajes de esquema. El primer caso que hay que tener en cuenta son los elementos opcionales declarados con los elementos **xsd:choice** y **xsd:sequence**. Los elementos opcionales declarados en un elemento **xsd:sequence** se validan, por lo general, de forma correcta, siempre que no haya otros elementos con el mismo nombre repetidos solo con elementos opcionales en ellos. Por ejemplo: 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

Para comprender por qué este segmento del esquema es no determinista, suponga que tiene el siguiente fragmento de XML no válido:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

Si se observa el fragmento, se puede ver por qué no es válido: hay dos elementos  `<aNode>` antes del elemento  `<anotherNode>`, cuando solo puede haber uno. 
  
Ahora suponga que tiene la siguiente instancia XML que validar:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

El reto está en determinar si esta instancia es válida. ¿Tiene dos elementos  `<aNode>` donde solo se permite uno, o tiene un elemento  `<aNode>` y otro elemento donde se permiten? El esquema es no determinista porque no hay forma de saberlo. 
  
De igual modo, los elementos opcionales declarados en un elemento **xsd:choice** son, generalmente, problemáticos. En el siguiente ejemplo simplificado, no hay manera de saber si la opción se produjo una vez sin que estuviera presente el elemento opcional o si nunca se produjo. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

La última práctica cuestionable es el uso de un elemento **xsd:any** sin una definición de espacio de nombres, como en  `<xsd:any namespace="##other"/>`, después de un elemento **xsd:sequence**. Esta construcción es especialmente problemática cuando va después de un elemento opcional. Si volvemos al ejemplo anterior y cambiamos solo el último nodo por un elemento **xsd:any**, podemos ver que todos los argumentos previos sobre no determinismo siguen estando vigentes, del siguiente modo: 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a>Valores de enumeración no válidos

Los esquemas XSD por lo general no efectúan ninguna validación de tipos hasta que se valida un documento de instancia real. La excepción ocurre cuando hay una enumeración en el esquema. En este caso, el esquema valida los valores de enumeración frente a los tipos de enumeración para asegurar que son valores de nodo correctos. A continuación, se indican dos ejemplos:
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Este esquema no es válido porque "eleven o'clock" no es un valor válido para un elemento del tipo **xsd:time**.
  
El siguiente es un ejemplo más complejo:
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Para entender por qué este ejemplo no es válido, debe comprender cómo se define el tipo **xsd:NMTOKEN**. La especificación de tipos de datos W3C define el tipo **NMTOKEN** como sigue: "Un NMTOKEN (token de nombre) es una combinación de los caracteres del nombre". 
  
Si investiga más a fondo, encontrará ' &' no es un carácter de nombre válido y, por lo tanto, "M & Ms" no valida como un tipo **NMTOKEN** . 
  
## <a name="empty-sequence-or-choice-elements"></a>Elementos de opción o secuencia vacíos

A veces, MSXML devuelve errores sobre las declaraciones de esquema que contienen elementos **xsd:choice** o **xsd:sequence** vacíos, como se muestra en el ejemplo siguiente. 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

Al quitar la etiqueta  `<xsd:choice />` vacía, se debería solucionar el problema. 
  
## <a name="regular-expressions"></a>Expresiones regulares

MSXML 5.0 puede tener problemas cuando valida modelos de expresiones regulares durante la carga. Las expresiones regulares pueden ser complicadas y hay que tener precaución al usarlas. Cada analizador XSD parece tener lenguajes de expresiones regulares flexibles; es decir, implementan el lenguaje de expresiones regulares XSD oficial junto con los elementos de otros lenguajes de expresiones regulares. Si el diseñador de formularios de InfoPath tiene problemas al analizar una expresión regular, los datos de muestra que genera pueden no ser válidos o no llegar a generarse en absoluto. Esto es aceptable en tiempo de diseño, porque InfoPath solo usa datos de muestra para fines de formato. Ahora bien, si se usa una expresión regular que MSXML no admite, InfoPath no puede usarla para validar un valor cuando el usuario está rellenando un formulario. En [Esquema XML Parte 0: Primera, segunda edición](http://www.w3.org/TR/xmlschema-0/) se describe lo que se admite en las expresiones regulares XSD. Para obtener más información sobre las expresiones regulares XSD y las expresiones regulares de nivel 1 de Unicode, vea las [Expresiones habituales de Unicode](http://www.unicode.org/reports/tr18/). 
  
## <a name="targetnamespace-attribute-issues"></a>Problemas con el atributo targetNamespace

XSD es interesante en el sentido de que, de manera predeterminada, el atributo **targetNamespace** se refiere únicamente a las declaraciones de nivel superior, aunque se puede establecer  `attributeFormDefault=qualified` y  `elementFormDefault=qualified` para invalidar este comportamiento predeterminado. Como ejemplo, suponga que tiene el siguiente XSD. 
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

Y que el documento de instancia XML se parece a este ejemplo.
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

Las definiciones locales no requieren el espacio de nombres de destino porque la cualificación de nombre completo está deshabilitada de manera predeterminada. Sin embargo, si cambia la definición local para que sea global, entonces la referencia debe completarse con el prefijo del espacio de nombres. Por ejemplo, el esquema siguiente no es válido.
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

Este esquema no es válido porque "global" está en el espacio de nombres "http://ns". La simple ref="global" no se reconoce porque el espacio de nombres predeterminado no es "http://ns". Para solucionarlo, debe agregar un prefijo al espacio de nombres de destino y usarlo en todos las referencias globales y usos de tipos. El esquema correcto se muestra a continuación.
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
    xmlns:ns="http://ns" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

Si su esquema tiene especificado el atributo **targetNamespace**, asegúrese de que todas las referencias globales están completas con el prefijo del espacio de nombres correcto. 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>Codificación de instrucciones de procesamiento XML (Unicode o ANSII)

XML admite conjuntos de caracteres Unicode. Por consiguiente, puede perder información si guarda archivos que usan caracteres ANSII. Sin embargo, guardar los archivos como UTF-16 puede resultar excesivo según el uso que se vaya a dar. Para reducir el costo de implementación de un lector XML, el autor del XML debe enunciar la codificación que se usa en la instrucción de procesamiento XML de nivel superior. Tal vez reconozca la siguiente instrucción de procesamiento.
  
```XML
xml version="1.0" encoding="UTF-8"
```

Esta etiqueta de instrucción de procesamiento especifica que la codificación del archivo es UTF-8. Debe asegurarse de que la codificación del archivo es la misma que la que se enuncia en la etiqueta de la instrucción de procesamiento. Puede determinar cuál es la codificación observando los bytes del archivo y buscando las marcas de orden de bytes Unicode. No obstante, hay una forma más sencilla. Si tiene problemas para abrir un esquema XSD, especifique la codificación "UTF-8", ábralo en un editor de texto como Bloc de notas y después guarde el archivo usando la codificación UTF-8 (Bloc de notas ofrece la lista desplegable **Codificación** en el cuadro de diálogo **Guardar como**). Si continúa teniendo problemas para abrir el archivo, no se trata de un problema de codificación. 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>Atributo maxOccurs dentro del elemento xsd:all

Debido al modo en que se define el no determinismo en la recomendación del esquema XML, el único valor válido para el atributo **maxOccurs** de un elemento **xsd:element** dentro de un elemento **xsd:all** es 1. Por ejemplo, lo siguiente es válido. 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

Sin embargo, este ejemplo no es válido.
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

Este ejemplo no es válido porque el sistema de validación no puede determinar si se asignan dos apariciones de  `<x/>` a la declaración única o a la declaración y a otra definición no válida. Del mismo modo, no se pueden tener dos elementos con el mismo nombre en una etiqueta  `<xsd:all>`. 
  
Este ejemplo también es interesante porque permite tener cualquier número de nodos  `<x/>` y  `<docs/>` dentro de un elemento contenedor en cualquier orden. Aunque esta construcción no es válida, existe una solución: con el elemento **xsd:choice** puede conseguir el mismo resultado, como se demuestra a continuación. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Cómo modificar o crear un XSD para InfoPath

Los dos ejemplos de las siguientes secciones muestran cómo modificar o crear un esquema para producir resultados concretos en InfoPath.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Permitir la inserción de elementos definidos por el usuario en el panel de tareas Campos

Para permitir que los elementos definidos por el usuario aparezcan bajo un elemento principal en el panel de tareas **Campos**, debe insertar un elemento **xsd:any** bajo el elemento principal. Para permitir insertar elementos definidos por el usuario dentro de  `<your_node_name>` , la declaración XSD debería parecerse a lo siguiente. 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

Si también desea permitir atributos definidos por el usuario, debe agregar  `<xsd:anyAttribute namespace="##any | ##other"/>` a la declaración del elemento. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Permitir enlazar elementos de texto enriquecido en los modos de diseño y de edición de InfoPath

Si desea declarar un elemento que se pueda enlazar a un control **Rich Text Box**, debe tener el formulario siguiente, que incluye el elemento **xsd:any** que tiene un atributo de espacio de nombres establecido en "http://www.w3.org/1999/xhtml", como se muestra en el ejemplo siguiente. 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a>Conclusión

Aprovechando las ventajas que presenta InfoPath para diseñar soluciones de formulario XML que se basan en archivos de esquema XML (.xsd) creados externamente, puede crear una plantilla de formulario que funcione con un esquema estándar de la industria o con un esquema personalizado creado en su compañía u organización. Con la información proporcionada en este artículo, puede crear archivos de esquema XSD personalizados compatibles con InfoPath y solucionar problemas habituales que pueden producirse cuando se cargan archivos XSD creados externamente en el entorno de diseño de InfoPath.
  
## <a name="see-also"></a>Vea también

- [Esquema XML W3C ](http://www.w3.org/XML/Schema)
- [Esquema W3C XML Primer](http://www.w3.org/TR/xmlschema-0/)
- [Referencia de estructuras de Esquema W3C XML](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [Referencia de tipos de datos de esquema W3C XML](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [Tutorial del esquema XML](http://www.w3schools.com/schema/default.asp)
- [Centro de programadores de XML](http://msdn.microsoft.com/en-us/xml/default.aspx)

