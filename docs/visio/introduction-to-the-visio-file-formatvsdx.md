---
title: Introducción al formato de archivo de Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar mediante programación con el formato de archivo de Visio 2013 y crear una aplicación de consola sencilla que examina un archivo de Visio 2013.
ms.openlocfilehash: aa3497af7c467c8f51ab80ab82071776568b4978
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822348"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Introducción al formato de archivo de Visio (.vsdx)

Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar mediante programación con el formato de archivo de Visio 2013 y crear una aplicación de consola sencilla que examina un archivo de Visio 2013.
  
|||
|:-----|:-----|
|**En este artículo** [Introducción](#vis15_IntroVSDX_Intro) [¿Qué es el formato de archivo de Visio 2013 "enfoque técnico"?](#vis15_IntroVSDX_What)                             [Escenarios de desarrollador para trabajar con el formato de archivo de Visio 2013](#vis15_IntroVSDX_Scenarios) [Exploración mediante programación el formato de archivo de Visio 2013](#vis15_IntroVSDX_Explore) [Recursos adicionales](#vis15_IntroVSDX_Resources)                    ||
   
## <a name="introduction"></a>Introducción
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 presenta un nuevo formato de archivo (.vsdx) para Visio que reemplaza el formato de archivo binario de Visio (.vsd) y el formato de archivo de dibujo XML de Visio (.vdx). Debido a que el formato de archivo de Visio 2013 se basa en convenciones de empaquetado abierto y XML, los programadores que están familiarizados con estas tecnologías pueden aprender rápidamente cómo trabajar con archivos de Visio 2013 mediante programación. Los programadores que están familiarizados con el formato de archivo de dibujo de Visio XML (.vdx) desde las versiones anteriores de Visio pueden encontrar muchas de las mismas estructuras XML dentro de los elementos de formato de archivo .vsdx. Interoperabilidad con los archivos de Visio aumenta en gran medida puesto que el software de terceros puede manipular los archivos de Visio en un nivel de formato de archivo. El formato de archivo de Visio 2013 es compatible con los servicios de Visio en Microsoft SharePoint Server 2013, sin necesidad de un formato de archivo "intermediario" para la publicación en SharePoint Server.
  
Hay varios tipos de archivo, por extensión, que conforman el formato de archivo de Visio 2013. Estas extensiones incluyen:
  
- .vsdx (dibujo de Visio)
    
- .vsdm (dibujo de Visio habilitado para macros)
    
- .vssx (galería de símbolos de Visio)
    
- .vssm (galería de símbolos de Visio habilitada para macros)
    
- .vstx (plantilla de Visio)
    
- .vstm (plantilla de Visio habilitada para macros)
    
> [!NOTE]
> Solo los archivos habilitados con macros (.vsdm, .vssm, .vstm) pueden almacenar macros de VBA. No es posible almacenar macros en archivos con la extensión .vsdx, .vssx ni .vstx. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>¿Qué es el formato de archivo de Visio 2013 "enfoque técnico"?
<a name="vis15_IntroVSDX_What"> </a>

El formato de archivo de Visio 2013 usa Open albarán Conventions (OPC), que define un medio estructurado para almacenar datos de la aplicación con los recursos relacionados con un contenedor de algunos sort─for ejemplo, un archivo ZIP. En un nivel básico, un archivo de Visio 2013 es en realidad un contenedor ZIP que contiene otros tipos de archivos. De hecho, puede guardar un dibujo de Visio 2013 como un archivo .vsdx, cambie el nombre de la extensión de archivo a "\*.zip" en el Explorador de Windows y, a continuación, abra el archivo como una carpeta para ver el contenido dentro de.
  
> [!NOTE]
>  Este artículo contiene sólo una breve introducción a las convenciones de empaquetado abierto. Puede encontrar más detallada de la cobertura de las convenciones de otros artículos: > para obtener más información acerca de las convenciones de empaquetado abierto a sí mismos, vea [OPC: nuevo estándar para empaquetar sus datos](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > Para obtener más información acerca de las convenciones de empaquetado abierto y su uso en archivos de Microsoft Office, vea [aspectos básicos de las convenciones de empaquetado abierto](http://msdn.microsoft.com/en-us/library/ee361919.aspx) y [presentación de los formatos de archivo XML abiertos de Office (2007)](http://msdn.microsoft.com/en-us/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Paquetes y elementos del paquete

Tal y como se ha iniciado anteriormente, los archivos de Visio 2013 son contenedores ZIP o "paquetes" que contienen otros archivos (denominados "las partes del paquete") dentro de ellos. Una parte del paquete puede ser un archivo XML, una imagen, incluso en una solución de VBA. Los elementos dentro del paquete pueden se dividen en dos categorías amplias, "partes del documento" y "elementos de relación". Los elementos de documento contienen el contenido real y los metadatos del archivo de Visio, al igual que el nombre del archivo, la primera página y todas las formas que contiene, e incluso las conexiones de datos de las formas. Imágenes y archivos de texto dentro del paquete se consideran partes del documento. Elementos de relación se describen con más detalle más adelante en este artículo.
  
> [!NOTE]
> Si abre un archivo de Visio 2013 mediante una utilidad ZIP, probablemente puede ver varias carpetas que se encuentren dentro del paquete ZIP. Incluso puede manipular estas direcciones subcaracterística al igual que las carpetas mediante una utilidad ZIP. Sin embargo, estas "carpetas" representan direcciones subcaracterística dentro del paquete ZIP, las carpetas no reales. No se puede usar los equivalentes de las carpetas mediante programación para trabajar con estas direcciones subcaracterística en su solución. 
  
Los elementos de paquete, tanto los de documento como los de relación, también tienen tipos de contenido asociado. Estos tipos de contenido son cadenas que definen un tipo de medio MIME. Estos tipos de contenido especifican y establecen el alcance de la clase de tipos MIME que se pueden obtener en el archivo.
  
### <a name="relationships"></a>Relaciones

Los elementos de relación (que terminan con la extensión "\*.rels" y se almacenan en una carpeta "_rels") se describe cómo se relacionan entre sí los elementos dentro del paquete y proporcionan la estructura del archivo. Un documento XML independiente, utiliza la relación de primarios y secundarios de elementos para determinar la relación de entidades a los otros. Otros archivos pueden utilizar otras jerarquías o la estructura de carpetas de archivo para describir la interacción de contenido en el archivo. Para el formato de archivo de Visio 2013, el paquete es un archivo de Visio válido si contiene el conjunto correcto de elementos y el paquete contiene las relaciones entre los elementos. 
  
Los elementos de relación son documentos XML que describen las relaciones entre los distintos elementos de documento de un paquete. Definen la asociación entre dos elementos: un origen especificado (definido por el nombre y la ubicación del archivo de relación) y un elemento de documento de destino especificado. Por ejemplo, los elementos de relación se usan para describir los maestros de forma que están asociados con el archivo, el modo en que las páginas se relacionan con el archivo y entre sí o el modo en que las imágenes y los objetos se relacionan con una página concreta. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Similitudes y diferencias con el esquema VDX de Visio

Como se ha mencionado, las versiones anteriores de Visio también incluyen un archivo basado en XML de formato, el formato de dibujo XML de Visio o .vdx. (En versiones anteriores de Visio, el esquema usado para el formato de dibujo XML de Visio se denomina DatadiagramML). Algunas partes del esquema XML de Visio hayan permanecido el mismo entre los dos formatos de archivo. Por ejemplo, el elemento de **Windows** y sus elementos secundarios permanecen unchanged─with la excepción de que el elemento de **Windows** ahora es un elemento raíz de un documento XML (window.xml). 
  
La diferencia entre el formato de dibujo XML y el formato de archivo de Visio 2013 más grande es el empaquetado. Un archivo con formato de dibujo XML se puede manipular como un XML independiente normal; el formato de archivo de Visio 2013 debe tratarse como un paquete. En Visio 2013, el código XML se ha dividido copia de seguridad en partes para su consumo sea más fácil. Otro cambio notable es que el formato de archivo de Visio 2013 almacena todas las propiedades de documento en elementos de documento descritos por la norma OPC (app.xml, core.xml, personalizado.XML).
  
Sin embargo, hay un cambio importante que todos los desarrolladores de Visio deben tener en cuenta: la introducción de los elementos de **sección** , **fila**y **celda**. En el esquema de formato de archivo de dibujo XML, filas y celdas de la hoja ShapeSheet individuales se representan mediante elementos con nombre. Por ejemplo, imagine que tiene un documento con una sola página que contiene una forma con un valor de **PinX** de "2" (lo que significa que el eje de giro de la forma es de 2 pulgadas desde el borde izquierdo del dibujo). El marcado relevante para que la configuración en el formato de archivo de dibujo XML se muestra en el siguiente código. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

En este caso, el elemento de **PinX** es un elemento secundario del elemento **XForm** , que a su vez es un elemento secundario del elemento de la **forma** . Este modelo de la interfaz de usuario de la ShapeSheet de Visio, donde la celda **PinX** se incluye en la sección **Transformación de forma** de una forma. 
  
En el formato de archivo de Visio 2013, todas las celdas de la ShapeSheet─ **PinX**, **LinePattern**, una celda de **X** en una fila **MoveTo** de una sección **Geometry** , etc.─are representado por un tipo de elemento XML, el elemento de **celda** . Los distintos elementos de **celda** se individuated entre sí por el valor de su atributo **N** . Por lo tanto, en el ejemplo anterior, los datos contenidos en la celda **PinX** de la hoja ShapeSheet se almacenan en un archivo VSDX tal como se muestra en el siguiente código. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

El elemento de **celda** para **PinX** (así como otras celdas individuales, que se denomina denominadas "singleton celdas" como **LinePattern** o **LockSelect**) es un elemento secundario directo del elemento de **forma** . Ningún elemento único se necesita para representar la fila que contiene la celda **PinX** , tal y como cada forma sólo puede tener una **PinX**.
  
¿Qué información acerca de las secciones que incluyen datos tabulares, al igual que las secciones de **geometría** ? Para las celdas de esas secciones, el esquema de formato de archivo de Visio 2013 usa **sección** y **fila** elements─also distintivo por su atributo **N** o **T** como se muestra below─to contienen los datos. Por ejemplo, la misma forma del ejemplo anterior podría contener datos en la sección de **geometría 1** que es similar al siguiente código en el esquema de dibujo XML. 
  
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

Sin embargo, tenga un aspecto similar al siguiente código en el archivo de Visio 2013.
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Escenarios de desarrollador para trabajar con el formato de archivo de Visio 2013
<a name="vis15_IntroVSDX_Scenarios"> </a>

Como se explicó anteriormente, el formato de archivo de Visio 2013 aprovecha varias tecnologías bien conocidas como archivos ZIP y XML para almacenar datos. Para manipular un dibujo en el nivel de archivo de Visio 2013, una solución sólo tiene que usar los espacios de nombres de .NET Framework y las clases asociadas a trabajar con archivos ZIP o XML, como [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) o [System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx).
  
La ventaja clave para los programadores del formato de archivo de Visio 2013 es que puedan leer y escribir en los archivos de Visio 2013 sin automatización de la aplicación de cliente de Visio. Algunos escenarios que pueden considerar como un desarrollador para trabajar con formato de archivo de Visio 2013 incluyen:
  
- Comprobación de los archivos de Visio 2013 individuales para los datos específicos. Forma selectiva puede leer un elemento fuera del contenedor ZIP sin tener que extraer todo el archivo.
    
- Actualización de las bibliotecas de Visio 2013 archivos con contenido específico. Puede cambiar mediante programación el logotipo en todas las páginas de fondo para reflejar las nuevas instrucciones de personalización de marca.
    
- Creación de aplicaciones que consumen los archivos de Visio 2013. Por ejemplo, puede crear una herramienta que lee un diagrama de flujo de trabajo de Visio y, a continuación, ejecuta su propia lógica de negocios en función de ese flujo de trabajo.
    
Tenga en cuenta que dado que estas soluciones usan ensamblados .NET Framework estándar, la mayoría de las soluciones que se pueden ejecutar en un equipo cliente también se pueden ejecutar en un servidor.
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Exploración mediante programación del formato de archivo de Visio 2013
<a name="vis15_IntroVSDX_Explore"> </a>

La tarea más básica y fundamental para cualquier desarrollador que trabaja con el formato de archivo de Visio 2013 es abrir el archivo como un paquete y, a continuación, obtener acceso a elementos individuales dentro del paquete. El **System.IO.Packaging.Package** en el WindowsBase.dll contiene muchas clases que permiten abrir y manipular paquetes y elementos. 
  
En el código de ejemplo siguiente, se puede ver cómo abrir un archivo .vsdx, leer la lista de elementos del paquete y obtener información sobre cada elemento.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Procedimiento para abrir un archivo .vsdx y ver los elementos de documento

1. Abra Visio 2013 y cree un nuevo documento.
    
2. Cree un documento nuevo y guárdelo en el escritorio.
    
3. Abra Visual Studio 2012.
    
4. En el menú **archivo** , elija **nuevo**y, a continuación, elija ** Project **.
    
5. En **Visual C#** o **Visual Basic**, expanda **Windows** y seleccione **aplicación de consola**.
    
6. En el cuadro **nombre** , escriba 'VisioFileExplorer'. Se abre el proyecto de aplicación de consola. 
    
7. En el **Explorador de soluciones**, haga clic con el botón secundario del mouse en **VisioFileExplorer** y haga clic en **Agregar referencia**. 
    
8. En el cuadro de diálogo **Agregar referencia**, **Ensamblados**, expanda **Framework** y seleccione **WindowsBase**.
    
9. Pegue el código siguiente en la solución.
    
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

10. Presione F5 para depurar la solución. Cuando el programa haya completado su ejecución, presione cualquier tecla para salir.
    
## <a name="see-also"></a>Vea también
<a name="vis15_IntroVSDX_Resources"> </a>

Para obtener más información sobre el formato de archivo de Visio 2013, las convenciones de empaquetado abierto o cómo trabajar con archivos de Visio 2013or Office OpenXML mediante programación, vea los siguientes recursos:
  
- [Visio para desarrolladores](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [OPC: nuevo estándar para empaquetar sus datos](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).
    
- [Aspectos básicos de las convenciones de empaquetado abierto](http://msdn.microsoft.com/en-us/library/ee361919.aspx)
    
- [Introducción a los formatos de archivo de Office (2007) Open XML](http://msdn.microsoft.com/en-us/library/aa338205.aspx)
    

