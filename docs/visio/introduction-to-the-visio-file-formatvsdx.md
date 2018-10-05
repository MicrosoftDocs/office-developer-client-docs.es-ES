---
title: Introducción al formato de archivo de Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar mediante programación con el formato de archivo de Visio 2013 y crear una aplicación de consola sencilla que examina un archivo de Visio 2013.
ms.openlocfilehash: 4efa90ee513def005653f4f8717b0149de1cdc3d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389368"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="5ceb7-103">Introducción al formato de archivo de Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="5ceb7-104">Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar mediante programación con el formato de archivo de Visio 2013 y crear una aplicación de consola sencilla que examina un archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ceb7-105">**En este artículo** [Introducción](#vis15_IntroVSDX_Intro) [¿Qué es el formato de archivo de Visio 2013 "enfoque técnico"?](#vis15_IntroVSDX_What)                   </span><span class="sxs-lookup"><span data-stu-id="5ceb7-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="5ceb7-106">[Escenarios de desarrollador para trabajar con el formato de archivo de Visio 2013](#vis15_IntroVSDX_Scenarios) [Exploración mediante programación el formato de archivo de Visio 2013](#vis15_IntroVSDX_Explore) [Recursos adicionales](#vis15_IntroVSDX_Resources)                    </span><span class="sxs-lookup"><span data-stu-id="5ceb7-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="5ceb7-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="5ceb7-107">Introduction</span></span>
<span data-ttu-id="5ceb7-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="5ceb7-108"></span></span>

<span data-ttu-id="5ceb7-109">Visio 2013 presenta un nuevo formato de archivo (.vsdx) para Visio que reemplaza el formato de archivo binario de Visio (.vsd) y el formato de archivo de dibujo XML de Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="5ceb7-110">Debido a que el formato de archivo de Visio 2013 se basa en convenciones de empaquetado abierto y XML, los programadores que están familiarizados con estas tecnologías pueden aprender rápidamente cómo trabajar con archivos de Visio 2013 mediante programación.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="5ceb7-111">Los programadores que están familiarizados con el formato de archivo de dibujo de Visio XML (.vdx) desde las versiones anteriores de Visio pueden encontrar muchas de las mismas estructuras XML dentro de los elementos de formato de archivo .vsdx.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="5ceb7-112">Interoperabilidad con los archivos de Visio aumenta en gran medida puesto que el software de terceros puede manipular los archivos de Visio en un nivel de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="5ceb7-113">El formato de archivo de Visio 2013 es compatible con los servicios de Visio en Microsoft SharePoint Server 2013, sin necesidad de un formato de archivo "intermediario" para la publicación en SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="5ceb7-114">Hay varios tipos de archivo, por extensión, que conforman el formato de archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="5ceb7-115">Estas extensiones incluyen:</span><span class="sxs-lookup"><span data-stu-id="5ceb7-115">These extensions include:</span></span>
  
- <span data-ttu-id="5ceb7-116">.vsdx (dibujo de Visio)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="5ceb7-117">.vsdm (dibujo de Visio habilitado para macros)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="5ceb7-118">.vssx (galería de símbolos de Visio)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="5ceb7-119">.vssm (galería de símbolos de Visio habilitada para macros)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="5ceb7-120">.vstx (plantilla de Visio)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="5ceb7-121">.vstm (plantilla de Visio habilitada para macros)</span><span class="sxs-lookup"><span data-stu-id="5ceb7-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="5ceb7-p104">Solo los archivos habilitados con macros (.vsdm, .vssm, .vstm) pueden almacenar macros de VBA. No es posible almacenar macros en archivos con la extensión .vsdx, .vssx ni .vstx.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="5ceb7-124">¿Qué es el formato de archivo de Visio 2013 "enfoque técnico"?</span><span class="sxs-lookup"><span data-stu-id="5ceb7-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="5ceb7-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="5ceb7-125"></span></span>

<span data-ttu-id="5ceb7-126">El formato de archivo de Visio 2013 usa Open albarán Conventions (OPC), que define un medio estructurado para almacenar datos de la aplicación con los recursos relacionados con un contenedor de algunos sort─for ejemplo, un archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="5ceb7-127">En un nivel básico, un archivo de Visio 2013 es en realidad un contenedor ZIP que contiene otros tipos de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="5ceb7-128">De hecho, puede guardar un dibujo de Visio 2013 como un archivo .vsdx, cambie el nombre de la extensión de archivo a "\*.zip" en el Explorador de Windows y, a continuación, abra el archivo como una carpeta para ver el contenido dentro de.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="5ceb7-129">Este artículo contiene sólo una breve introducción a las convenciones de empaquetado abierto.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="5ceb7-130">Puede encontrar más detallada de la cobertura de las convenciones de otros artículos: > para obtener más información acerca de las convenciones de empaquetado abierto a sí mismos, vea [OPC: nuevo estándar para empaquetar sus datos](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="5ceb7-131">> Para obtener más información acerca de las convenciones de empaquetado abierto y su uso en archivos de Microsoft Office, vea [aspectos básicos de las convenciones de empaquetado abierto](https://msdn.microsoft.com/library/ee361919.aspx) y [presentación de los formatos de archivo XML abiertos de Office (2007)](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="5ceb7-132">Paquetes y elementos del paquete</span><span class="sxs-lookup"><span data-stu-id="5ceb7-132">Packages and Package Parts</span></span>

<span data-ttu-id="5ceb7-133">Tal y como se ha iniciado anteriormente, los archivos de Visio 2013 son contenedores ZIP o "paquetes" que contienen otros archivos (denominados "las partes del paquete") dentro de ellos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="5ceb7-134">Una parte del paquete puede ser un archivo XML, una imagen, incluso en una solución de VBA.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="5ceb7-135">Los elementos dentro del paquete pueden se dividen en dos categorías amplias, "partes del documento" y "elementos de relación".</span><span class="sxs-lookup"><span data-stu-id="5ceb7-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="5ceb7-136">Los elementos de documento contienen el contenido real y los metadatos del archivo de Visio, al igual que el nombre del archivo, la primera página y todas las formas que contiene, e incluso las conexiones de datos de las formas.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="5ceb7-137">Imágenes y archivos de texto dentro del paquete se consideran partes del documento.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="5ceb7-138">Elementos de relación se describen con más detalle más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5ceb7-139">Si abre un archivo de Visio 2013 mediante una utilidad ZIP, probablemente puede ver varias carpetas que se encuentren dentro del paquete ZIP.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="5ceb7-140">Incluso puede manipular estas direcciones subcaracterística al igual que las carpetas mediante una utilidad ZIP.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="5ceb7-141">Sin embargo, estas "carpetas" representan direcciones subcaracterística dentro del paquete ZIP, las carpetas no reales.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="5ceb7-142">No se puede usar los equivalentes de las carpetas mediante programación para trabajar con estas direcciones subcaracterística en su solución.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="5ceb7-p109">Los elementos de paquete, tanto los de documento como los de relación, también tienen tipos de contenido asociado. Estos tipos de contenido son cadenas que definen un tipo de medio MIME. Estos tipos de contenido especifican y establecen el alcance de la clase de tipos MIME que se pueden obtener en el archivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="5ceb7-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5ceb7-146">Relationships</span></span>

<span data-ttu-id="5ceb7-147">Los elementos de relación (que terminan con la extensión "\*.rels" y se almacenan en una carpeta "_rels") se describe cómo se relacionan entre sí los elementos dentro del paquete y proporcionan la estructura del archivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="5ceb7-148">Un documento XML independiente, utiliza la relación de primarios y secundarios de elementos para determinar la relación de entidades a los otros.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="5ceb7-149">Otros archivos pueden utilizar otras jerarquías o la estructura de carpetas de archivo para describir la interacción de contenido en el archivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="5ceb7-150">Para el formato de archivo de Visio 2013, el paquete es un archivo de Visio válido si contiene el conjunto correcto de elementos y el paquete contiene las relaciones entre los elementos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="5ceb7-p111">Los elementos de relación son documentos XML que describen las relaciones entre los distintos elementos de documento de un paquete. Definen la asociación entre dos elementos: un origen especificado (definido por el nombre y la ubicación del archivo de relación) y un elemento de documento de destino especificado. Por ejemplo, los elementos de relación se usan para describir los maestros de forma que están asociados con el archivo, el modo en que las páginas se relacionan con el archivo y entre sí o el modo en que las imágenes y los objetos se relacionan con una página concreta.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="5ceb7-154">Similitudes y diferencias con el esquema VDX de Visio</span><span class="sxs-lookup"><span data-stu-id="5ceb7-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="5ceb7-155">Como se ha mencionado, las versiones anteriores de Visio también incluyen un archivo basado en XML de formato, el formato de dibujo XML de Visio o .vdx.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="5ceb7-156">(En versiones anteriores de Visio, el esquema usado para el formato de dibujo XML de Visio se denomina DatadiagramML). Algunas partes del esquema XML de Visio hayan permanecido el mismo entre los dos formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="5ceb7-157">Por ejemplo, el elemento de **Windows** y sus elementos secundarios permanecen unchanged─with la excepción de que el elemento de **Windows** ahora es un elemento raíz de un documento XML (window.xml).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="5ceb7-158">La diferencia entre el formato de dibujo XML y el formato de archivo de Visio 2013 más grande es el empaquetado.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="5ceb7-159">Un archivo con formato de dibujo XML se puede manipular como un XML independiente normal; el formato de archivo de Visio 2013 debe tratarse como un paquete.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="5ceb7-160">En Visio 2013, el código XML se ha dividido copia de seguridad en partes para su consumo sea más fácil.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="5ceb7-161">Otro cambio notable es que el formato de archivo de Visio 2013 almacena todas las propiedades de documento en elementos de documento descritos por la norma OPC (app.xml, core.xml, personalizado.XML).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="5ceb7-162">Sin embargo, hay un cambio importante que todos los desarrolladores de Visio deben tener en cuenta: la introducción de los elementos de **sección** , **fila**y **celda**.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="5ceb7-163">En el esquema de formato de archivo de dibujo XML, filas y celdas de la hoja ShapeSheet individuales se representan mediante elementos con nombre.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="5ceb7-164">Por ejemplo, imagine que tiene un documento con una sola página que contiene una forma con un valor de **PinX** de "2" (lo que significa que el eje de giro de la forma es de 2 pulgadas desde el borde izquierdo del dibujo).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="5ceb7-165">El marcado relevante para que la configuración en el formato de archivo de dibujo XML se muestra en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="5ceb7-166">En este caso, el elemento de **PinX** es un elemento secundario del elemento **XForm** , que a su vez es un elemento secundario del elemento de la **forma** .</span><span class="sxs-lookup"><span data-stu-id="5ceb7-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="5ceb7-167">Este modelo de la interfaz de usuario de la ShapeSheet de Visio, donde la celda **PinX** se incluye en la sección **Transformación de forma** de una forma.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="5ceb7-168">En el formato de archivo de Visio 2013, todas las celdas de la ShapeSheet─ **PinX**, **LinePattern**, una celda de **X** en una fila **MoveTo** de una sección **Geometry** , etc.─are representado por un tipo de elemento XML, el elemento de **celda** .</span><span class="sxs-lookup"><span data-stu-id="5ceb7-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="5ceb7-169">Los distintos elementos de **celda** se individuated entre sí por el valor de su atributo **N** .</span><span class="sxs-lookup"><span data-stu-id="5ceb7-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="5ceb7-170">Por lo tanto, en el ejemplo anterior, los datos contenidos en la celda **PinX** de la hoja ShapeSheet se almacenan en un archivo VSDX tal como se muestra en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="5ceb7-171">El elemento de **celda** para **PinX** (así como otras celdas individuales, que se denomina denominadas "singleton celdas" como **LinePattern** o **LockSelect**) es un elemento secundario directo del elemento de **forma** .</span><span class="sxs-lookup"><span data-stu-id="5ceb7-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="5ceb7-172">Ningún elemento único se necesita para representar la fila que contiene la celda **PinX** , tal y como cada forma sólo puede tener una **PinX**.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="5ceb7-173">¿Qué información acerca de las secciones que incluyen datos tabulares, al igual que las secciones de **geometría** ?</span><span class="sxs-lookup"><span data-stu-id="5ceb7-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="5ceb7-174">Para las celdas de esas secciones, el esquema de formato de archivo de Visio 2013 usa **sección** y **fila** elements─also distintivo por su atributo **N** o **T** como se muestra below─to contienen los datos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="5ceb7-175">Por ejemplo, la misma forma del ejemplo anterior podría contener datos en la sección de **geometría 1** que es similar al siguiente código en el esquema de dibujo XML.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="5ceb7-176">Sin embargo, tenga un aspecto similar al siguiente código en el archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="5ceb7-177">Escenarios de desarrollador para trabajar con el formato de archivo de Visio 2013</span><span class="sxs-lookup"><span data-stu-id="5ceb7-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="5ceb7-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="5ceb7-178"></span></span>

<span data-ttu-id="5ceb7-179">Como se explicó anteriormente, el formato de archivo de Visio 2013 aprovecha varias tecnologías bien conocidas como archivos ZIP y XML para almacenar datos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="5ceb7-180">Para manipular un dibujo en el nivel de archivo de Visio 2013, una solución sólo tiene que usar los espacios de nombres de .NET Framework y las clases asociadas a trabajar con archivos ZIP o XML, como [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) o [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="5ceb7-181">La ventaja clave para los programadores del formato de archivo de Visio 2013 es que puedan leer y escribir en los archivos de Visio 2013 sin automatización de la aplicación de cliente de Visio.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="5ceb7-182">Algunos escenarios que pueden considerar como un desarrollador para trabajar con formato de archivo de Visio 2013 incluyen:</span><span class="sxs-lookup"><span data-stu-id="5ceb7-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="5ceb7-183">Comprobación de los archivos de Visio 2013 individuales para los datos específicos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="5ceb7-184">Forma selectiva puede leer un elemento fuera del contenedor ZIP sin tener que extraer todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="5ceb7-185">Actualización de las bibliotecas de Visio 2013 archivos con contenido específico.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="5ceb7-186">Puede cambiar mediante programación el logotipo en todas las páginas de fondo para reflejar las nuevas instrucciones de personalización de marca.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="5ceb7-187">Creación de aplicaciones que consumen los archivos de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="5ceb7-188">Por ejemplo, puede crear una herramienta que lee un diagrama de flujo de trabajo de Visio y, a continuación, ejecuta su propia lógica de negocios en función de ese flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="5ceb7-189">Tenga en cuenta que dado que estas soluciones usan ensamblados .NET Framework estándar, la mayoría de las soluciones que se pueden ejecutar en un equipo cliente también se pueden ejecutar en un servidor.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="5ceb7-190">Exploración mediante programación del formato de archivo de Visio 2013</span><span class="sxs-lookup"><span data-stu-id="5ceb7-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="5ceb7-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="5ceb7-191"></span></span>

<span data-ttu-id="5ceb7-192">La tarea más básica y fundamental para cualquier desarrollador que trabaja con el formato de archivo de Visio 2013 es abrir el archivo como un paquete y, a continuación, obtener acceso a elementos individuales dentro del paquete.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="5ceb7-193">El **System.IO.Packaging.Package** en el WindowsBase.dll contiene muchas clases que permiten abrir y manipular paquetes y elementos.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="5ceb7-194">En el código de ejemplo siguiente, se puede ver cómo abrir un archivo .vsdx, leer la lista de elementos del paquete y obtener información sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="5ceb7-195">Procedimiento para abrir un archivo .vsdx y ver los elementos de documento</span><span class="sxs-lookup"><span data-stu-id="5ceb7-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="5ceb7-196">Abra Visio 2013 y cree un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="5ceb7-197">Cree un documento nuevo y guárdelo en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="5ceb7-198">Abra Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="5ceb7-199">En el menú **archivo** , elija **nuevo**y, a continuación, elija \*\* Project \*\*.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="5ceb7-200">En **Visual C#** o **Visual Basic**, expanda **Windows** y seleccione **aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="5ceb7-201">En el cuadro **nombre** , escriba 'VisioFileExplorer'.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="5ceb7-202">Se abre el proyecto de aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="5ceb7-203">En el **Explorador de soluciones**, haga clic con el botón secundario del mouse en **VisioFileExplorer** y haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="5ceb7-204">En el cuadro de diálogo **Agregar referencia**, **Ensamblados**, expanda **Framework** y seleccione **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="5ceb7-205">Pegue el código siguiente en la solución.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="5ceb7-p126">Presione F5 para depurar la solución. Cuando el programa haya completado su ejecución, presione cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="5ceb7-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ceb7-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ceb7-208">See also</span></span>
<span data-ttu-id="5ceb7-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ceb7-209"></span></span>

<span data-ttu-id="5ceb7-210">Para obtener más información sobre el formato de archivo de Visio 2013, las convenciones de empaquetado abierto o cómo trabajar con archivos de Visio 2013or Office OpenXML mediante programación, vea los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="5ceb7-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="5ceb7-211">Visio para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="5ceb7-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="5ceb7-212">[OPC: nuevo estándar para empaquetar sus datos](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ceb7-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="5ceb7-213">Aspectos básicos de las convenciones de empaquetado abierto</span><span class="sxs-lookup"><span data-stu-id="5ceb7-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="5ceb7-214">Introducción a los formatos de archivo de Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="5ceb7-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

