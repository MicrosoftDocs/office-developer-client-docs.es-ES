---
title: Introducción al formato de archivo de Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar con el formato de archivo Visio 2013 mediante programación y cree una aplicación de consola sencilla que examina un archivo Visio 2013.
localization_priority: Priority
ms.openlocfilehash: 74c0f05a1db280386f3dc9dfd23da73a9b2daaf5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357277"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="dc68f-103">Introducción al formato de archivo de Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="dc68f-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="dc68f-104">Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar con el formato de archivo Visio 2013 mediante programación y cree una aplicación de consola sencilla que examina un archivo Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="dc68f-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc68f-105">**En este artículo**         [Introducción](#vis15_IntroVSDX_Intro)          [¿Qué hay detrás del formato de archivo de Visio 2013?](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="dc68f-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="dc68f-106">[Escenarios para desarrolladores para trabajar con el formato de archivo de Visio 2013](#vis15_IntroVSDX_Scenarios)[Explorar el formato de archivo de Visio 2013 mediante programación](#vis15_IntroVSDX_Explore)[Recursos adicionales](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="dc68f-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="dc68f-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="dc68f-107">Introduction</span></span>
<span data-ttu-id="dc68f-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="dc68f-108"></span></span>

<span data-ttu-id="dc68f-109">Visio 2013 presenta un nuevo formato de archivo (.vsdx) de Visio que reemplaza el formato de archivo binario de Visio (.vsd) y el formato de archivo de dibujo de Visio XML (.vdx).</span><span class="sxs-lookup"><span data-stu-id="dc68f-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="dc68f-110">Dado que el formato de archivo de Visio 2013 se basa en convenciones de empaquetado abierto y XML, los desarrolladores familiarizados con estas tecnologías pueden aprender rápidamente a trabajar con archivos de Visio 2013 mediante programación.</span><span class="sxs-lookup"><span data-stu-id="dc68f-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="dc68f-111">Los desarrolladores familiarizados con el formato de archivo de dibujo de Visio XML (.vdx) de versiones anteriores de Visio encontrarán muchas de las mismas estructuras de XML en los elementos del formato de archivo .vsdx.</span><span class="sxs-lookup"><span data-stu-id="dc68f-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="dc68f-112">La interoperabilidad con archivos de Visio aumenta enormemente gracias a que el software de terceros puede manipular archivos de Visio a nivel de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="dc68f-113">El formato de archivo de Visio 2013 es compatible con los servicios de Visio en Microsoft SharePoint Server 2013, sin necesidad de un formato de archivo "intermediario" para publicar en SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="dc68f-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="dc68f-114">Existen varios tipos de archivo, por extensión, que componen el formato de archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="dc68f-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="dc68f-115">Estas extensiones incluyen:</span><span class="sxs-lookup"><span data-stu-id="dc68f-115">These extensions include:</span></span>
  
- <span data-ttu-id="dc68f-116">.vsdx (dibujo de Visio)</span><span class="sxs-lookup"><span data-stu-id="dc68f-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="dc68f-117">.vsdm (dibujo habilitado para macros de Visio)</span><span class="sxs-lookup"><span data-stu-id="dc68f-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="dc68f-118">.vssx (galería de símbolos de Visio)</span><span class="sxs-lookup"><span data-stu-id="dc68f-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="dc68f-119">.vssm (galería de símbolos habilitada para macros de Visio)</span><span class="sxs-lookup"><span data-stu-id="dc68f-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="dc68f-120">.vstx (plantilla de Visio)</span><span class="sxs-lookup"><span data-stu-id="dc68f-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="dc68f-121">.vstm (plantilla habilitada para macros de Visio)</span><span class="sxs-lookup"><span data-stu-id="dc68f-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="dc68f-p104">Solo los archivos habilitados con macros (.vsdm, .vssm, .vstm) pueden almacenar macros de VBA. No es posible almacenar macros en archivos con la extensión .vsdx, .vssx ni .vstx.</span><span class="sxs-lookup"><span data-stu-id="dc68f-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="dc68f-124">¿Qué hay detrás del formato de archivo de Visio 2013?</span><span class="sxs-lookup"><span data-stu-id="dc68f-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="dc68f-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="dc68f-125"></span></span>

<span data-ttu-id="dc68f-126">El formato de archivo de Visio 2013 usa convenciones de empaquetado abierto (OPC), que definen una manera estructurada de almacenar los datos de la aplicación junto con los recursos relacionados mediante un contenedor de algún tipo; por ejemplo, un archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="dc68f-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="dc68f-127">En un nivel básico, un archivo de Visio 2013 es, en realidad, un contenedor ZIP que contiene otros tipos de archivos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="dc68f-128">De hecho, puede guardar un dibujo de Visio 2013 como un archivo .vsdx, cambiar la extensión del archivo a "\*.zip" en el Explorador de Windows y, a continuación, abrir el archivo como una carpeta para ver el contenido.</span><span class="sxs-lookup"><span data-stu-id="dc68f-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="dc68f-129">Este artículo contiene una breve introducción a las convenciones de empaquetado abierto.</span><span class="sxs-lookup"><span data-stu-id="dc68f-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="dc68f-130">Para obtener información más detallada sobre estas convenciones en otros artículos: >  Para más información sobre las convenciones de empaquetado abierto en sí, consulte [OPC: Nuevo estándar para empaquetar sus datos](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc68f-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="dc68f-131">>  Para obtener más información sobre las convenciones de empaquetado abierto y su uso en los archivos de Microsoft Office, consulte [Aspectos fundamentales de las convenciones de empaquetado abierto](https://msdn.microsoft.com/library/ee361919.aspx) e  [Introducción a los formato de archivo Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc68f-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="dc68f-132">Paquetes y elementos de paquete</span><span class="sxs-lookup"><span data-stu-id="dc68f-132">Packages and Package Parts</span></span>

<span data-ttu-id="dc68f-133">Como se mencionó anteriormente, los archivos de Visio 2013 son contenedores ZIP o "paquetes" que contienen otros archivos (denominados "elementos de paquete") dentro de ellos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="dc68f-134">Un elemento del paquete puede ser un archivo XML, una imagen e, incluso, una solución de VBA.</span><span class="sxs-lookup"><span data-stu-id="dc68f-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="dc68f-135">Los elementos de paquete se dividen en dos categorías más generales: "elementos de documento" y "elementos de relación".</span><span class="sxs-lookup"><span data-stu-id="dc68f-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="dc68f-136">En los elementos de documento se encuentran el contenido y los metadatos del archivo de Visio; por ejemplo, el nombre del archivo, la primera página y todas las formas que contiene e, incluso, las conexiones de datos para las formas.</span><span class="sxs-lookup"><span data-stu-id="dc68f-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="dc68f-137">Las imágenes y los archivos de texto dentro del paquete se consideran elementos de documento.</span><span class="sxs-lookup"><span data-stu-id="dc68f-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="dc68f-138">Los elementos de relación se describen con mayor detalle más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dc68f-139">Si abre un archivo de Visio 2013 con una herramienta de compresión, probablemente verá varias carpetas dentro del paquete ZIP.</span><span class="sxs-lookup"><span data-stu-id="dc68f-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="dc68f-140">Puede, incluso, manipular estas subdirecciones como carpetas con una herramienta de compresión.</span><span class="sxs-lookup"><span data-stu-id="dc68f-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="dc68f-141">No obstante, estas "carpetas" representan subdirecciones dentro del paquete ZIP, no carpetas reales.</span><span class="sxs-lookup"><span data-stu-id="dc68f-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="dc68f-142">No puede usar los equivalentes de carpetas mediante programación para trabajar con estas subdirecciones en su solución.</span><span class="sxs-lookup"><span data-stu-id="dc68f-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="dc68f-p109">Los elementos de paquete, tanto los de documento como los de relación, también tienen tipos de contenido asociado. Estos tipos de contenido son cadenas que definen un tipo de medio MIME. Estos tipos de contenido especifican y establecen el alcance de la clase de tipos MIME que se pueden obtener en el archivo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="dc68f-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dc68f-146">Relationships</span></span>

<span data-ttu-id="dc68f-147">Los elementos de relación (que terminan con la extensión "\*.rels" y se almacenan en una carpeta "_rels") describen cómo se relacionan entre sí los elementos dentro del paquete y proporcionan la estructura del archivo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="dc68f-148">Un documento XML independiente usa la relación de elemento primario/secundario de los elementos para determinar la relación de las entidades entre sí.</span><span class="sxs-lookup"><span data-stu-id="dc68f-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="dc68f-149">Otros archivos pueden usar otras jerarquías o la estructura de carpetas de archivo para describir la interacción del contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="dc68f-150">Para el formato de archivo de Visio 2013, el paquete es un archivo de Visio válido si contiene el conjunto adecuado de elementos y el paquete contiene las relaciones entre los elementos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="dc68f-p111">Los elementos de relación son documentos XML que describen las relaciones entre los distintos elementos de documento de un paquete. Definen la asociación entre dos elementos: un origen especificado (definido por el nombre y la ubicación del archivo de relación) y un elemento de documento de destino especificado. Por ejemplo, los elementos de relación se usan para describir los maestros de forma que están asociados con el archivo, el modo en que las páginas se relacionan con el archivo y entre sí o el modo en que las imágenes y los objetos se relacionan con una página concreta.</span><span class="sxs-lookup"><span data-stu-id="dc68f-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="dc68f-154">Similitudes y diferencias con el esquema VDX de Visio</span><span class="sxs-lookup"><span data-stu-id="dc68f-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="dc68f-155">Como ya se ha mencionado, las versiones anteriores de Visio incluían también un formato de archivo basado en XML, el formato de dibujo de Visio XML o .vdx.</span><span class="sxs-lookup"><span data-stu-id="dc68f-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="dc68f-156">(En versiones anteriores de Visio, el esquema que se usa para el formato de dibujo de Visio XML se denomina DatadiagramML). Algunas partes del esquema de Visio XML han permanecido igual entre los dos formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="dc68f-157">Por ejemplo, el elemento **Windows** y sus elementos secundarios no sufren modificaciones, con la excepción que el elemento **Windows** pasa a ser un elemento de raíz de un documento XML (window.xml).</span><span class="sxs-lookup"><span data-stu-id="dc68f-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="dc68f-158">La diferencia más notable entre el formato de dibujo XML y el formato de archivo de Visio 2013 es el empaquetado.</span><span class="sxs-lookup"><span data-stu-id="dc68f-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="dc68f-159">Un archivo de formato de dibujo XML podría tratarse como un XML normal independiente; el formato de archivo de Visio 2013 debe tratarse como un paquete.</span><span class="sxs-lookup"><span data-stu-id="dc68f-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="dc68f-160">En Visio 2013, se ha dividido el XML en secciones para facilitar su consumo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="dc68f-161">Otro cambio notable es que el formato de archivo de Visio 2013 almacena todas las propiedades del documento en elementos del documento que se describe en la norma OPC (app.xml, core.xml personalizado.XML).</span><span class="sxs-lookup"><span data-stu-id="dc68f-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="dc68f-162">No obstante, hay un cambio importante que todos los desarrolladores de Visio deben tener en cuenta: la introducción de los elementos **Cell** (celda), **Row** (fila) y **Section** (sección).</span><span class="sxs-lookup"><span data-stu-id="dc68f-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="dc68f-163">En el esquema de formato de archivo de dibujo XML, las filas y celdas individuales de ShapeSheet se representan mediante elementos con nombre.</span><span class="sxs-lookup"><span data-stu-id="dc68f-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="dc68f-164">Por ejemplo, imagine que tiene un documento de una sola página que contiene una forma con un valor **PinX** de "2" (lo que significa que el eje de giro de la forma es de 2 pulgadas (5 cm) desde el borde izquierdo del dibujo).</span><span class="sxs-lookup"><span data-stu-id="dc68f-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="dc68f-165">En el siguiente código se muestra el marcado relevante para la configuración del formato de archivo de dibujo XML.</span><span class="sxs-lookup"><span data-stu-id="dc68f-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="dc68f-166">Aquí, el elemento **PinX** es un elemento secundario del elemento **XForm**, que es, a su vez, un elemento secundario del elemento **Shape** (forma).</span><span class="sxs-lookup"><span data-stu-id="dc68f-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="dc68f-167">Este da forma a la interfaz de usuario de Visio ShapeSheet, donde la celda **PinX** se incluye en la sección **Transformación de forma** de una forma.</span><span class="sxs-lookup"><span data-stu-id="dc68f-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="dc68f-168">En el formato de archivo de Visio 2013, todas las celdas de ShapeSheet - **PinX**, **LinePattern**, una celda **X** en una fila **MoveTo** en una sección **Geometría**, etc. - están representadas por un tipo de elemento XML: el elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="dc68f-169">Los diferentes elementos **Cell** se distinguen entre sí por el valor de su atributo **N**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="dc68f-170">Por lo tanto, en el ejemplo anterior, los datos contenidos en la celda **PinX** en ShapeSheet se almacenan en un archivo VSDX, como se muestra en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="dc68f-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="dc68f-171">El elemento **Cell** para **PinX** (así como otras celdas individuales con nombre, denominadas "celdas singleton", como **LinePattern** o **LockSelect**) es un elemento secundario directo del elemento **Shape**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="dc68f-172">No es necesario ningún elemento único para representar la fila que contiene la celda **PinX**, ya que cada forma solo puede tener una **PinX**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="dc68f-173">¿Qué sucede con las secciones que incluyen datos tabulares, como las secciones**Geometría**?</span><span class="sxs-lookup"><span data-stu-id="dc68f-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="dc68f-174">Para las celdas de esas secciones, el esquema de formato de archivo de Visio 2013 usa elementos **Section** y **Row**, también diferenciados por su atributo **N** o \*\*T \*\* tal como se muestra debajo, para contener los datos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="dc68f-175">Por ejemplo, la misma forma del ejemplo anterior puede contener datos en la sección **Geometría 1** que son similares al siguiente código en el esquema de dibujo XML.</span><span class="sxs-lookup"><span data-stu-id="dc68f-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Geom IX="0">
        <!--- Other cells and rows in the Geometry 1 section -->
        <LineTo IX="1">
            <X F="Width*0">0</X>
            <Y F="Height*0">0</Y>
        </LineTo>
    </Geom>
</Shape>

```

<span data-ttu-id="dc68f-176">Sin embargo, se parece al siguiente código del archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="dc68f-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Section N="Geometry" IX="0"> 
        <!--- Other cells and rows in the Geometry 1 section -->
        <Row IX="1" T="LineTo">
            <Cell V="0" N="X" V="Width*0" />
            <Cell V="0" N="Y" V="Height*0" />
        </Row>
    </Section>
</Shape>

```

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="dc68f-177">Escenarios para desarrolladores para trabajar con el formato de archivo de Visio 2013</span><span class="sxs-lookup"><span data-stu-id="dc68f-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="dc68f-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="dc68f-178"></span></span>

<span data-ttu-id="dc68f-179">Como se ha explicado anteriormente, el formato de archivo de Visio 2013 aprovecha varias tecnologías bien comprendidas, como archivos ZIP y XML, para almacenar datos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="dc68f-180">Para manipular un dibujo de Visio 2013 al nivel de archivo, una solución solo necesita usar las clases y los espacios de nombres de .NET Framework que se asocian al trabajo con archivos ZIP o XML, como [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) o [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc68f-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="dc68f-181">La mayor ventaja para los desarrolladores de los formatos de archivo de Visio 2013 es que se puede leer y escribir en archivos de Visio 2013 sin automatizar la aplicación de cliente de Visio.</span><span class="sxs-lookup"><span data-stu-id="dc68f-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="dc68f-182">Estos son algunos de los escenarios que puede considerar como desarrollador para trabajar con el formato de archivo de Visio 2013:</span><span class="sxs-lookup"><span data-stu-id="dc68f-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="dc68f-183">Comprobación de archivos individuales de Visio 2013 en busca de datos específicos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="dc68f-184">Puede leer un elemento del contenedor ZIP de manera selectiva sin tener que extraer todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="dc68f-185">Actualización de las bibliotecas de los archivos de Visio 2013 con contenido específico.</span><span class="sxs-lookup"><span data-stu-id="dc68f-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="dc68f-186">Puede cambiar el logotipo en todas las páginas de fondo mediante programación para reflejar nuevas pautas de marca.</span><span class="sxs-lookup"><span data-stu-id="dc68f-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="dc68f-187">Creación de aplicaciones que utilizan los archivos de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="dc68f-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="dc68f-188">Por ejemplo, puede crear una herramienta que lea un diagrama de flujo de trabajo de Visio y luego ejecute su propia lógica empresarial basándose en ese flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="dc68f-189">Tenga en cuenta que dado que estas soluciones usan ensamblados .NET Framework estándar, la mayoría de las soluciones que se pueden ejecutar en un equipo cliente también se pueden ejecutar en un servidor.</span><span class="sxs-lookup"><span data-stu-id="dc68f-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="dc68f-190">Manipulación del formato de archivo de Visio 2013 mediante programación</span><span class="sxs-lookup"><span data-stu-id="dc68f-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="dc68f-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="dc68f-191"></span></span>

<span data-ttu-id="dc68f-192">La tarea más básica y fundamental para los programadores que trabajan con el formato de archivo de Visio 2013 es abrir el archivo como un paquete y, a continuación, acceder a los elementos individuales dentro del paquete.</span><span class="sxs-lookup"><span data-stu-id="dc68f-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="dc68f-193">El **System.IO.Packaging.Package** en la WindowsBase.dll contiene muchas clases que le permiten abrir y manipular paquetes y elementos.</span><span class="sxs-lookup"><span data-stu-id="dc68f-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="dc68f-194">En el código de ejemplo siguiente, se puede ver cómo abrir un archivo .vsdx, leer la lista de elementos de paquete y obtener información sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="dc68f-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="dc68f-195">Para abrir un archivo .vsdx y ver los elementos de documento</span><span class="sxs-lookup"><span data-stu-id="dc68f-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="dc68f-196">Abra Visio 2013 y cree un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="dc68f-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="dc68f-197">Cree un nuevo documento y guárdelo en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="dc68f-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="dc68f-198">Abra Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="dc68f-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="dc68f-199">En el menú **Archivo**, elija **Nuevo** y, luego, \*\* Proyecto \*\*.</span><span class="sxs-lookup"><span data-stu-id="dc68f-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="dc68f-200">En \*\*Visual C# \*\* o **Visual Basic**, expanda **Windows**y seleccione **Aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="dc68f-201">En el cuadro **Nombre**, escriba 'VisioFileExplorer'.</span><span class="sxs-lookup"><span data-stu-id="dc68f-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="dc68f-202">Se abre la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="dc68f-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="dc68f-203">En el **Explorador de soluciones**, haga clic con el botón derecho en **VisioFileExplorer**y, a continuación, en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="dc68f-204">En el cuadro de diálogo **Agregar referencia**, en **Ensamblados**, expanda **Framework**y luego elija **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="dc68f-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="dc68f-205">Pegue el código siguiente en la solución.</span><span class="sxs-lookup"><span data-stu-id="dc68f-205">Paste the following code into the solution.</span></span>
    
  ```cs
  using System;
  using System.Collections.Generic;
  using System.Linq;
  using System.Text;
  using System.IO;
  using System.IO.Packaging;
  using System.Diagnostics;
  namespace VisioFileExplorer
  {
      class Program
      {
          static void Main(string[] args)
          {    
              try
              {
                  Console.WriteLine("Opening the VSDX file ...");
                  // Need to get the folder path for the Desktop
                  // where the file is saved.
                  string dirPath = System.Environment.GetFolderPath(
                      System.Environment.SpecialFolder.Desktop);
                  DirectoryInfo myDir = new DirectoryInfo(dirPath);
                  // It is a best practice to get the file name string
                  // using a FileInfo object, but it isn't necessary.
                  FileInfo[] fInfos = myDir.GetFiles("*.vsdx");
                  FileInfo fi = fInfos[0];
                  string fName = fi.FullName;
                  // We're not going to do any more than open
                  // and read the list of parts in the package, although
                  // we can create a package or read/write what's inside.
                  using (Package fPackage = Package.Open(
                      fName, FileMode.Open, FileAccess.Read))
                  {
                      
                      // The way to get a reference to a package part is
                      // by using its URI. Thus, we're reading the URI
                      // for each part in the package.
                      PackagePartCollection fParts = fPackage.GetParts();
                      foreach (PackagePart fPart in fParts)
                      {
                          Console.WriteLine("Package part: {0}", fPart.Uri);
                      }
                  }   
              }
              catch (Exception err)
              {
                  Console.WriteLine("Error: {0}", err.Message);
              }
              finally
              {
                  Console.Write("\nPress any key to continue ...");
                  Console.ReadKey();
              }   
          }
      }
  }
  ```

  ```vb
  Imports System
  Imports System.Collections.Generic
  Imports System.Linq
  Imports System.Text
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Diagnostics
  Module Module1
      Sub Main()
          Try
              Console.WriteLine("Opening the VSDX file ...")
              ' Need to get the folder path for the Desktop
              ' or where the file is saved.
              Dim dirPath As String = System.Environment.GetFolderPath( _
                  System.Environment.SpecialFolder.Desktop)
              Dim myDir As New DirectoryInfo(dirPath)
              ' It is a best practice to get the file name string
              ' using a FileInfo object, but it isn't necessary.
              Dim fInfos As FileInfo() = myDir.GetFiles("*.vsdx")
              Dim fi As FileInfo = fInfos(0)
              Dim fName As String = fi.FullName
              ' We don't need to do any more than open
              ' and read the list of parts in the package, although
              ' we can create a package or read/write what's inside.
              Using fPackage As Package = Package.Open( _
                  fName, FileMode.Open, FileAccess.Read)
                  ' The way to get a reference to a document part is
                  ' by using its URI. Thus, we're reading the URI
                  ' for each document part in the package.
                  Dim fParts As PackagePartCollection = fPackage.GetParts()
                  For Each fPart As PackagePart In fParts
                      Console.WriteLine("Package part: {0}", fPart.Uri)
                  Next
              End Using
          Catch err As Exception
              Console.WriteLine("Error: {0}", err.Message)
          Finally
              Console.Write(vbLf &amp; "Press any key to continue ...")
              Console.ReadKey()
          End Try
      End Sub
  End Module
  
  ```

10. <span data-ttu-id="dc68f-p126">Presione F5 para depurar la solución. Cuando el programa haya completado su ejecución, presione cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="dc68f-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc68f-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc68f-208">See also</span></span>
<span data-ttu-id="dc68f-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="dc68f-209"></span></span>

<span data-ttu-id="dc68f-210">Para obtener más información sobre el formato de archivo de Visio 2013, las convenciones de empaquetado abierto o cómo trabajar con archivos de Visio 2013 u Office OpenXML mediante programación, consulte los recursos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc68f-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="dc68f-211">Visio para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="dc68f-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="dc68f-212">[OPC: Nuevo estándar para empaquetar sus datos](https://msdn.microsoft.com/magazine/cc163372.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc68f-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="dc68f-213">Aspectos fundamentales de las convenciones de empaquetado abierto</span><span class="sxs-lookup"><span data-stu-id="dc68f-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="dc68f-214">Introducción a los formato de archivo Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="dc68f-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

