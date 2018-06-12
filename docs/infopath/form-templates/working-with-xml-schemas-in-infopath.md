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
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="d1460-104">Trabajo con esquemas XML en InfoPath</span><span class="sxs-lookup"><span data-stu-id="d1460-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="d1460-p102">Las plantillas de formulario que se crean con Microsoft InfoPath usan un esquema XML (XSD) para llevar a cabo la validación estructural y de datos en el XML que entra, se modifica y sale de un formulario de InfoPath. Todas las plantillas de formulario creadas en el diseñador de formularios de InfoPath contienen por lo menos un archivo de esquema XSD (.xsd) que se usa para la validación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d1460-p102">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form. Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d1460-p103">[!NOTA] La información que se presenta en este tema se aplica a las plantillas de formulario diseñadas para su uso en el editor de InfoPath. Las plantillas de formulario compatibles con el explorador tienen requisitos de esquema XSD más estrictos. Para obtener más información, vea la documentación sobre los esquemas XML en plantillas de formulario compatibles con el explorador disponible en MSDN.</span><span class="sxs-lookup"><span data-stu-id="d1460-p103">The information contained in this topic applies to form templates designed for use in the InfoPath editor. Browser-compatible form templates have stricter XSD Schema requirements. For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="d1460-110">Uso de esquemas XML creados externamente</span><span class="sxs-lookup"><span data-stu-id="d1460-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="d1460-111">Para cargar un archivo de esquema XSD que no se haya creado en InfoPath, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d1460-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="d1460-112">Para crear una plantilla de formulario basada en un esquema externo</span><span class="sxs-lookup"><span data-stu-id="d1460-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="d1460-113">En Backstage, haga clic en **Nuevo**, haga clic en **XML o Esquema** bajo **Plantillas de formulario avanzadas** y, por último, haga clic en **Diseñar este formulario**.</span><span class="sxs-lookup"><span data-stu-id="d1460-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="d1460-114">En el **Asistente del origen de datos**, especifique el archivo de esquema XSD que desea usar y haga clic en **Siguiente** para completar las páginas restantes del asistente.</span><span class="sxs-lookup"><span data-stu-id="d1460-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="d1460-115">Construcciones XSD no admitidas</span><span class="sxs-lookup"><span data-stu-id="d1460-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="d1460-p104">En las secciones siguientes se describen las construcciones XSD que InfoPath no puede controlar en tiempo de ejecución. Evite estas construcciones cuando cree una plantilla de formulario en el diseñador de formularios de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d1460-p104">The following sections describe XSD constructs that InfoPath cannot handle at run time. Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="d1460-118">Tipos ENTITY y ENTITIES</span><span class="sxs-lookup"><span data-stu-id="d1460-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="d1460-p105">Los tipos **ENTITY** y **ENTITIES** requieren una definición de tipo de documento (DTD) para validación que no es compatible con InfoPath. InfoPath no permite diseñar una plantilla de formulario basada en tal esquema y muestra un mensaje de error en el que recomienda cambiar el tipo **ENTITY** por el tipo **NCName** del que deriva **ENTITY**.</span><span class="sxs-lookup"><span data-stu-id="d1460-p105">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support. InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="d1460-121">[!NOTA] Si crea manualmente una plantilla de formulario de InfoPath fuera del modo de diseño y la plantilla usa un XSD que incluye los tipos **ENTITY** y **ENTITIES**, la plantilla funcionará en tiempo de ejecución si el archivo Template.xml contiene la definición de tipo de documento necesaria para estos tipos.</span><span class="sxs-lookup"><span data-stu-id="d1460-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="d1460-122">Elemento xsd:any obligatorio</span><span class="sxs-lookup"><span data-stu-id="d1460-122">Required xsd:any Element</span></span>

<span data-ttu-id="d1460-p106">La aparición de un elemento comodín **xsd:any**, es decir, la aparición de un elemento **xsd:any** con un valor del atributo **minOccurs** mayor que cero ("se requiere alguno"), evita que InfoPath cree de manera determinista una instancia válida para este fragmento del esquema. InfoPath debe poder crear una instancia válida cuando genere un formulario que usa este fragmento del esquema. Como parte de la ejecución del **Asistente del origen de datos**, los esquemas con elementos **xsd:any** necesarios exigen que se elija qué elemento del esquema se desea usar en lugar del elemento **xsd:any** obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d1460-p106">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment. InfoPath must be able to create a valid instance when generating a form that uses this schema fragment. As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="d1460-126">Elementos con un tipo complejo abstracto</span><span class="sxs-lookup"><span data-stu-id="d1460-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="d1460-p107">El modo de diseño de InfoPath admite diseñar una plantilla de formulario basada en esquemas que usen tipos complejos abstractos. Por ejemplo, si un elemento denominado  `shippingAddress` tiene un tipo complejo abstracto denominado  `address` que tiene dos derivaciones,  `USAddress` y  `CanadianAddress`, InfoPath trata cualquier instancia de  `shippingAddress` como una elección entre  `shippingAddress` con el tipo  `USAddress` y  `shippingAddress` con el tipo  `CanadianAddress`. En este ejemplo, si los esquemas proporcionados no contienen tipos que deriven de la dirección, entonces InfoPath solicita un esquema adicional que satisfaga este requisito.</span><span class="sxs-lookup"><span data-stu-id="d1460-p107">InfoPath design mode supports designing a form template against schemas that use abstract complex types. For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` . In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="d1460-130">Construcciones XSD con funcionalidad reducida</span><span class="sxs-lookup"><span data-stu-id="d1460-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="d1460-131">En las secciones siguientes se describen las construcciones XSD que tienen funcionalidad reducida cuando se usan para crear plantillas de formulario en el diseñador de formularios de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d1460-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="d1460-132">Grupos de sustitución</span><span class="sxs-lookup"><span data-stu-id="d1460-132">Substitution Groups</span></span>

<span data-ttu-id="d1460-p108">Todos los miembros del grupo de sustitución aparecen en el panel de tareas **Campos**. InfoPath representa las posibilidades de sustitución como una opción de todos los grupos de sustitución (incluido el elemento definitorio, si no es abstracto). Si no hay grupos de sustitución para un elemento abstracto, InfoPath solicita que se proporcione un esquema que contenga al menos un elemento que sea un grupo de sustitución.</span><span class="sxs-lookup"><span data-stu-id="d1460-p108">All members of the substitution group appear in the **Fields** task pane. InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract). If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="d1460-136">Elementos de opciones no enlazados</span><span class="sxs-lookup"><span data-stu-id="d1460-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="d1460-137">En el fragmento de esquema siguiente se muestra un elemento de opciones no enlazado:</span><span class="sxs-lookup"><span data-stu-id="d1460-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="d1460-p109">InfoPath muestra elementos de opciones extensibles como opciones extensibles en el panel de tareas **Campos**. Hay un control **Grupo de opciones extensible** que se puede usar para representar la lista heterogénea definida por el elemento de opciones extensible en el XSD.</span><span class="sxs-lookup"><span data-stu-id="d1460-p109">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane. There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="d1460-140">Secuencia extensible</span><span class="sxs-lookup"><span data-stu-id="d1460-140">Repeating Sequence</span></span>

<span data-ttu-id="d1460-141">En el fragmento de esquema siguiente se muestra una secuencia extensible:</span><span class="sxs-lookup"><span data-stu-id="d1460-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="d1460-142">Siempre que la secuencia extensible contenga un elemento obligatorio, InfoPath carga el XSD sin modificarlo y permite enlazar controles de sección extensibles con la secuencia extensible.</span><span class="sxs-lookup"><span data-stu-id="d1460-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="d1460-143">Opción de grupos de modelos</span><span class="sxs-lookup"><span data-stu-id="d1460-143">Choice of Model Groups</span></span>

<span data-ttu-id="d1460-144">En el fragmento de esquema siguiente se muestra el elemento de opción que contiene varios grupos de modelos:</span><span class="sxs-lookup"><span data-stu-id="d1460-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="d1460-p110">El modo de diseño de InfoPath admite construcciones XSD sin necesidad de efectuar ninguna modificación en el diseñador de formularios. Al no modificar el significado del esquema, InfoPath simplifica la construcción de opción anterior en una opción única equivalente contraída en el panel de tareas **Campos**.</span><span class="sxs-lookup"><span data-stu-id="d1460-p110">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer. While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="d1460-147">Elemento opcional del mismo nivel con el mismo nombre completo</span><span class="sxs-lookup"><span data-stu-id="d1460-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="d1460-148">En el fragmento de esquema siguiente se muestra un elemento del mismo nivel opcional con el mismo nombre completo (`QName`):</span><span class="sxs-lookup"><span data-stu-id="d1460-148">The following schema fragment shows an optional sibling with same qualified name (`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="d1460-p111">Las expresiones **XPath** de estos nodos pueden ser complejas porque cada posible instancia XML debe estar justificada en el diseñador de formularios de InfoPath. InfoPath no expone aquellas partes del esquema en las que pueda tener dificultades al crear los enlaces **XPath** correctos. Se muestran advertencias sobre las partes del esquema que se omiten.</span><span class="sxs-lookup"><span data-stu-id="d1460-p111">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer. InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings. Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="d1460-152">Construcciones XSD con significado especial en InfoPath</span><span class="sxs-lookup"><span data-stu-id="d1460-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="d1460-p112">En las secciones siguientes se describen las construcciones XSD que tienen significado especial cuando se usan para crear una plantilla de formulario en modo de diseño. En estas secciones se describe cómo se usan loas construcciones en el esquema para habilitar algunos comportamientos.</span><span class="sxs-lookup"><span data-stu-id="d1460-p112">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode. These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="d1460-155">Agregar nuevos grupos y campos de elementos con el panel de tareas Campos</span><span class="sxs-lookup"><span data-stu-id="d1460-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="d1460-p113">Puede construir el esquema de manera que se pueda usar el panel de tareas **Campos** para agregar nuevos campos y grupos de elementos en tiempo de ejecución. Para ello, declare un elemento del esquema con un elemento **xsd:any** opcional, no enlazado, que especifique el atributo de espacio de nombres con el comodín **##any**. A continuación, en modo de diseño, puede usar el panel de tareas **Campos** para agregar nuevos grupos y campos de elementos a ese elemento. Por ejemplo, podría agregar nuevo contenido al elemento siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1460-p113">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time. To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard. Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element. For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="d1460-160">Agregar nuevos campos de atributos con el panel de tareas Campos</span><span class="sxs-lookup"><span data-stu-id="d1460-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="d1460-p114">Al igual que en el caso de los elementos, puede declarar un atributo con un elemento **anyAttribute** que tenga el atributo de espacio de nombres especificado como el comodín **##any**. En tiempo de diseño, puede usar el panel de tareas **Campos** para agregar nuevo contenido a ese atributo del esquema.</span><span class="sxs-lookup"><span data-stu-id="d1460-p114">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard. At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="d1460-163">Almacenar firmas XML en orígenes de datos</span><span class="sxs-lookup"><span data-stu-id="d1460-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="d1460-p115">Para permitir que los usuarios firmen digitalmente un formulario en tiempo de ejecución, el esquema del origen de datos debe declarar un elemento denominado firma para almacenar la información de las firmas XML (firma digital) que se crea cuando un usuario firma el formulario. Esta declaración se hace con el elemento **xsd:any** con el atributo de espacio de nombres especificado como espacio de nombres de firmas XML con un carácter de comodín, del modo siguiente: "http://www.w3c.org/2000/09/xmldsig#"</span><span class="sxs-lookup"><span data-stu-id="d1460-p115">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form. You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "http://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
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

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="d1460-166">Enlazar un campo a un control de cuadro de texto enriquecido</span><span class="sxs-lookup"><span data-stu-id="d1460-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="d1460-p116">Los controles de **Cuadro de texto enriquecido** en InfoPath generan XHTML genérico; por lo tanto, en el esquema se debe especificar que son válidos cualquier cantidad de texto y de nodos XHTML en el XML de la instancia del formulario. Se consigue hacer esta especificación con la siguiente construcción XSD:</span><span class="sxs-lookup"><span data-stu-id="d1460-p116">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance. You can achieve this specification with the following XSD construct:</span></span> 
  
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
> <span data-ttu-id="d1460-p117">[!NOTA] InfoPath nunca modifica el contenido del archivo de esquema (.xsd), pero se puede inferir lógicamente un subconjunto del mismo para fines de diseño. El archivo de esquema permanece inalterado dentro de la plantilla de formulario tanto en tiempo de diseño como en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d1460-p117">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes. The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="d1460-171">Depurar errores de XSD habituales</span><span class="sxs-lookup"><span data-stu-id="d1460-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="d1460-p118">Si en el diseñador de formularios de InfoPath carga archivos XSD creados externamente, es posible que reciba alguno de estos dos mensajes de error: mensajes de error de MSXML o mensajes de error de InfoPath. Los mensajes de error de MSXML aparecen en la sección **Detalles** del cuadro de diálogo de mensajes de error de InfoPath y siempre comienzan con una referencia al nombre o la ruta de acceso del archivo de esquema que causa el error. Algunas construcciones de esquema XSD válidos no se admiten en InfoPath; éstas se comentan en la sección Construcciones XSD no admitidas. En las secciones siguientes se describen algunos errores habituales que pueden provocar que los esquemas no se carguen correctamente en InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d1460-p118">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages. MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error. Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section. The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="d1460-176">Declaración del espacio de nombres XSD</span><span class="sxs-lookup"><span data-stu-id="d1460-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="d1460-p119">Al igual que todos los estándares W3C, los esquemas XML (XSD) completaron un largo proceso de revisión antes de ser recomendados. Hubo muchos borradores de trabajo y se escribieron muchos archivos XSD basados en estos estándares en desarrollo. Durante este proceso, Microsoft creó un lenguaje de esquema propio al que denominó XDR (XML-Data Reduced) y que se incluyó con MSXML 3.0. Desde el lanzamiento de MSXML 4.0, Microsoft XML Core Services admite la recomendación completa de XSD. Muchos programas de creación de esquemas no esperaron a que XSD se convirtiera en una recomendación completa. Las versiones anteriores de estos programas pueden producir archivos XSD obsoletos que la infraestructura de MSXML 5.0, de la que depende InfoPath, no admite.</span><span class="sxs-lookup"><span data-stu-id="d1460-p119">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation. There were many working drafts, and consequently, many XSD files were written based on these evolving standards. During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0. Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD. Many programs for creating schemas did not wait for XSD to become a full recommendation. Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="d1460-183">Para asegurar que un archivo XSD admite la recomendación XSD completa, debe contener la siguiente declaración de espacio de nombres XML en la etiqueta \<schema\>:</span><span class="sxs-lookup"><span data-stu-id="d1460-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="d1460-p120">Al igual que todas las declaraciones de espacios de nombres XML, el prefijo XML (en este caso "xsd") puede ser cualquier cadena de prefijo válida. Algunos prefijos habituales que se pueden ver en la práctica son "xsd", "xs" y "" (sin prefijo). Por lo general, MSXML informa de un error referente a que la raíz no está adecuadamente definida si falta esta declaración del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d1460-p120">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string. Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix). MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="d1460-187">Importar e incluir esquemas</span><span class="sxs-lookup"><span data-stu-id="d1460-187">Importing and Including Schemas</span></span>

<span data-ttu-id="d1460-p121">Los esquemas XSD son extensibles y pueden importar e incluir otros esquemas. En general, se debe importar un esquema si el esquema especificado en el atributo **targetNamespace** es distinto del esquema actual. Se debería incluir si el esquema especificado en el atributo **targetNamespace** es el mismo que el esquema actual.</span><span class="sxs-lookup"><span data-stu-id="d1460-p121">XSD schemas are extensible and can import and include other schemas. Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema. You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="d1460-191">La semántica para importar e incluir esquemas es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1460-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="d1460-p122">Si falta el atributo **schemaLocation** (como sucede con algunos convertidores), MSXML devuelve un error porque no encuentra el archivo. Si recibe este error, compruebe también que otros usuarios de la plantilla de formulario pueden tener acceso al recurso o ubicación especificados en el atributo schemaLocation. Lógicamente, se producirán errores si el atributo **schemaLocation** hace referencia a un servidor o directorio que está averiado o no existe, o si los usuarios no tienen permisos de acceso. Asegúrese también de examinar todos los esquemas importados e incluidos para comprobar que son válidos.</span><span class="sxs-lookup"><span data-stu-id="d1460-p122">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file. If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template. Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions. Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d1460-p123">[!NOTA] Los errores causados por problemas con el atributo **schemaLocation** son problemáticos solo cuando InfoPath importa primero los esquemas; es decir, cuando se comienza a diseñar un formulario basado en un esquema existente. Después de esto, InfoPath trabaja con versiones almacenadas en memoria caché de los archivos de esquema que están en la plantilla del formulario.</span><span class="sxs-lookup"><span data-stu-id="d1460-p123">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema. After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="d1460-p124">Un atributo de espacio de nombres vacío se permite cuando se importa un esquema que no especifica un atributo **targetNamespace**. En general, el espacio de nombres del esquema importado debe coincidir con el **targetNamespace** especificado en el esquema que se desea importar.</span><span class="sxs-lookup"><span data-stu-id="d1460-p124">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute. In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="d1460-200">Esquemas no deterministas</span><span class="sxs-lookup"><span data-stu-id="d1460-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="d1460-p125">La infraestructura de MSXML 5.0 de la que depende InfoPath detecta y devuelve errores para advertir de esquemas no deterministas, pero el mensaje de error resultante no proporciona un número de línea que indique qué parte del esquema está generando el error. En esta sección se comenta por qué es importante para los archivos de esquema XSD ser deterministas y lo que significa ser no determinista. También se muestran algunos errores comunes que conviene evitar.</span><span class="sxs-lookup"><span data-stu-id="d1460-p125">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error. This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic. It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="d1460-p126">Los esquemas XSD existen con el fin de validar la estructura de datos XML y la semántica de tipos. Para llevar a cabo esta tarea, el sistema de validación (en este caso, MSXML 5.0) debe asignar los nodos XML a las declaraciones XSD. Sin esta asignación, el sistema de validación no puede llevar a cabo su tarea. Si se puede garantizar la asignación, entonces el esquema es determinista. Si hay una única instancia XML que imposibilita esta asignación, entonces el esquema es no determinista.</span><span class="sxs-lookup"><span data-stu-id="d1460-p126">XSD schemas exist for the purpose of validating XML data structure and type semantics. To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations. Without this mapping, the validating system cannot accomplish its task. If a mapping can be guaranteed, then the schema is deterministic. If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="d1460-209">En el ejemplo siguiente el esquema es no determinista:</span><span class="sxs-lookup"><span data-stu-id="d1460-209">The following example schema is nondeterministic:</span></span>
  
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

<span data-ttu-id="d1460-210">Para explicar por qué este segmento de XSD es no determinista, supongamos que tiene el siguiente fragmento de XML que desea validar con este esquema:</span><span class="sxs-lookup"><span data-stu-id="d1460-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="d1460-p127">En este fragmento de XML, no está claro si el elemento  *\<file_path\>*  es el nodo obligatorio de esta primera parte de la declaración de opción o el opcional de la segunda parte de la declaración de opción. Esta distinción es importante por las razones siguientes:</span><span class="sxs-lookup"><span data-stu-id="d1460-p127">In this XML fragment, it is not clear whether the  *\<file_path\>*  element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration. This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="d1460-213">Si el fragmento de XML se valida frente a la primera parte de la declaración de opción, entonces el XML es valido para el esquema.</span><span class="sxs-lookup"><span data-stu-id="d1460-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="d1460-214">Si el fragmento de XML se valida frente a la segunda parte de la declaración de opción, entonces el esquema no es valido porque falta el nodo \<URI\> obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d1460-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="d1460-p128">Algunos sistemas de validación de XSD caen en el error de validar frente a este esquema porque existe una ruta de acceso válida. MSXML es más estricto y devuelve un error en el que indica que el esquema es no determinista.</span><span class="sxs-lookup"><span data-stu-id="d1460-p128">Some XSD validation systems err toward validating against this schema because there is a valid path. MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="d1460-p129">A continuación, se ofrecen unos cuantos ejemplos más de esquemas no deterministas. El primero se ocupa de elementos opcionales. Estos casos proceden a menudo de convertidores XDR a XSD por las diferencias en la cardinalidad predeterminada de los dos lenguajes de esquema. El primer caso que hay que tener en cuenta son los elementos opcionales declarados con los elementos **xsd:choice** y **xsd:sequence**. Los elementos opcionales declarados en un elemento **xsd:sequence** se validan, por lo general, de forma correcta, siempre que no haya otros elementos con el mismo nombre repetidos solo con elementos opcionales en ellos. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d1460-p129">What follows are a few more examples of nondeterministic schemas. The first deals with optional elements. These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages. The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements. Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between. For example:</span></span> 
  
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

<span data-ttu-id="d1460-223">Para comprender por qué este segmento del esquema es no determinista, suponga que tiene el siguiente fragmento de XML no válido:</span><span class="sxs-lookup"><span data-stu-id="d1460-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="d1460-224">Si se observa el fragmento, se puede ver por qué no es válido: hay dos elementos  `<aNode>` antes del elemento  `<anotherNode>`, cuando solo puede haber uno.</span><span class="sxs-lookup"><span data-stu-id="d1460-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="d1460-225">Ahora suponga que tiene la siguiente instancia XML que validar:</span><span class="sxs-lookup"><span data-stu-id="d1460-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="d1460-p130">El reto está en determinar si esta instancia es válida. ¿Tiene dos elementos  `<aNode>` donde solo se permite uno, o tiene un elemento  `<aNode>` y otro elemento donde se permiten? El esquema es no determinista porque no hay forma de saberlo.</span><span class="sxs-lookup"><span data-stu-id="d1460-p130">The challenge is to determine whether this instance is valid. Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed? The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="d1460-p131">De igual modo, los elementos opcionales declarados en un elemento **xsd:choice** son, generalmente, problemáticos. En el siguiente ejemplo simplificado, no hay manera de saber si la opción se produjo una vez sin que estuviera presente el elemento opcional o si nunca se produjo.</span><span class="sxs-lookup"><span data-stu-id="d1460-p131">Similarly, optional elements declared in an **xsd:choice** element are usually problematic. In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="d1460-p132">La última práctica cuestionable es el uso de un elemento **xsd:any** sin una definición de espacio de nombres, como en  `<xsd:any namespace="##other"/>`, después de un elemento **xsd:sequence**. Esta construcción es especialmente problemática cuando va después de un elemento opcional. Si volvemos al ejemplo anterior y cambiamos solo el último nodo por un elemento **xsd:any**, podemos ver que todos los argumentos previos sobre no determinismo siguen estando vigentes, del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="d1460-p132">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element. This construct is especially troublesome when it follows an optional element. If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
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

## <a name="illegal-enumeration-values"></a><span data-ttu-id="d1460-234">Valores de enumeración no válidos</span><span class="sxs-lookup"><span data-stu-id="d1460-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="d1460-p133">Los esquemas XSD por lo general no efectúan ninguna validación de tipos hasta que se valida un documento de instancia real. La excepción ocurre cuando hay una enumeración en el esquema. En este caso, el esquema valida los valores de enumeración frente a los tipos de enumeración para asegurar que son valores de nodo correctos. A continuación, se indican dos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="d1460-p133">XSD schemas typically do not perform any type validation until you validate an actual instance document. An exception to this is when you have an enumeration in your schema. In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values. Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="d1460-239">Este esquema no es válido porque "eleven o'clock" no es un valor válido para un elemento del tipo **xsd:time**.</span><span class="sxs-lookup"><span data-stu-id="d1460-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="d1460-240">El siguiente es un ejemplo más complejo:</span><span class="sxs-lookup"><span data-stu-id="d1460-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="d1460-p134">Para entender por qué este ejemplo no es válido, debe comprender cómo se define el tipo **xsd:NMTOKEN**. La especificación de tipos de datos W3C define el tipo **NMTOKEN** como sigue: "Un NMTOKEN (token de nombre) es una combinación de los caracteres del nombre".</span><span class="sxs-lookup"><span data-stu-id="d1460-p134">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined. The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="d1460-243">Si investiga más a fondo, encontrará ' &' no es un carácter de nombre válido y, por lo tanto, "M & Ms" no valida como un tipo **NMTOKEN** .</span><span class="sxs-lookup"><span data-stu-id="d1460-243">If you investigate further, you find that '&' is not a valid name character, and therefore "M&Ms" does not validate as an **NMTOKEN** type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="d1460-244">Elementos de opción o secuencia vacíos</span><span class="sxs-lookup"><span data-stu-id="d1460-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="d1460-245">A veces, MSXML devuelve errores sobre las declaraciones de esquema que contienen elementos **xsd:choice** o **xsd:sequence** vacíos, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d1460-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="d1460-246">Al quitar la etiqueta  `<xsd:choice />` vacía, se debería solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="d1460-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="d1460-247">Expresiones regulares</span><span class="sxs-lookup"><span data-stu-id="d1460-247">Regular Expressions</span></span>

<span data-ttu-id="d1460-p135">MSXML 5.0 puede tener problemas cuando valida modelos de expresiones regulares durante la carga. Las expresiones regulares pueden ser complicadas y hay que tener precaución al usarlas. Cada analizador XSD parece tener lenguajes de expresiones regulares flexibles; es decir, implementan el lenguaje de expresiones regulares XSD oficial junto con los elementos de otros lenguajes de expresiones regulares. Si el diseñador de formularios de InfoPath tiene problemas al analizar una expresión regular, los datos de muestra que genera pueden no ser válidos o no llegar a generarse en absoluto. Esto es aceptable en tiempo de diseño, porque InfoPath solo usa datos de muestra para fines de formato. Ahora bien, si se usa una expresión regular que MSXML no admite, InfoPath no puede usarla para validar un valor cuando el usuario está rellenando un formulario. En [Esquema XML Parte 0: Primera, segunda edición](http://www.w3.org/TR/xmlschema-0/) se describe lo que se admite en las expresiones regulares XSD. Para obtener más información sobre las expresiones regulares XSD y las expresiones regulares de nivel 1 de Unicode, vea las [Expresiones habituales de Unicode](http://www.unicode.org/reports/tr18/).</span><span class="sxs-lookup"><span data-stu-id="d1460-p135">MSXML 5.0 can have problems validating regular expression patterns on load. Regular expressions can be complicated, and you should be careful when you are using them. Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages. If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all. This is acceptable at design time, because InfoPath uses only sample data for formatting. However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form. [XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions. For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](http://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="d1460-256">Problemas con el atributo targetNamespace</span><span class="sxs-lookup"><span data-stu-id="d1460-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="d1460-p136">XSD es interesante en el sentido de que, de manera predeterminada, el atributo **targetNamespace** se refiere únicamente a las declaraciones de nivel superior, aunque se puede establecer  `attributeFormDefault=qualified` y  `elementFormDefault=qualified` para invalidar este comportamiento predeterminado. Como ejemplo, suponga que tiene el siguiente XSD.</span><span class="sxs-lookup"><span data-stu-id="d1460-p136">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior. As an example, assume that you have the following XSD.</span></span> 
  
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

<span data-ttu-id="d1460-259">Y que el documento de instancia XML se parece a este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d1460-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="d1460-p137">Las definiciones locales no requieren el espacio de nombres de destino porque la cualificación de nombre completo está deshabilitada de manera predeterminada. Sin embargo, si cambia la definición local para que sea global, entonces la referencia debe completarse con el prefijo del espacio de nombres. Por ejemplo, el esquema siguiente no es válido.</span><span class="sxs-lookup"><span data-stu-id="d1460-p137">Local definitions do not require the target namespace because qualification is turned off by default. However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix. For example, the following schema is invalid.</span></span>
  
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

<span data-ttu-id="d1460-p138">Este esquema no es válido porque "global" está en el espacio de nombres "http://ns". La simple ref="global" no se reconoce porque el espacio de nombres predeterminado no es "http://ns". Para solucionarlo, debe agregar un prefijo al espacio de nombres de destino y usarlo en todos las referencias globales y usos de tipos. El esquema correcto se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d1460-p138">This schema is invalid because "global" is in the namespace "http://ns". The simple ref="global" is not recognized because the default namespace is not "http://ns". To fix this, you must add a prefix for the target namespace and use that for all global references and type uses. The corrected schema looks like the following.</span></span>
  
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

<span data-ttu-id="d1460-267">Si su esquema tiene especificado el atributo **targetNamespace**, asegúrese de que todas las referencias globales están completas con el prefijo del espacio de nombres correcto.</span><span class="sxs-lookup"><span data-stu-id="d1460-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="d1460-268">Codificación de instrucciones de procesamiento XML (Unicode o ANSII)</span><span class="sxs-lookup"><span data-stu-id="d1460-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="d1460-p139">XML admite conjuntos de caracteres Unicode. Por consiguiente, puede perder información si guarda archivos que usan caracteres ANSII. Sin embargo, guardar los archivos como UTF-16 puede resultar excesivo según el uso que se vaya a dar. Para reducir el costo de implementación de un lector XML, el autor del XML debe enunciar la codificación que se usa en la instrucción de procesamiento XML de nivel superior. Tal vez reconozca la siguiente instrucción de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="d1460-p139">XML supports only Unicode character sets. Therefore, you may lose information if you save files that use ANSII characters. However, saving files as UTF-16 may be excessive for your particular use. To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction. You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="d1460-p140">Esta etiqueta de instrucción de procesamiento especifica que la codificación del archivo es UTF-8. Debe asegurarse de que la codificación del archivo es la misma que la que se enuncia en la etiqueta de la instrucción de procesamiento. Puede determinar cuál es la codificación observando los bytes del archivo y buscando las marcas de orden de bytes Unicode. No obstante, hay una forma más sencilla. Si tiene problemas para abrir un esquema XSD, especifique la codificación "UTF-8", ábralo en un editor de texto como Bloc de notas y después guarde el archivo usando la codificación UTF-8 (Bloc de notas ofrece la lista desplegable **Codificación** en el cuadro de diálogo **Guardar como**). Si continúa teniendo problemas para abrir el archivo, no se trata de un problema de codificación.</span><span class="sxs-lookup"><span data-stu-id="d1460-p140">This processing instruction tag specifies that the encoding of the file is UTF-8. You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag. You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks. But there is an easier way. If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box). If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="d1460-280">Atributo maxOccurs dentro del elemento xsd:all</span><span class="sxs-lookup"><span data-stu-id="d1460-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="d1460-p141">Debido al modo en que se define el no determinismo en la recomendación del esquema XML, el único valor válido para el atributo **maxOccurs** de un elemento **xsd:element** dentro de un elemento **xsd:all** es 1. Por ejemplo, lo siguiente es válido.</span><span class="sxs-lookup"><span data-stu-id="d1460-p141">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1. For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="d1460-283">Sin embargo, este ejemplo no es válido.</span><span class="sxs-lookup"><span data-stu-id="d1460-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="d1460-p142">Este ejemplo no es válido porque el sistema de validación no puede determinar si se asignan dos apariciones de  `<x/>` a la declaración única o a la declaración y a otra definición no válida. Del mismo modo, no se pueden tener dos elementos con el mismo nombre en una etiqueta  `<xsd:all>`.</span><span class="sxs-lookup"><span data-stu-id="d1460-p142">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition. Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="d1460-p143">Este ejemplo también es interesante porque permite tener cualquier número de nodos  `<x/>` y  `<docs/>` dentro de un elemento contenedor en cualquier orden. Aunque esta construcción no es válida, existe una solución: con el elemento **xsd:choice** puede conseguir el mismo resultado, como se demuestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d1460-p143">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order. Although this construct is invalid, there is a workaround. By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="d1460-289">Cómo modificar o crear un XSD para InfoPath</span><span class="sxs-lookup"><span data-stu-id="d1460-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="d1460-290">Los dos ejemplos de las siguientes secciones muestran cómo modificar o crear un esquema para producir resultados concretos en InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d1460-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="d1460-291">Permitir la inserción de elementos definidos por el usuario en el panel de tareas Campos</span><span class="sxs-lookup"><span data-stu-id="d1460-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="d1460-p144">Para permitir que los elementos definidos por el usuario aparezcan bajo un elemento principal en el panel de tareas **Campos**, debe insertar un elemento **xsd:any** bajo el elemento principal. Para permitir insertar elementos definidos por el usuario dentro de  `<your_node_name>` , la declaración XSD debería parecerse a lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d1460-p144">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element. To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
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

<span data-ttu-id="d1460-294">Si también desea permitir atributos definidos por el usuario, debe agregar  `<xsd:anyAttribute namespace="##any | ##other"/>` a la declaración del elemento.</span><span class="sxs-lookup"><span data-stu-id="d1460-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="d1460-295">Permitir enlazar elementos de texto enriquecido en los modos de diseño y de edición de InfoPath</span><span class="sxs-lookup"><span data-stu-id="d1460-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="d1460-296">Si desea declarar un elemento que se pueda enlazar a un control **Rich Text Box**, debe tener el formulario siguiente, que incluye el elemento **xsd:any** que tiene un atributo de espacio de nombres establecido en "http://www.w3.org/1999/xhtml", como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d1460-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "http://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
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

## <a name="conclusion"></a><span data-ttu-id="d1460-297">Conclusión</span><span class="sxs-lookup"><span data-stu-id="d1460-297">Conclusion</span></span>

<span data-ttu-id="d1460-p145">Aprovechando las ventajas que presenta InfoPath para diseñar soluciones de formulario XML que se basan en archivos de esquema XML (.xsd) creados externamente, puede crear una plantilla de formulario que funcione con un esquema estándar de la industria o con un esquema personalizado creado en su compañía u organización. Con la información proporcionada en este artículo, puede crear archivos de esquema XSD personalizados compatibles con InfoPath y solucionar problemas habituales que pueden producirse cuando se cargan archivos XSD creados externamente en el entorno de diseño de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d1460-p145">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization. By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1460-300">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1460-300">See also</span></span>

- [<span data-ttu-id="d1460-301">Esquema XML W3C </span><span class="sxs-lookup"><span data-stu-id="d1460-301">W3C XML Schema</span></span>](http://www.w3.org/XML/Schema)
- [<span data-ttu-id="d1460-302">Esquema W3C XML Primer</span><span class="sxs-lookup"><span data-stu-id="d1460-302">W3C XML Schema Primer</span></span>](http://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="d1460-303">Referencia de estructuras de Esquema W3C XML</span><span class="sxs-lookup"><span data-stu-id="d1460-303">W3C XML Schema Structures Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [<span data-ttu-id="d1460-304">Referencia de tipos de datos de esquema W3C XML</span><span class="sxs-lookup"><span data-stu-id="d1460-304">W3C XML Schema Datatypes Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [<span data-ttu-id="d1460-305">Tutorial del esquema XML</span><span class="sxs-lookup"><span data-stu-id="d1460-305">XML Schema Tutorial</span></span>](http://www.w3schools.com/schema/default.asp)
- [<span data-ttu-id="d1460-306">Centro de programadores de XML</span><span class="sxs-lookup"><span data-stu-id="d1460-306">XML Developer Center</span></span>](http://msdn.microsoft.com/en-us/xml/default.aspx)

