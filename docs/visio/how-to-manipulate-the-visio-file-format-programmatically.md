---
title: Manipular el formato de archivo de Visio mediante programación
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Crear una solución en Visual Studio 2012 para leer el nuevo paquete de formato de archivo en Visio 2013, seleccionar partes del paquete, cambiar los datos de un elemento y agregar nuevos elementos al paquete.
localization_priority: Priority
ms.openlocfilehash: f54a0afec4bc45d322e3a18194eafc3bd768e0d0
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819304"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="ab10a-103">Manipular el formato de archivo de Visio mediante programación</span><span class="sxs-lookup"><span data-stu-id="ab10a-103">Manipulate the Visio file format programmatically</span></span>

![Tema de procedimiento](media/mod_icon_howto.png)
  
<span data-ttu-id="ab10a-105">Aprenda a crear una solución en Visual Studio 2012 para leer el nuevo paquete de formato de archivo en Visio 2013, seleccionar partes del paquete, cambiar los datos de un elemento y agregar nuevos elementos al paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-105">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="ab10a-106">Conceptos básicos de la manipulación del formato de archivo de Visio</span><span class="sxs-lookup"><span data-stu-id="ab10a-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="ab10a-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-107"><a name="vis15_ManipulateFF_Essentials"> </a></span></span>

<span data-ttu-id="ab10a-108">Versiones anteriores de archivos guardados de Visio en un formato de archivo binario propietario (.vsd) o un único documento en formato de archivo de dibujo XML de Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="ab10a-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="ab10a-109">Visio 2013 presenta un nuevo formato de archivo (.vsdx), que está basado en las tecnologías de archivo XML y ZIP.</span><span class="sxs-lookup"><span data-stu-id="ab10a-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="ab10a-110">Al igual que en versiones anteriores de Visio, los archivos se guardan en un único contenedor.</span><span class="sxs-lookup"><span data-stu-id="ab10a-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="ab10a-111">Sin embargo, a diferencia de los archivos heredados, el nuevo formato de archivo se puede abrir, leer, actualizar, cambiar y construir sin necesidad de automatizar la aplicación de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="ab10a-112">Los programadores que estén familiarizados con la manipulación de XML o con el espacio de nombres [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) pueden comenzar rápidamente a trabajar con el nuevo formato de archivo mediante programación.</span><span class="sxs-lookup"><span data-stu-id="ab10a-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="ab10a-113">Los desarrolladores que han trabajado con los formato de dibujo XML de Visio de versiones anteriores comprobarán que muchas de las estructuras de ese formato se han conservado en el nuevo formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="ab10a-114">En este artículo, examinaremos cómo se trabaja con el formato de archivo de Visio 2013 mediante programación a través de Microsoft .NET Framework 4.5, C# o Visual Basic y Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ab10a-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="ab10a-115">Aprenderá a abrir un archivo de Visio 2013, seleccionar elementos de documento dentro del archivo, cambiar los datos de los elementos y crear un nuevo elemento de documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ab10a-116">Los ejemplos de código de este artículo dan por supuesto que tiene un conocimiento rudimentario de las clases de los espacios de nombres [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8) y [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ab10a-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8) and [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) namespaces.</span></span> <span data-ttu-id="ab10a-117">> En este artículo también se da por supuesto que entiende los conceptos y la terminología de las Convenciones de empaquetado abierto.</span><span class="sxs-lookup"><span data-stu-id="ab10a-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="ab10a-118">Debe estar algo familiarizado con los conceptos paquetes, elementos de documento o elementos de paquete y relaciones.</span><span class="sxs-lookup"><span data-stu-id="ab10a-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="ab10a-119">Para obtener más información, vea [OPC: Nuevo estándar para empaquetar sus datos](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data).</span><span class="sxs-lookup"><span data-stu-id="ab10a-119">For more information, see [OPC: A New Standard for Packaging Your Data](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data).</span></span> <span data-ttu-id="ab10a-120">> El código muestra cómo crear consultas LINQ (Language Integrated Query) para seleccionar código XML.</span><span class="sxs-lookup"><span data-stu-id="ab10a-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="ab10a-121">La mayoría de los ejemplos de código usan la sintaxis de consulta para compilar consultas LINQ.</span><span class="sxs-lookup"><span data-stu-id="ab10a-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="ab10a-122">Puede volver a escribir las consultas LINQ que se proporcionan en el código usando la sintaxis de método de LINQ, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="ab10a-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="ab10a-123">Para obtener más información sobre la sintaxis de métodos y la sintaxis de consultas de LINQ, vea [Sintaxis de consultas y sintaxis de métodos en LINQ (C#)](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)> En la tabla 1 se muestran los temas esenciales con los que debe estar familiarizado antes de trabajar con este artículo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="ab10a-124">**Tabla 1. Conceptos básicos de la manipulación del formato de archivo de Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="ab10a-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="ab10a-125">**Título del artículo**</span><span class="sxs-lookup"><span data-stu-id="ab10a-125">**Article title**</span></span>|<span data-ttu-id="ab10a-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab10a-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab10a-127">Introducción al formato de archivo de Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="ab10a-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="ab10a-128">Esta información general de alto nivel describe algunas de las características principales del formato de archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="ab10a-129">Trata sobre las Convenciones de empaquetado abierto (OPC) que se han aplicado al formato de archivo de Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="ab10a-130">También indica algunas diferencias entre el formato de archivo de Visio 2013 y el formato de archivo anterior de dibujo XML (.vdx) de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="ab10a-131">OPC: Nuevo estándar para empaquetar sus datos</span><span class="sxs-lookup"><span data-stu-id="ab10a-131">OPC: A New Standard for Packaging Your Data</span></span>](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data) <br/> |<span data-ttu-id="ab10a-132">En este artículo de MSDN Magazine se describen las Convenciones de empaquetado abierto como concepto.</span><span class="sxs-lookup"><span data-stu-id="ab10a-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|<span data-ttu-id="ab10a-133">[Aspectos fundamentales de las convenciones de empaquetado abierto](https://docs.microsoft.com/en-us/previous-versions/office/office-12/ee361919(v=office.12))</span><span class="sxs-lookup"><span data-stu-id="ab10a-133">[Essentials of the Open Packaging Conventions](https://docs.microsoft.com/en-us/previous-versions/office/office-12/ee361919(v=office.12))</span></span> <br/> <span data-ttu-id="ab10a-134">[Introducción a los formato de archivo Office (2007) Open XML](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12))</span><span class="sxs-lookup"><span data-stu-id="ab10a-134">[Introducing the Office (2007) Open XML File Formats](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12))</span></span> <br/> |<span data-ttu-id="ab10a-135">En estos dos artículos se explica cómo se han aplicado las Convenciones de empaquetado abierto a los archivos de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="ab10a-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="ab10a-136">Contienen descripciones de cómo funcionan las relaciones en un paquete e incluyen algunos ejemplos de código.</span><span class="sxs-lookup"><span data-stu-id="ab10a-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="ab10a-137">Crear un archivo .vsdx y una nueva solución de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ab10a-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="ab10a-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span></span>

<span data-ttu-id="ab10a-139">Antes de empezar a trabajar con los procedimientos descritos en este artículo, debe crear un archivo de Visio 2013 para abrirlo y manipularlo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="ab10a-140">El dibujo que se usa en los ejemplos de código de este artículo contiene una sola página con dos formas conectadas, una de las cuales es una forma de inicio o finalización de la plantilla "Diagrama de flujo básico".</span><span class="sxs-lookup"><span data-stu-id="ab10a-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="ab10a-141">Use el procedimiento siguiente para crear un nuevo archivo de Visio 2013 que se usará en los demás procedimientos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="ab10a-142">Para crear un nuevo archivo en Visio 2013</span><span class="sxs-lookup"><span data-stu-id="ab10a-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="ab10a-143">Abra Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="ab10a-144">Cree un nuevo documento basado en la plantilla de diagrama de flujo básico. Para ello, elija **CATEGORÍAS**, **Diagrama de flujo**, **Diagrama de flujo básico**, **Crear**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="ab10a-145">Desde la ventana **Formas**, arrastre una forma de **Inicio o finalización** hasta el lienzo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="ab10a-146">Seleccione la nueva forma de inicio o finalización en el lienzo de dibujo y escriba "Begin Process" (Empezar proceso).</span><span class="sxs-lookup"><span data-stu-id="ab10a-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="ab10a-147">Desde la ventana **Formas**, arrastre una forma de **Proceso** hasta el lienzo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="ab10a-148">Seleccione la nueva forma de proceso en el lienzo de dibujo y escriba "Perform some task" (Realizar alguna tarea).</span><span class="sxs-lookup"><span data-stu-id="ab10a-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="ab10a-149">En el menú contextual de la forma de inicio o finalización, seleccione **Agregar un conector a la página** y después dibuje un conector entre las formas de inicio o finalización y de proceso en el lienzo, como se muestra en la figura 1.</span><span class="sxs-lookup"><span data-stu-id="ab10a-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="ab10a-150">**Figura 1. Dibujo sencillo de Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="ab10a-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![Una forma inicial/final conectada a una forma de proceso](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="ab10a-152">Guarde el archivo en el escritorio como un archivo .vsdx. Para ello, elija **Archivos**, **Guardar como**, **Equipo**, **Escritorio**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="ab10a-153">En el cuadro de diálogo **Guardar como**, escriba Paquete de Visio en el cuadro **Nombre de archivo**, seleccione **Dibujo de Visio (\*.vsdx)** en la lista **Guardar como tipo** y elija el botón **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="ab10a-154">Cierre el archivo y después cierre Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="ab10a-155">A veces Visio abre un archivo correctamente incluso si dicho archivo tiene algún problema.</span><span class="sxs-lookup"><span data-stu-id="ab10a-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="ab10a-156">Para asegurarse de que Visio le informe de cualquier problema en el archivo, debe habilitar las advertencias al abrir archivos cuando pruebe soluciones que manipulen archivos de Visio en el nivel de paquete de archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="ab10a-157">> Para habilitar las advertencias al abrir archivos, en Visio 2013, elija **Archivo**, **Opciones**, **Avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="ab10a-158">En **Guardar o abrir**, seleccione **Mostrar advertencias antes de abrir archivos**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="ab10a-159">Estos procedimientos usan una aplicación de consola de Windows para manipular el archivo "Visio Package.vsdx".</span><span class="sxs-lookup"><span data-stu-id="ab10a-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="ab10a-160">Use el procedimiento siguiente para crear y configurar una nueva aplicación de consola de Windows en Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ab10a-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="ab10a-161">Para crear una nueva solución en Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="ab10a-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="ab10a-162">En el menú **Archivo**, elija **Nuevo**, **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="ab10a-163">En el cuadro de diálogo **Nuevo proyecto**, expanda **Visual C#** o **Visual Basic** y después elija **Windows**, **Aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="ab10a-164">En el cuadro **Nombre**, escriba "VisioFileAccessor", seleccione una ubicación para el proyecto y elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="ab10a-165">En el menú **Proyecto**, elija **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="ab10a-166">En el cuadro de diálogo **Administrador de referencias**, en **Ensamblados**, elija **Marco** y después agregue una referencia a los componentes **System.Xml** y **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="ab10a-167">En el archivo Program.cs o Module1.vb del proyecto, agregue las siguientes directivas **using** (instrucciones **Imports** en Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="ab10a-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
    ```cs
    using System.Xml;
    using System.Xml.Linq;
    using System.IO;
    using System.IO.Packaging;
    using System.Text;
    
    ```

    ```vb
    Imports System.Xml
    Imports System.Xml.Linq
    Imports System.IO
    Imports System.IO.Packaging
    Imports System.Text
    
    ```

5. <span data-ttu-id="ab10a-168">También en el archivo Program.cs o Module1.vb, antes del final del método **Main** de la clase **Program** (**Module1** en Visual Basic), agregue el código siguiente que detiene la ejecución de la aplicación de consola hasta que el usuario presione una tecla.</span><span class="sxs-lookup"><span data-stu-id="ab10a-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
    ```cs
    // This code stops the execution of the console application
    // so you can read the output.
    Console.WriteLine("Press any key to continue ...");
    Console.ReadKey();
    
    ```

    ```vb
    ' This code stops the execution of the console application
    ' so you can read the output.
    Console.WriteLine("Press any key to continue ...")
    Console.ReadKey()
    ```

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="ab10a-169">Abrir un archivo de Visio 2013 como un paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="ab10a-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span></span>

<span data-ttu-id="ab10a-171">Para poder manipular los datos del archivo, debe abrir el archivo dentro de un objeto [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8), que está contenido en el espacio de nombres [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ab10a-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8) object, which is contained within the [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) namespace.</span></span> <span data-ttu-id="ab10a-172">El objeto **Package** representa el archivo de Visio como un todo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="ab10a-173">Expone los miembros que permiten seleccionar elementos individuales del documento dentro del paquete de archivos.</span><span class="sxs-lookup"><span data-stu-id="ab10a-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="ab10a-174">En particular, la clase **Package** expone el método [Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8) estático que se usa para abrir un archivo como un paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8) method that you use to open a file as a package.</span></span> <span data-ttu-id="ab10a-175">También expone un método [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8) para cerrar el paquete una vez que se haya terminado con él.</span><span class="sxs-lookup"><span data-stu-id="ab10a-175">It also exposes a [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="ab10a-176">Recomendamos que use un bloque **using** para abrir el archivo de Visio en el objeto **Package** para que no tenga que cerrar explícitamente el paquete de archivos cuando haya terminado con él.</span><span class="sxs-lookup"><span data-stu-id="ab10a-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="ab10a-177">También puede llamar explícitamente al método **Package.Close** del bloque **finally** de una construcción **try/catch/finally**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="ab10a-178">Use el código siguiente para obtener la ruta de acceso completa para el archivo "Visio Package.vsdx" mediante un objeto [FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8), pase la ruta de acceso como un argumento al método **Package.Open** y después devuelva un objeto **Package** al código de llamada.</span><span class="sxs-lookup"><span data-stu-id="ab10a-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="ab10a-179">Para abrir un archivo .vsdx como un paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="ab10a-180">Después del método **Main** de la clase **Program** (o **Module1** en Visual Basic), agregue el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static Package OpenPackage(string fileName, 
        Environment.SpecialFolder folder)
    {
        Package visioPackage = null;
        // Get a reference to the location 
        // where the Visio file is stored.
        string directoryPath = System.Environment.GetFolderPath(
            folder);
        DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
        // Get the Visio file from the location.
        FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
        if (fileInfos.Count() > 0)
        {
            FileInfo fileInfo = fileInfos[0];
            string filePathName = fileInfo.FullName;
            // Open the Visio file as a package with
            // read/write file access.
            visioPackage = Package.Open(
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite);
            }
            // Return the Visio file as a package.
            return visioPackage;
    }
    ```

    ```vb
    Private Function OpenPackage(fileName As String, _
        folder As Environment.SpecialFolder) As Package
        Dim visioPackage As Package = Nothing
        ' Get a reference to the location
        ' where the Visio file is stored.
        Dim directoryPath As String = System.Environment.GetFolderPath( _
            folder)
        Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
        ' Get the Visio file from the location.
        Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
        If (fileInfos.Count() > 0) Then
            Dim fileInfo As FileInfo = fileInfos(0)
            Dim filePathName As String = fileInfo.FullName
            ' Open the Visio file as a package 
            ' with read/write access.
            visioPackage = Package.Open( _
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite)
            End If
        ' Return the Visio file as a package.
        Return visioPackage
    End Function
    
    ```

2. <span data-ttu-id="ab10a-181">En el método **Main** de la clase **Program** (o **Module1** en Visual Basic), agregue el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    // Open the Visio file in a Package object.
    using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
        Environment.SpecialFolder.Desktop))
    {
    }
    
    ```

    ```vb
    ' Open the Visio file in a Package object.
    Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
        Environment.SpecialFolder.Desktop)
    End Using
    
    ```

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="ab10a-182">Seleccionar y leer elementos de un paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-182">Select and read package parts from a package</span></span>
<span data-ttu-id="ab10a-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span></span>

<span data-ttu-id="ab10a-184">Una vez que tenga el archivo de Visio 2013 abierto como un paquete, puede tener acceso a sus elementos de documento mediante la clase [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) incluida en el espacio de nombres **System.IO.Packaging**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="ab10a-185">Se pueden crear instancias de objetos **PackagePart** individualmente o como un conjunto</span><span class="sxs-lookup"><span data-stu-id="ab10a-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="ab10a-186">La clase **Package** expone un método [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) y un método [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) para obtener objetos **PackagePart** de **Package**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="ab10a-187">El método **Package.GetParts** devuelve una instancia de la clase [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx), con la que después puede interactuar de la misma manera que cualquier otra colección que implemente la interfaz [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2).</span><span class="sxs-lookup"><span data-stu-id="ab10a-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) interface.</span></span> 
  
<span data-ttu-id="ab10a-188">Use el código del procedimiento siguiente para obtener un objeto **PackagePartCollection** de la clase **Package** como una colección, iterar en los objetos **PackagePart** de la colección y escribir el URI y el tipo de contenido de cada objeto **PackagePart** en la consola.</span><span class="sxs-lookup"><span data-stu-id="ab10a-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="ab10a-189">Para iterar en los elementos de un paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="ab10a-190">Después del método `OpenPackage` de la clase **Program** (o **Module1** en Visual Basic), agregue el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static void IteratePackageParts(Package filePackage)
    {
        
        // Get all of the package parts contained in the package
        // and then write the URI and content type of each one to the console.
        PackagePartCollection packageParts = filePackage.GetParts();
        foreach (PackagePart part in packageParts)
        {
            Console.WriteLine("Package part URI: {0}", part.Uri);
            Console.WriteLine("Content type: {0}", part.ContentType.ToString());
        }
    }
    
    ```

    ```vb
    Private Sub IteratePackageParts(filePackage As Package)
        ' Get all of the package parts contained in the package
        ' and then write the URI and content type of each one to the console.
        Dim packageParts As PackagePartCollection = filePackage.GetParts()
        For Each part In packageParts
            Console.WriteLine("Package part: {0}", part.Uri)
            Console.WriteLine("Content type: {0}", part.ContentType.ToString())
        Next
    End Sub 
    
    ```

2. <span data-ttu-id="ab10a-191">Agregue el código siguiente dentro del bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic): </span><span class="sxs-lookup"><span data-stu-id="ab10a-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. <span data-ttu-id="ab10a-p112">Elija la tecla F5 para depurar la solución. Cuando el programa haya completado su ejecución, elija cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p112">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="ab10a-194">La aplicación de consola produce una salida similar a la siguiente (se ha omitido parte de la salida por razones de brevedad):</span><span class="sxs-lookup"><span data-stu-id="ab10a-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
<span data-ttu-id="ab10a-195">La mayoría de las veces tendrá que seleccionar un objeto **PackagePart** sin necesidad de iterar en todos ellos.</span><span class="sxs-lookup"><span data-stu-id="ab10a-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="ab10a-196">Puede obtener un objeto **PackagePart** de **Package** mediante su relación con **Package** u otro objeto **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="ab10a-197">Una relación en el formato de archivo de Visio 2013 es una entidad discreta que describe la manera en que un elemento del documento se relaciona con el paquete de archivos o la manera en que dos elementos del documento se relacionan entre sí.</span><span class="sxs-lookup"><span data-stu-id="ab10a-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="ab10a-198">Por ejemplo, el propio paquete de archivos de Visio 2013 tiene una relación con su elemento de documento de Visio, y el elemento de documento de Visio tiene una relación con el elemento de Windows.</span><span class="sxs-lookup"><span data-stu-id="ab10a-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="ab10a-199">Estas relaciones se representan como instancias de las clases [PackageRelationship](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationship?view=netframework-4.8) o [PackageRelationshipCollection](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationshipcollection?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ab10a-199">These relationships are represented as instances of the [PackageRelationship](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationship?view=netframework-4.8) or [PackageRelationshipCollection](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationshipcollection?view=netframework-4.8) classes.</span></span> 
  
<span data-ttu-id="ab10a-200">La clase **Package** expone varios métodos para obtener las relaciones que contiene como objetos **PackageRelationship** o **PackageRelationshipCollection**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="ab10a-201">Puede usar el método [GetRelationshipsByType(String)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.getrelationshipsbytype?redirectedfrom=MSDN&view=netframework-4.8#System_IO_Packaging_Package_GetRelationshipsByType_System_String_) para instanciar un objeto **PackageRelationshipCollection** que contenga objetos **PackageRelationship** de un único tipo específico.</span><span class="sxs-lookup"><span data-stu-id="ab10a-201">You can use the [GetRelationshipsByType(String)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.getrelationshipsbytype?redirectedfrom=MSDN&view=netframework-4.8#System_IO_Packaging_Package_GetRelationshipsByType_System_String_) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="ab10a-202">Evidentemente, para usar el método **Package.GetRelationshipsByType** debe conocer el tipo de relación que necesita.</span><span class="sxs-lookup"><span data-stu-id="ab10a-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="ab10a-203">Los tipos de relación son cadenas en el formato del espacio de nombres XML.</span><span class="sxs-lookup"><span data-stu-id="ab10a-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="ab10a-204">Por ejemplo, el tipo de relación del elemento de documento de Visio es https://schemas.microsoft.com/visio/2010/relationships/document.</span><span class="sxs-lookup"><span data-stu-id="ab10a-204">For example, the relationship type of the Visio Document part is https://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="ab10a-p115">Una vez que conozca la relación de un objeto **PackagePart** con la clase **Package** o con otro objeto **PackagePart** (es decir, tiene un objeto **PackageRelationship** que hace referencia al objeto **PackagePart** que quiere), puede usar esa relación para obtener el identificador URI de dicho objeto **PackagePart**. Después, pase el identificador URI al método **Package.GetPart** para devolver el objeto **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p115">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**. You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ab10a-207">También puede obtener una referencia a un objeto **PackagePart** determinado si usa solo el método **Package.GetPart** y el URI del objeto **PackagePart**, omitiendo el paso en el que obtiene las relaciones de los elementos del paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="ab10a-208">Sin embargo, algunos elementos del paquete de archivos de Visio se pueden guardar en ubicaciones distintas de sus ubicaciones predeterminadas en un paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="ab10a-209">No dé por supuesto que un elemento de paquete siempre se encuentra en el mismo URI para cada archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="ab10a-210">> En su lugar, recomendamos que use las relaciones para tener acceso a objetos **PackagePart** individuales.</span><span class="sxs-lookup"><span data-stu-id="ab10a-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="ab10a-211">Use el procedimiento siguiente para obtener un objeto **PackagePart** (el elemento de documento de Visio) mediante un objeto **PackageRelationship** de la clase **Package** que hace referencia al elemento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="ab10a-212">Para seleccionar un elemento específico del paquete mediante una relación</span><span class="sxs-lookup"><span data-stu-id="ab10a-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="ab10a-213">Después del método `IteratePackageParts` de la clase **Program** (o **Module1** en Visual Basic), agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        string relationship)
    {
        
        // Use the namespace that describes the relationship 
        // to get the relationship.
        PackageRelationship packageRel = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart part = null;
        // If the Visio file package contains this type of relationship with 
        // one of its parts, return that part.
        if (packageRel != null)
        {
            // Clean up the URI using a helper class and then get the part.
            Uri docUri = PackUriHelper.ResolvePartUri(
                new Uri("/", UriKind.Relative), packageRel.TargetUri);
            part = filePackage.GetPart(docUri);
        }
        return part;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, relationship As String) _
        As PackagePart
        ' Use the namespace that describes the relationship 
        ' to get the relationship.
        Dim packageRel As PackageRelationship = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
        Dim part As PackagePart = Nothing
        ' If the Visio file package contains this type of relationship with 
        ' one of its parts, return that part.
        If Not IsNothing(packageRel) Then
            ' Clean up the URI using a helper class and then get the part.
            Dim docUri = PackUriHelper.ResolvePartUri( _
                New Uri("/", UriKind.Relative), packageRel.TargetUri)
            part = filePackage.GetPart(docUri)
        End If
        Return part
    End Function
    
    ```

2. <span data-ttu-id="ab10a-214">Reemplace el código del bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic) por el código siguiente. </span><span class="sxs-lookup"><span data-stu-id="ab10a-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "https://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "https://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

<span data-ttu-id="ab10a-215">Como se mencionó anteriormente, también puede obtener objetos **PackagePart** mediante su relación con otros objetos **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="ab10a-216">Esto es importante porque, para un documento de Visio de cierta complejidad, la mayoría de los objetos **PackagePart** no tienen una relación con la clase **Package**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="ab10a-217">Por ejemplo, un elemento de contenido de página individual del paquete de archivo (es decir, /visio/pages/page1.xml) tiene una relación con el elemento de índice de página (es decir, /visio/pages/pages.xml), pero no con el propio paquete de archivos.</span><span class="sxs-lookup"><span data-stu-id="ab10a-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="ab10a-218">Si no tiene el identificador URI exacto de la página individual del paquete, puede usar su relación con el elemento de índice de página para obtener una referencia a él.</span><span class="sxs-lookup"><span data-stu-id="ab10a-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="ab10a-219">La clase **PackagePart** expone un método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) que puede usar para devolver un objeto **PackageRelationshipCollection** que contenga solo un tipo de objeto **PackageRelationship**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="ab10a-220">Cuando tenga **PackageRelationshipCollection**, podrá seleccionar el elemento **PackageRelationship** que necesite de la colección y después hacer referencia al objeto **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="ab10a-221">Use el código siguiente para obtener **PackagePart** de **Package** mediante su relación con (obteniendo un objeto **PackageRelationship** de) otro objeto **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="ab10a-222">Para seleccionar un elemento de paquete específico a partir de su relación con otro elemento de paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="ab10a-223">Después del método `GetPackagePart` de la clase **Program** (o **Module1** en Visual Basic), agregue el método de sobrecarga siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        PackagePart sourcePart, string relationship)
    {
        // This gets only the first PackagePart that shares the relationship
        // with the PackagePart passed in as an argument. You can modify the code
        // here to return a different PackageRelationship from the collection.
        PackageRelationship packageRel = 
            sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart relatedPart = null;
        if (packageRel != null)
        {
            // Use the PackUriHelper class to determine the URI of PackagePart
            // that has the specified relationship to the PackagePart passed in
            // as an argument.
            Uri partUri = PackUriHelper.ResolvePartUri(
                sourcePart.Uri, packageRel.TargetUri);
            relatedPart = filePackage.GetPart(partUri);
        }
        return relatedPart;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, 
        sourcePart As PackagePart, relationship As String) As PackagePart
        ' This gets only the first PackagePart that shares the relationship
        ' with the PackagePart passed in as an argument. You can modify the
        ' code to return a different PackageRelationship from the collection.
        Dim packageRel As PackageRelationship = sourcePart. _
            GetRelationshipsByType(relationship).FirstOrDefault()
        Dim relatedPart As PackagePart = Nothing
        If Not IsNothing(packageRel) Then
            ' Use the PackUriHelper class to determine the URI of the 
            ' PackagePart that has the specified relationship to the 
            ' PackagePart passed in as an argument.
            Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
                sourcePart.Uri, packageRel.TargetUri)
            relatedPart = filePackage.GetPart(partUri)
        End If
        Return relatedPart
    End Function
    ```

2. <span data-ttu-id="ab10a-p119">Agregue el código siguiente en el bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic), debajo del código del procedimiento anterior. (No elimine el código que agregó en el procedimiento anterior). </span><span class="sxs-lookup"><span data-stu-id="ab10a-p119">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure. (Do not delete the code that you added in the previous procedure.)</span></span> 
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

<span data-ttu-id="ab10a-226">Para poder realizar cambios en el código XML incluido en un elemento de documento, debe cargar el documento XML en un objeto que permita leer el código XML, mediante la clase [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) o la clase [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab10a-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="ab10a-227">Ambas clases exponen métodos para tareas como seleccionar elementos XML contenidos en los documentos XML; crear, leer y escribir atributos; e insertar nuevos elementos XML en un documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="ab10a-p121">De estas dos, la clase **XDocument** permite consultar el código XML mediante LINQ. Con LINQ, puede seleccionar fácilmente los elementos individuales de un documento XML creando consultas, en lugar de iterar en todos los elementos de una colección y probar los elementos que necesita. Por estas razones, los siguientes procedimientos de este artículo usan la clase **XDocument** y otras clases del espacio de nombres **System.Xml.Linq** para trabajar con código XML.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p121">Of the two, the **XDocument** class allows you to query the XML using LINQ. With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need. For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="ab10a-231">Use el procedimiento siguiente para abrir un objeto **PackagePart** como un documento XML en un objeto **XDocument**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="ab10a-232">Para leer el código XML de un elemento de paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="ab10a-233">Después de la última sobrecarga del método `GetPackagePart` de la clase **Program** (o **Module1** en Visual Basic), agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static XDocument GetXMLFromPart(PackagePart packagePart)
    {
        XDocument partXml = null;
        // Open the packagePart as a stream and then 
        // open the stream in an XDocument object.
        Stream partStream = packagePart.GetStream();
        partXml = XDocument.Load(partStream);
        return partXml;
    }
    ```

    ```vb
    Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
        Dim partXml As XDocument = Nothing
        ' Open the packagePart as a stream and then
        ' open the stream in an an XDocument object.
        Dim partStream As Stream = packagePart.GetStream()
        partXml = XDocument.Load(partStream)
        Return partXml
    End Function
    ```

2. <span data-ttu-id="ab10a-234">Agregue el código siguiente en el bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic), debajo del código del procedimiento anterior. </span><span class="sxs-lookup"><span data-stu-id="ab10a-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="ab10a-235">Seleccionar y cambiar los datos XML de un elemento de un paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="ab10a-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span></span>

<span data-ttu-id="ab10a-p122">Una vez que haya cargado un elemento de documento en un objeto **XDocument**, puede usar LINQ para seleccionar elementos XML y realizar cambios en el documento XML. Puede cambiar datos XML, agregar o quitar datos y volver a guardar el documento XML en el elemento de documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p122">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document. You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="ab10a-239">La tarea más común para manipular el formato de archivo de Visio consiste en seleccionar elementos XML específicos o colecciones de elementos del documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="ab10a-240">El espacio de nombres **System.Xml.Linq** incluye la clase [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx), que representa un elemento XML.</span><span class="sxs-lookup"><span data-stu-id="ab10a-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="ab10a-241">La clase **XElement** proporciona acceso a los datos contenidos en el archivo de Visio en un nivel pormenorizado, desde elementos **Shape** individuales hasta elementos **ValidationRule** (como ejemplos).</span><span class="sxs-lookup"><span data-stu-id="ab10a-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="ab10a-242">Use el código siguiente para seleccionar los elementos **Shape** de un objeto **XDocument** (que contenga un elemento de contenido de página) y después seleccionar un elemento **Shape** determinado.</span><span class="sxs-lookup"><span data-stu-id="ab10a-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="ab10a-243">Para seleccionar un elemento específico de un elemento de paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="ab10a-244">Después del método `GetXMLFromPart` de la clase **Program** (o **Module1** en Visual Basic), agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
        
    ```cs
    private static IEnumerable<XElement> GetXElementsByName(
        XDocument packagePart, string elementType)
    {
        // Construct a LINQ query that selects elements by their element type.
        IEnumerable<XElement> elements = 
            from element in packagePart.Descendants() 
            where element.Name.LocalName == elementType 
            select element;
        // Return the selected elements to the calling code.
        return elements.DefaultIfEmpty(null);
    }
    
    ```

    ```vb
    Private Function GetXElementsByName(partXML As XDocument, _
        elementType As String) As IEnumerable(Of XElement)
        ' Construct a LINQ query that selects elements by their element type.
        Dim elements As IEnumerable(Of XElement) =
            From element In partXML.Descendants()
            Where element.Name.LocalName = elementType
            Select element
        ' If there aren't any elements of the specified type
        ' in the document, return Nothing to the calling code.
        Return elements.DefaultIfEmpty(Nothing)
    End Function
    ```

2. <span data-ttu-id="ab10a-245">Después del método `GetXElementsByName` de la clase **Program** (o **Module1** en Visual Basic) del paso anterior, agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
        string attributeName, string attributeValue) 
    {
        // Construct a LINQ query that selects elements from a group
        // of elements by the value of a specific attribute.
        IEnumerable<XElement> selectedElements = 
            from el in elements
            where el.Attribute(attributeName).Value == attributeValue
            select el;
        // If there aren't any elements of the specified type
        // with the specified attribute value in the document,
        // return null to the calling code.
        return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
    }
    ```

    ```vb
    Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
        attributeName As String, attributeValue As String) As XElement
        ' Construct a LINQ query that selects elements from a group
        ' of elements by the value of a specific attribute.
        Dim selectedElements As IEnumerable(Of XElement) =
            From el In elements
            Where el.Attribute(attributeName).Value = attributeValue
            Select el
        ' If there aren't any elements of the specified type 
        ' with the specified attribute value in the document,
        ' return Nothing to the calling code.
        Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
    End Function
    
    ```

3. <span data-ttu-id="ab10a-246">Agregue el código siguiente en el bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic), debajo del código del procedimiento anterior. </span><span class="sxs-lookup"><span data-stu-id="ab10a-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Get all of the shapes from the page by getting
    // all of the Shape elements from the pageXML document.
    IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
    // Select a Shape element from the shapes on the page by 
    // its name. You can modify this code to select elements
    // by other attributes and their values.
    XElement startEndShapeXML = 
        GetXElementByAttribute(shapesXML, "NameU", "Start/End");
    
    ```

    ```vb
    ' Get all of the shapes from the page by getting
    ' all of the Shape elements from the pageXML document.
    Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
        pageXML, "Shape")
    ' Select a Shape element from the shapes on the page by
    ' its name. You can modify this code to select elements
    ' by other attributes and their values.
    Dim startEndShapeXML As XElement = GetXElementByAttribute( _
        shapesXML, "NameU", "Start/End")
    ```

<span data-ttu-id="ab10a-247">Una vez que haya obtenido una referencia a un objeto **XElement** contenido en un objeto **XDocument**, puede manipularlo como cualquier otro dato XML y, por lo tanto, modificar los datos contenidos en el archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="ab10a-248">Por ejemplo, si una forma tiene texto cuando se abre en Visio, el elemento **Shape** correspondiente contendrá al menos un elemento **Text**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="ab10a-249">Si cambia el valor de ese elemento **Text**, el texto de la forma cambia cuando el archivo se visualiza en Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="ab10a-250">Agregue el código siguiente al bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic) para cambiar el texto de la forma de inicio o finalización de "Begin process" (Empezar proceso) a "Start process" (Iniciar proceso).</span><span class="sxs-lookup"><span data-stu-id="ab10a-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> <span data-ttu-id="ab10a-251">En el ejemplo de código anterior, el texto de la forma existente y la cadena usada para reemplazarlo tienen el mismo número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ab10a-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="ab10a-252">Tenga en cuenta también que la consulta LINQ cambia el valor del último nodo secundario del elemento devuelto (que, en este caso, es un nodo de texto).</span><span class="sxs-lookup"><span data-stu-id="ab10a-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="ab10a-253">Esto se hace para evitar cambiar la configuración del elemento **cp**, que es un elemento secundario del elemento **Text**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="ab10a-254">> Es posible que se cause inestabilidad en el archivo si se modifica el texto de una forma mediante programación sobrescribiendo todos los elementos secundarios del elemento **Text**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="ab10a-255">Como en el ejemplo anterior, el formato de texto se representa mediante elementos **cp** bajo el elemento **Text** del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="ab10a-256">La definición del formato se almacena en el elemento primario **Section**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="ab10a-257">Si estos dos fragmentos de información son incoherentes, es posible que el archivo no se comporte de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="ab10a-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="ab10a-258">Visio resuelve muchas incoherencias, pero es mejor asegurarse de que cualquier cambio introducido mediante programación sea coherente para controlar el comportamiento final del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="ab10a-p126">Cuando se realizan cambios en el código XML de un elemento de documento, dichos cambios solo existen en la memoria. Para conservar los cambios en el archivo, debe guardar el XML en el elemento de documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p126">When you make changes to the XML of a document part, those changes exist in memory only. To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="ab10a-261">El código siguiente usa la clase [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) y la clase [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) para volver a escribir el código XML en el elemento de paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="ab10a-262">Aunque puede usar el método [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) para guardar el código XML en el elemento, las clases **XmlWriter** y **XmlWriterSettings** permiten un mayor control sobre la salida, incluida la especificación del tipo de codificación.</span><span class="sxs-lookup"><span data-stu-id="ab10a-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="ab10a-263">La clase **XDocument** expone un método [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) que toma un objeto **XmlWriter** y escribe XML de nuevo en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="ab10a-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="ab10a-264">Use el procedimiento siguiente para guardar el código XML de la página de Visio en el elemento de contenido de página.</span><span class="sxs-lookup"><span data-stu-id="ab10a-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="ab10a-265">Para guardar el código XML cambiado en el paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="ab10a-266">Después del método `GetXElementByAttribute` de la clase **Program** (o **Module1** en Visual Basic) del paso anterior, agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void SaveXDocumentToPart(PackagePart packagePart, 
        XDocument partXML)
    {
        
        // Create a new XmlWriterSettings object to 
        // define the characteristics for the XmlWriter
        XmlWriterSettings partWriterSettings = new XmlWriterSettings();
        partWriterSettings.Encoding = Encoding.UTF8;
        // Create a new XmlWriter and then write the XML
        // back to the document part.
        XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
            partWriterSettings);
        partXML.WriteTo(partWriter);
        // Flush and close the XmlWriter.
        partWriter.Flush();
        partWriter.Close();
    }
    ```

    ```vb
    Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
        partXML As XDocument)
        ' Create a new XmlWriterSettings object to 
        ' define the characteristics for the XmlWriter.
        Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
        partWriterSettings.Encoding = Encoding.UTF8
        ' Create a new XmlWriter and then write the XML
        ' back to the document part.
        Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
        partXML.WriteTo(partWriter)
        ' Flush and close the XmlWriter.
        partWriter.Flush()
        partWriter.Close()
    End Sub
    ```

2. <span data-ttu-id="ab10a-267">Agregue el código siguiente en el bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic), debajo del código del procedimiento anterior. </span><span class="sxs-lookup"><span data-stu-id="ab10a-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. <span data-ttu-id="ab10a-p128">Elija la tecla F5 para depurar la solución. Cuando el programa haya completado su ejecución, elija cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p128">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="ab10a-270">Abra el archivo Package.vsdx de Visio en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="ab10a-271">La forma de inicio o finalización ahora debería contener el texto "Start process" (Iniciar proceso).</span><span class="sxs-lookup"><span data-stu-id="ab10a-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="ab10a-272">Recalcular los datos del archivo</span><span class="sxs-lookup"><span data-stu-id="ab10a-272">Recalculate data in the file</span></span>
<span data-ttu-id="ab10a-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span></span>

<span data-ttu-id="ab10a-274">Algunos de los cambios a los datos de un archivo pueden requerir que Visio vuelva a calcular el documento al abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="ab10a-275">Visio ofrece mucha lógica para un diagrama, especialmente para relaciones de forma (es decir, cuando una forma depende de otra) y para la conexión de formas.</span><span class="sxs-lookup"><span data-stu-id="ab10a-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="ab10a-276">Si se cambia alguno de los datos en los que se basa la lógica personalizada, Visio debe propagar los cambios en todos los datos calculados del archivo que se vean afectados.</span><span class="sxs-lookup"><span data-stu-id="ab10a-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="ab10a-277">El formato de archivo de Visio 2013 incluye un par de técnicas que puede usar para recalcular los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="ab10a-278">Hay tres tipos de escenarios que debe tener en cuenta cuando decida si necesita recalcular el archivo de Visio y cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="ab10a-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="ab10a-279">Los cambios en los datos no afectan a otros valores del formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="ab10a-280">No es necesario agregar instrucciones adicionales en Visio para recalcular el documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="ab10a-281">Tal como se mostró anteriormente, a veces se puede cambiar el texto de una forma sin necesidad de recalcular el documento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="ab10a-282">Los cambios en los datos están limitados a cambios en los valores de las celdas de ShapeSheet en XML, y hay otros valores de ShapeSheet que dependen de estos datos.</span><span class="sxs-lookup"><span data-stu-id="ab10a-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="ab10a-283">En este caso, debe agregar una instrucción de procesamiento XML (mediante la clase [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)) al elemento **Cell** que haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="ab10a-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="ab10a-284">Por ejemplo, la celda **ThemeIndex** de una forma afecta a los valores de otras celdas de ShapeSheet contenidas en la forma.</span><span class="sxs-lookup"><span data-stu-id="ab10a-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="ab10a-285">Si cambia la celda **ThemeIndex** dentro del propio archivo (por ejemplo, el elemento **Cell** con un valor **N** de "ThemeIndex"), deberá agregar una instrucción de procesamiento al elemento **Cell** para que los valores dependientes se actualicen.</span><span class="sxs-lookup"><span data-stu-id="ab10a-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="ab10a-286">Los cambios en los datos afectan a la ubicación de un conector o de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab10a-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="ab10a-287">Otra posible situación es que haya muchos cambios en los datos de ShapeSheet y quiera recalcular todo el documento con una sola instrucción (en lugar de agregar instrucciones de procesamiento individuales para cada cambio).</span><span class="sxs-lookup"><span data-stu-id="ab10a-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="ab10a-288">En este caso, puede indicar a Visio que recalcule todo el documento al abrirlo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="ab10a-289">Para ello, agregue una propiedad **RecalcDocument** al elemento de propiedades de archivo personalizadas (/docProps/custom.xml) del paquete de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="ab10a-290">Un ejemplo de este tipo de escenario es el proceso de ajustar la posición o el tamaño de las formas de un diagrama conectado.</span><span class="sxs-lookup"><span data-stu-id="ab10a-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="ab10a-291">Tenga en cuenta que esta es la opción más costosa desde el punto de vista del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ab10a-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="ab10a-292">Use el procedimiento siguiente para insertar un elemento **Cell** en un elemento **Shape**, donde otros elementos **Cell** del mismo elemento **Shape** necesitan recalcularse debido al nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="ab10a-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="ab10a-293">El nuevo elemento **Cell** incluye una instrucción de procesamiento como un elemento secundario, para informar a Visio de que debe realizar algún cálculo local.</span><span class="sxs-lookup"><span data-stu-id="ab10a-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="ab10a-294">Para recalcular los valores de una sola forma</span><span class="sxs-lookup"><span data-stu-id="ab10a-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="ab10a-295">Reemplace el código de los dos ejemplos anteriores (cambiando el texto de la forma y la llamada a `SaveXDocumentToPart`) del bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic) por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Insert a new Cell element in the Start/End shape that adds an arbitrary
    // local ThemeIndex value. This code assumes that the shape does not 
    // already have a local ThemeIndex cell.
    startEndShapeXML.Add(new XElement("Cell",
        new XAttribute("N", "ThemeIndex"),
        new XAttribute("V", "25"),
        new XProcessingInstruction("NewValue", "V")));
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Insert a new Cell element in the shape that adds an arbitrary local
    ' ThemeIndex value. This code assumes that the shape does not
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. <span data-ttu-id="ab10a-p135">Elija la tecla F5 para depurar la solución. Cuando el programa haya completado su ejecución, elija cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p135">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="ab10a-298">Abra el archivo Package.vsdx de Visio en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="ab10a-299">La forma de inicio o finalización ahora debería tener un color de relleno diferente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="ab10a-300">El color de la forma se basa en el valor de la celda **ThemeIndex**, que determina de qué tema activo hereda la forma.</span><span class="sxs-lookup"><span data-stu-id="ab10a-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="ab10a-301">En el ejemplo anterior, se establece que la forma hereda de un tema diferente (la celda **ThemeIndex** está establecida en un valor de "25").</span><span class="sxs-lookup"><span data-stu-id="ab10a-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="ab10a-302">Si no usa una instrucción de procesamiento, el color del texto de la forma (que también se ve afectado por la celda **ThemeIndex**) no se recalcula.</span><span class="sxs-lookup"><span data-stu-id="ab10a-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="ab10a-303">El color de relleno de la forma cambiaría a blanco, pero el texto seguiría siendo blanco y, por tanto, ilegible.</span><span class="sxs-lookup"><span data-stu-id="ab10a-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="ab10a-304">Además, sin la instrucción de procesamiento, es posible que Visio actualice la forma en una fecha posterior, por lo que el archivo permanecería en un estado inestable y los valores de formato de la forma podrían actualizarse de una manera impredecible.</span><span class="sxs-lookup"><span data-stu-id="ab10a-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="ab10a-305">Si cambia los datos del archivo de modo que Visio tenga que recalcular el documento (por ejemplo, cambia la posición de una forma conectada y, por lo tanto, obliga a los conectores a volver a enrutarse), debe agregar una instrucción de actualización en el archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="ab10a-306">La instrucción se crea agregando un elemento **property** con un valor de atributo **name** de "RecalcDocument" al código XML del elemento de propiedades de archivo personalizadas del paquete de archivos de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="ab10a-307">Recomendamos que compruebe el elemento de propiedades de archivo personalizadas para asegurarse de que todavía no se ha registrado ninguna instrucción "RecalcDocument" en el archivo.</span><span class="sxs-lookup"><span data-stu-id="ab10a-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="ab10a-308">Use el código siguiente para cambiar el valor de la celda **PinY** de la forma de inicio o finalización de los ejemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="ab10a-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="ab10a-309">El código selecciona el elemento **Cell** que contiene los datos de la celda **PinY** como un objeto **XElement** mediante el valor de su atributo **N**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="ab10a-310">Después, el código agrega una instrucción de actualización al elemento de propiedades de archivo personalizadas del archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab10a-311">Este código se basa en los métodos `GetPackagePart` y `SaveXDocumentToPart` creados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="ab10a-312">Para recalcular todo el documento al abrirlo</span><span class="sxs-lookup"><span data-stu-id="ab10a-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="ab10a-313">Después del método `SaveXDocumentToPart` de la clase **Program** (o **Module1** en Visual Basic) del paso anterior, agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
            "custom-properties");
        XDocument customPartXML = GetXMLFromPart(customPart);
        // Check to see whether document recalculation has already been 
        // set for this document. If it hasn't, use the integer
        // value returned by CheckForRecalc as the property ID.
        int pidValue = CheckForRecalc(customPartXML);
        if (pidValue > -1)
        {
            XElement customPartRoot = customPartXML.Elements().ElementAt(0);
            // Two XML namespaces are needed to add XML data to this 
            // document. Here, we're using the GetNamespaceOfPrefix and 
            // GetDefaultNamespace methods to get the namespaces that 
            // we need. You can specify the exact strings for the 
            // namespaces, but that is not recommended.
            XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
            XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
            // Construct the XML for the new property in the XDocument.Add method.
            // This ensures that the XNamespace objects will resolve properly, 
            // apply the correct prefix, and will not default to an empty namespace.
            customPartRoot.Add(
                new XElement(customPropsSchemaNS + "property",
                    new XAttribute("pid", pidValue.ToString()),
                    new XAttribute("name", "RecalcDocument"),
                    new XAttribute("fmtid", 
                        "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                    new XElement(customVTypesNS + "bool", "true")
                ));
        }
        // Save the Custom Properties package part back to the package.
        SaveXDocumentToPart(customPart, customPartXML);
    }
    ```

    ```vb
    Private Sub RecalcDocument(filePackage As Package)
            ' Get the Custom File Properties part from the package and
            ' then extract the XML from it.
            Dim customPart As PackagePart = GetPackagePart(filePackage, _
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
                "relationships/custom-properties")
            Dim customPartXML As XDocument = GetXMLFromPart(customPart)
            ' Check to see whether document recalculation has already been
            ' set for this document. If it hasn't, use the integer
            ' value returned by CheckForRecalc as the property ID.
            Dim pidValue As Integer = CheckForRecalc(customPartXML)
            If (pidValue > 1) Then
                Dim customPartRoot As XElement = _
                    customPartXML.Elements().ElementAt(0)
                ' Two XML namespaces are needed to add XML data to this 
                ' document. Here, we're using the GetNamespaceOfPrefix and
                ' GetDefaultNamespace methods to get the namespaces that
                ' we need. You can specify the exact strings for the 
                ' namespaces, but that is not recommended.
                Dim customVTypesNS As XNamespace = _
                    customPartRoot.GetNamespaceOfPrefix("vt")
                Dim customPropsSchemaNS As XNamespace = _
                    customPartRoot.GetDefaultNamespace()
                ' Contruct the XML for the new property in the XDocument.Add
                ' method. This ensures that the XML namespaces resolve 
                ' properly, apply the correct prefix, and do not default to 
                ' an empty namespace.
                customPartRoot.Add( _
                    New XElement(customPropsSchemaNS + "property", _
                        New XAttribute("pid", pidValue.ToString()), _
                        New XAttribute("name", "RecalcDocument"), _
                        New XAttribute("fmtid", _
                            "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                        New XElement(customVTypesNS + "bool", "true") _
                ))
            ' Save the Custom Properties package part back to the package.
            SaveXDocumentToPart(customPart, customPartXML)
            End If
        End Sub
    ```

2. <span data-ttu-id="ab10a-314">Después del método `RecalcDocument` de la clase **Program** (o **Module1** en Visual Basic) del paso anterior, agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static int CheckForRecalc(XDocument customPropsXDoc) 
    {
        
        // Set the inital pidValue to -1, which is not an allowed value.
        // The calling code tests to see whether the pidValue is 
        // greater than -1.
        int pidValue = -1;
        // Get all of the property elements from the document. 
        IEnumerable<XElement> props = GetXElementsByName(
            customPropsXDoc, "property");
        // Get the RecalcDocument property from the document if it exists already.
        XElement recalcProp = GetXElementByAttribute(props, 
            "name", "RecalcDocument");
        // If there is already a RecalcDocument instruction in the 
        // Custom File Properties part, then we don't need to add another one. 
        // Otherwise, we need to create a unique pid value.
        if (recalcProp != null)
        {
            return pidValue;
        }
        else
        {
            // Get all of the pid values of the property elements and then
            // convert the IEnumerable object into an array.
            IEnumerable<string> propIDs = 
                from prop in props
                where prop.Name.LocalName == "property"
                select prop.Attribute("pid").Value;
            string[] propIDArray = propIDs.ToArray();
            // Increment this id value until a unique value is found.
            // This starts at 2, because 0 and 1 are not valid pid values.
            int id = 2;
            while (pidValue == -1)
            {
                if (propIDArray.Contains(id.ToString()))
                {
                    id++;
                }
                else
                {
                    pidValue = id;
                }
            }
        }
        return pidValue;
    }
    
    ```

    ```vb
    Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
        ' Set the initial pidValue to -1, which is not an allowed value. 
        ' The calling code test to see whether the pidValue is
        ' greater than -1.
        Dim pidValue As Integer = -1
        ' Get all of the property elements from the document.
        Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
            customPropsXDoc, "property")
        ' Get the RecalcDocument property from the document if 
        ' it exists already.
        Dim recalcProp As XElement = GetXElementByAttribute(props, _
            "name", "RecalcDocument")
        ' If there is already a RecalcDocument instruction in the 
        ' Custom File Properties part, then we don't need another one.
        ' Otherwise, we need to create a unique pid value.
        If Not IsNothing(recalcProp) Then
            Return pidValue
        Else
            ' Get all of the pid values of the proeprty elements and then
            ' convert the IEnumerable object into an array.
            Dim propIDs As IEnumerable(Of String) = _
            From prop In props
            Where prop.Name.LocalName = "property"
            Select prop.Attribute("pid").Value
            Dim propIDArray As String() = propIDs.ToArray()
            ' Increment this id value until a unique value is found.
            ' This starts at 2, because 0 and 1 are not valid pid values.
            Dim id As Integer = 2
            While (pidValue = -1)
                If (propIDArray.Contains(id.ToString())) Then
                    id = id + 1
                Else
                    pidValue = id
                End If
            End While
        End If
        Return pidValue
    End Function
    ```

3. <span data-ttu-id="ab10a-315">Reemplace el código del ejemplo anterior del bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic) por el código siguiente. </span><span class="sxs-lookup"><span data-stu-id="ab10a-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Change the shape's horizontal position on the page 
    // by getting a reference to the Cell element for the PinY 
    // ShapeSheet cell and changing the value of its V attribute.
    XElement pinYCellXML = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY");
    pinYCellXML.SetAttributeValue("V", "2");
    // Add instructions to Visio to recalculate the entire document
    // when it is next opened.
    RecalcDocument(visioPackage);
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Change the shape's horizontal position on the page
    ' by getting a reference to the Cell element for the PinY
    ' ShapeSheet cell and changing the value of its V attribute.
    Dim pinYCellXML As XElement = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY")
    pinYCellXML.SetAttributeValue("V", "2")
    ' Add instructions to Visio to recalculate the entire document
    ' when it is next opened.
    RecalcDocument(visioPackage)
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

4. <span data-ttu-id="ab10a-p140">Elija la tecla F5 para depurar la solución. Cuando el programa haya completado su ejecución, elija cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p140">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="ab10a-318">Abra el archivo Package.vsdx de Visio en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="ab10a-p141">La forma de inicio o finalización ahora debería encontrarse a 2 pulgadas del borde inferior del dibujo. El conector entre la forma de inicio o finalización y la forma de proceso debe haberse enrutado de nuevo para incluir el cambio en el diseño. Si la propiedad **RecalcDocument** no se hubiera agregado al archivo, la posición de la forma habría cambiado, pero el conector no se habría enrutado a la nueva ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p141">The Start/End shape should now be 2 inches from the bottom edge of the drawing. The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout. If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="ab10a-322">Agregar un nuevo elemento a un paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-322">Add a new package part to a package</span></span>
<span data-ttu-id="ab10a-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span></span>

<span data-ttu-id="ab10a-324">Uno de los escenarios más comunes para modificar un paquete de archivos consiste en agregar un nuevo elemento de documento al paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="ab10a-325">Por ejemplo, si quiere agregar una página al dibujo de Visio mediante la adición de contenido al paquete, debe agregar un elemento de contenido de página al paquete.</span><span class="sxs-lookup"><span data-stu-id="ab10a-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="ab10a-326">El proceso para agregar un nuevo elemento al paquete es sencillo:</span><span class="sxs-lookup"><span data-stu-id="ab10a-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="ab10a-p143">Cree el documento XML con los datos del objeto **PackagePart**. Debe prestar especial atención a los espacios de nombres XML que rigen el esquema del tipo específico de documento XML que cree.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p143">You create the XML document with the data for the **PackagePart**. You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="ab10a-329">Cree un nuevo archivo que contenga el código XML y guárdelo en una ubicación en el objeto **Package**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="ab10a-330">Cree las relaciones necesarias entre el nuevo objeto **PackagePart** y la clase **Package** u otro objeto **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="ab10a-p144">Actualice todos los elementos existentes que necesiten hacer referencia al nuevo elemento. Por ejemplo, si agrega un nuevo elemento de contenido de página (una página nueva) al archivo, debe actualizar también el elemento de índice de página (el archivo /visio/pages/pages.xml) para incluir la información correcta sobre la nueva página.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p144">You update any existing parts that need to reference the new part. For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="ab10a-333">Use el procedimiento siguiente para crear un nuevo elemento de extensibilidad de la cinta de opciones en el archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="ab10a-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="ab10a-334">El nuevo elemento de extensibilidad de la cinta de opciones agrega a la cinta una nueva pestaña con un solo grupo que contiene un solo botón.</span><span class="sxs-lookup"><span data-stu-id="ab10a-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="ab10a-335">Para crear un nuevo elemento de paquete</span><span class="sxs-lookup"><span data-stu-id="ab10a-335">To create a new package part</span></span>

1. <span data-ttu-id="ab10a-336">Después del método `CheckForRecalc` de la clase **Program** (o **Module1** en Visual Basic) del procedimiento anterior, agregue el método siguiente. </span><span class="sxs-lookup"><span data-stu-id="ab10a-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "https://schemas.microsoft.com/office/2006/01/customui";
        XDocument customUIXDoc = new XDocument(
            new XDeclaration("1.0", "utf-8", "true"),
            new XElement(customUINS + "customUI",
                new XElement(customUINS + "ribbon",
                    new XElement(customUINS + "tabs",
                        new XElement(customUINS + "tab",
                            new XAttribute("id", "customTab"),
                            new XAttribute("label", "CUSTOM"),
                            new XElement(customUINS + "group",
                                new XAttribute("id", "customGroup"),
                                new XAttribute("label", "Custom Group"),
                                new XElement(customUINS + "button",
                                    new XAttribute("id", "customButton"),
                                    new XAttribute("label", "Custom Button"),
                                    new XAttribute("size", "large"),
                                    new XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        );
        return customUIXDoc;
    }
    ```

    ```vb
    Private Function CreateCustomUI() As XDocument
        ' Add a new Custom User Interface document part to the package.
        ' This code adds a new CUSTOM tab to the ribbon for this
        ' document. The tab has one group that contains one button.
        Dim customUINS As XNamespace = _
            "https://schemas.microsoft.com/office/2006/01/customui"
        Dim customUIXML = New XDocument( _
            New XDeclaration("1.0", "utf-8", "true"), _
            New XElement(customUINS + "customUI", _
                New XElement(customUINS + "ribbon",
                    New XElement(customUINS + "tabs",
                        New XElement(customUINS + "tab",
                            New XAttribute("id", "customTab"),
                            New XAttribute("label", "CUSTOM"),
                            New XElement(customUINS + "group",
                                New XAttribute("id", "customGroup"),
                                New XAttribute("label", "Custom Group"),
                                New XElement(customUINS + "button",
                                    New XAttribute("id", "customButton"),
                                    New XAttribute("label", "Custom Button"),
                                    New XAttribute("size", "large"),
                                    New XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        )
        Return customUIXML
    End Function
    ```

2. <span data-ttu-id="ab10a-337">Después del método `CreateCustomUI` de la clase **Program** (o **Module1** en Visual Basic) del paso anterior, agregue el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void CreateNewPackagePart(Package filePackage, 
        XDocument partXML, Uri packageLocation, string contentType, 
        string relationship)
    {
        // Need to check first to see whether the part exists already.
        if (!filePackage.PartExists(packageLocation))
        {
            // Create a new blank package part at the specified URI 
            // of the specified content type.
            PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
                contentType);
            // Create a stream from the package part and save the 
            // XML document to the package part.
            using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
                FileAccess.ReadWrite))
            {
                partXML.Save(partStream);
            }
        }
        // Add a relationship from the file package to this
        // package part. You can also create relationships
        // between an existing package part and a new part.
        filePackage.CreateRelationship(packageLocation,
            TargetMode.Internal,
            relationship);
    }
    ```

    ```vb
    Private Sub CreateNewPackagePart(filePackage As Package, _
        partXML As XDocument, packageLocation As Uri, contentType As String, _
        relationship As String)
        ' Need to check first to see whether the part exists already.
        If Not (filePackage.PartExists(packageLocation)) Then
            ' Create a new blank package part at the specified URI
            ' of the specified content type.
            Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
                contentType)
            ' Create a stream from the package part and save the
            ' XML document to the package part.
            Using partStream As Stream = newPart.GetStream(FileMode.Create, _
                FileAccess.ReadWrite)
                partXML.Save(partStream)
            End Using
            ' Add a relationship from the file package to this
            ' package part. You can also create relationships
            ' between an existing package part and a new part.
            filePackage.CreateRelationship(packageLocation, _
                TargetMode.Internal, relationship)
        End If
    End Sub
    ```

3. <span data-ttu-id="ab10a-338">Reemplace todo el código del bloque **using** del método **Main** de la clase **Program** (bloque **Using** del método **Main** en **Module1** en Visual Basic) por el código siguiente. </span><span class="sxs-lookup"><span data-stu-id="ab10a-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. <span data-ttu-id="ab10a-p146">Elija la tecla F5 para depurar la solución. Cuando el programa haya completado su ejecución, elija cualquier tecla para salir.</span><span class="sxs-lookup"><span data-stu-id="ab10a-p146">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="ab10a-341">Abra el archivo Package.vsdx de Visio en Visio 2013 y elija la pestaña **PERSONALIZADO**.</span><span class="sxs-lookup"><span data-stu-id="ab10a-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="ab10a-342">La cinta de opciones personalizada es similar a la figura 2 cuando el archivo se abre en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ab10a-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="ab10a-343">**Figura 2. Pestaña personalizada en la cinta de opciones de Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="ab10a-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![Pestaña personalizada en la cinta](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="ab10a-345">El código XML creado por el método `CreateCustomUI` se parece al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab10a-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="https://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a><span data-ttu-id="ab10a-346">Reconocimientos</span><span class="sxs-lookup"><span data-stu-id="ab10a-346">Acknowledgements</span></span>
<span data-ttu-id="ab10a-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-347"><a name="vis15_ManipulateFF_Ackn"> </a></span></span>

<span data-ttu-id="ab10a-348">Nos gustaría agradecer la contribución y los comentarios de **Al Edlund**, MVP de Visio, en la creación de los ejemplos de código contenidos en este artículo técnico.</span><span class="sxs-lookup"><span data-stu-id="ab10a-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="ab10a-349">Al es un experto en la manipulación del formato de archivo de Visio, incluido el formato de dibujo XML de Visio (.vdx) y el nuevo formato de archivo de Visio (.vsdx).</span><span class="sxs-lookup"><span data-stu-id="ab10a-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="ab10a-350">Al ha creado proyectos que exploran los formatos de archivo de Visio mediante programación y exponen las estructuras internas.</span><span class="sxs-lookup"><span data-stu-id="ab10a-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="ab10a-351">Para obtener más información sobre el trabajo de Al con el formato de archivo de Visio, vea a continuación los vínculos de la sección Recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="ab10a-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab10a-352">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab10a-352">See also</span></span>
<span data-ttu-id="ab10a-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="ab10a-353"><a name="vis15_ManipulateFF_Additional"> </a></span></span>

- <span data-ttu-id="ab10a-354">De Al Edlund:</span><span class="sxs-lookup"><span data-stu-id="ab10a-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="ab10a-355">Proyecto [pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) en CodePlex.</span><span class="sxs-lookup"><span data-stu-id="ab10a-355">[pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="ab10a-356">Vídeo [pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) de YouTube.</span><span class="sxs-lookup"><span data-stu-id="ab10a-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="ab10a-357">Vídeo [pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) de YouTube.</span><span class="sxs-lookup"><span data-stu-id="ab10a-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="ab10a-358">Centro para desarrolladores de Visio</span><span class="sxs-lookup"><span data-stu-id="ab10a-358">Visio Developer Center</span></span>](https://developer.microsoft.com/visio)
    
- <span data-ttu-id="ab10a-359">[Manipulate Office Open XML Formats Documents](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12)) (Manipular documentos con formato de archivo Open XML de Office)</span><span class="sxs-lookup"><span data-stu-id="ab10a-359">[Manipulate Office Open XML Formats Documents](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12))</span></span>
    
- <span data-ttu-id="ab10a-360">[Create a Document with Namespaces (C#) (LINQ to XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140)) [Creación de un documento con espacios de nombres (C#) (LINQ a XML)]</span><span class="sxs-lookup"><span data-stu-id="ab10a-360">[Create a Document with Namespaces (C#) (LINQ to XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140))</span></span>
    
- <span data-ttu-id="ab10a-361">[Add Custom XML Parts to Documents Without Starting Microsoft Office](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90)) (Adición de elementos XML personalizados a documentos sin iniciar Microsoft Office)</span><span class="sxs-lookup"><span data-stu-id="ab10a-361">[Add Custom XML Parts to Documents Without Starting Microsoft Office](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90))</span></span>
    

