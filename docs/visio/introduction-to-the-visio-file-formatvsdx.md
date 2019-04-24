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
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Introducción al formato de archivo de Visio (.vsdx)

Obtenga información sobre el nuevo formato de archivo en Visio 2013, explore algunos conceptos de alto nivel para trabajar con el formato de archivo Visio 2013 mediante programación y cree una aplicación de consola sencilla que examina un archivo Visio 2013.
  
|||
|:-----|:-----|
|**En este artículo**         [Introducción](#vis15_IntroVSDX_Intro)          [¿Qué hay detrás del formato de archivo de Visio 2013?](#vis15_IntroVSDX_What)          [Escenarios para desarrolladores para trabajar con el formato de archivo de Visio 2013](#vis15_IntroVSDX_Scenarios)[Explorar el formato de archivo de Visio 2013 mediante programación](#vis15_IntroVSDX_Explore)[Recursos adicionales](#vis15_IntroVSDX_Resources)||
   
## <a name="introduction"></a>Introducción
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 presenta un nuevo formato de archivo (.vsdx) de Visio que reemplaza el formato de archivo binario de Visio (.vsd) y el formato de archivo de dibujo de Visio XML (.vdx). Dado que el formato de archivo de Visio 2013 se basa en convenciones de empaquetado abierto y XML, los desarrolladores familiarizados con estas tecnologías pueden aprender rápidamente a trabajar con archivos de Visio 2013 mediante programación. Los desarrolladores familiarizados con el formato de archivo de dibujo de Visio XML (.vdx) de versiones anteriores de Visio encontrarán muchas de las mismas estructuras de XML en los elementos del formato de archivo .vsdx. La interoperabilidad con archivos de Visio aumenta enormemente gracias a que el software de terceros puede manipular archivos de Visio a nivel de formato de archivo. El formato de archivo de Visio 2013 es compatible con los servicios de Visio en Microsoft SharePoint Server 2013, sin necesidad de un formato de archivo "intermediario" para publicar en SharePoint Server.
  
Existen varios tipos de archivo, por extensión, que componen el formato de archivo de Visio 2013. Estas extensiones incluyen:
  
- .vsdx (dibujo de Visio)
    
- .vsdm (dibujo habilitado para macros de Visio)
    
- .vssx (galería de símbolos de Visio)
    
- .vssm (galería de símbolos habilitada para macros de Visio)
    
- .vstx (plantilla de Visio)
    
- .vstm (plantilla habilitada para macros de Visio)
    
> [!NOTE]
> Solo los archivos habilitados con macros (.vsdm, .vssm, .vstm) pueden almacenar macros de VBA. No es posible almacenar macros en archivos con la extensión .vsdx, .vssx ni .vstx. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>¿Qué hay detrás del formato de archivo de Visio 2013?
<a name="vis15_IntroVSDX_What"> </a>

El formato de archivo de Visio 2013 usa convenciones de empaquetado abierto (OPC), que definen una manera estructurada de almacenar los datos de la aplicación junto con los recursos relacionados mediante un contenedor de algún tipo; por ejemplo, un archivo ZIP. En un nivel básico, un archivo de Visio 2013 es, en realidad, un contenedor ZIP que contiene otros tipos de archivos. De hecho, puede guardar un dibujo de Visio 2013 como un archivo .vsdx, cambiar la extensión del archivo a "\*.zip" en el Explorador de Windows y, a continuación, abrir el archivo como una carpeta para ver el contenido.
  
> [!NOTE]
>  Este artículo contiene una breve introducción a las convenciones de empaquetado abierto. Para obtener información más detallada sobre estas convenciones en otros artículos: >  Para más información sobre las convenciones de empaquetado abierto en sí, consulte [OPC: Nuevo estándar para empaquetar sus datos](https://msdn.microsoft.com/magazine/cc163372.aspx). >  Para obtener más información sobre las convenciones de empaquetado abierto y su uso en los archivos de Microsoft Office, consulte [Aspectos fundamentales de las convenciones de empaquetado abierto](https://msdn.microsoft.com/library/ee361919.aspx) e  [Introducción a los formato de archivo Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Paquetes y elementos de paquete

Como se mencionó anteriormente, los archivos de Visio 2013 son contenedores ZIP o "paquetes" que contienen otros archivos (denominados "elementos de paquete") dentro de ellos. Un elemento del paquete puede ser un archivo XML, una imagen e, incluso, una solución de VBA. Los elementos de paquete se dividen en dos categorías más generales: "elementos de documento" y "elementos de relación". En los elementos de documento se encuentran el contenido y los metadatos del archivo de Visio; por ejemplo, el nombre del archivo, la primera página y todas las formas que contiene e, incluso, las conexiones de datos para las formas. Las imágenes y los archivos de texto dentro del paquete se consideran elementos de documento. Los elementos de relación se describen con mayor detalle más adelante en este artículo.
  
> [!NOTE]
> Si abre un archivo de Visio 2013 con una herramienta de compresión, probablemente verá varias carpetas dentro del paquete ZIP. Puede, incluso, manipular estas subdirecciones como carpetas con una herramienta de compresión. No obstante, estas "carpetas" representan subdirecciones dentro del paquete ZIP, no carpetas reales. No puede usar los equivalentes de carpetas mediante programación para trabajar con estas subdirecciones en su solución. 
  
Los elementos de paquete, tanto los de documento como los de relación, también tienen tipos de contenido asociado. Estos tipos de contenido son cadenas que definen un tipo de medio MIME. Estos tipos de contenido especifican y establecen el alcance de la clase de tipos MIME que se pueden obtener en el archivo.
  
### <a name="relationships"></a>Relaciones

Los elementos de relación (que terminan con la extensión "\*.rels" y se almacenan en una carpeta "_rels") describen cómo se relacionan entre sí los elementos dentro del paquete y proporcionan la estructura del archivo. Un documento XML independiente usa la relación de elemento primario/secundario de los elementos para determinar la relación de las entidades entre sí. Otros archivos pueden usar otras jerarquías o la estructura de carpetas de archivo para describir la interacción del contenido del archivo. Para el formato de archivo de Visio 2013, el paquete es un archivo de Visio válido si contiene el conjunto adecuado de elementos y el paquete contiene las relaciones entre los elementos. 
  
Los elementos de relación son documentos XML que describen las relaciones entre los distintos elementos de documento de un paquete. Definen la asociación entre dos elementos: un origen especificado (definido por el nombre y la ubicación del archivo de relación) y un elemento de documento de destino especificado. Por ejemplo, los elementos de relación se usan para describir los maestros de forma que están asociados con el archivo, el modo en que las páginas se relacionan con el archivo y entre sí o el modo en que las imágenes y los objetos se relacionan con una página concreta. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Similitudes y diferencias con el esquema VDX de Visio

Como ya se ha mencionado, las versiones anteriores de Visio incluían también un formato de archivo basado en XML, el formato de dibujo de Visio XML o .vdx. (En versiones anteriores de Visio, el esquema que se usa para el formato de dibujo de Visio XML se denomina DatadiagramML). Algunas partes del esquema de Visio XML han permanecido igual entre los dos formatos de archivo. Por ejemplo, el elemento **Windows** y sus elementos secundarios no sufren modificaciones, con la excepción que el elemento **Windows** pasa a ser un elemento de raíz de un documento XML (window.xml). 
  
La diferencia más notable entre el formato de dibujo XML y el formato de archivo de Visio 2013 es el empaquetado. Un archivo de formato de dibujo XML podría tratarse como un XML normal independiente; el formato de archivo de Visio 2013 debe tratarse como un paquete. En Visio 2013, se ha dividido el XML en secciones para facilitar su consumo. Otro cambio notable es que el formato de archivo de Visio 2013 almacena todas las propiedades del documento en elementos del documento que se describe en la norma OPC (app.xml, core.xml personalizado.XML).
  
No obstante, hay un cambio importante que todos los desarrolladores de Visio deben tener en cuenta: la introducción de los elementos **Cell** (celda), **Row** (fila) y **Section** (sección). En el esquema de formato de archivo de dibujo XML, las filas y celdas individuales de ShapeSheet se representan mediante elementos con nombre. Por ejemplo, imagine que tiene un documento de una sola página que contiene una forma con un valor **PinX** de "2" (lo que significa que el eje de giro de la forma es de 2 pulgadas (5 cm) desde el borde izquierdo del dibujo). En el siguiente código se muestra el marcado relevante para la configuración del formato de archivo de dibujo XML. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Aquí, el elemento **PinX** es un elemento secundario del elemento **XForm**, que es, a su vez, un elemento secundario del elemento **Shape** (forma). Este da forma a la interfaz de usuario de Visio ShapeSheet, donde la celda **PinX** se incluye en la sección **Transformación de forma** de una forma. 
  
En el formato de archivo de Visio 2013, todas las celdas de ShapeSheet - **PinX**, **LinePattern**, una celda **X** en una fila **MoveTo** en una sección **Geometría**, etc. - están representadas por un tipo de elemento XML: el elemento **Cell**. Los diferentes elementos **Cell** se distinguen entre sí por el valor de su atributo **N**. Por lo tanto, en el ejemplo anterior, los datos contenidos en la celda **PinX** en ShapeSheet se almacenan en un archivo VSDX, como se muestra en el siguiente código. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

El elemento **Cell** para **PinX** (así como otras celdas individuales con nombre, denominadas "celdas singleton", como **LinePattern** o **LockSelect**) es un elemento secundario directo del elemento **Shape**. No es necesario ningún elemento único para representar la fila que contiene la celda **PinX**, ya que cada forma solo puede tener una **PinX**.
  
¿Qué sucede con las secciones que incluyen datos tabulares, como las secciones**Geometría**? Para las celdas de esas secciones, el esquema de formato de archivo de Visio 2013 usa elementos **Section** y **Row**, también diferenciados por su atributo **N** o **T ** tal como se muestra debajo, para contener los datos. Por ejemplo, la misma forma del ejemplo anterior puede contener datos en la sección **Geometría 1** que son similares al siguiente código en el esquema de dibujo XML. 
  
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

Sin embargo, se parece al siguiente código del archivo de Visio 2013.
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Escenarios para desarrolladores para trabajar con el formato de archivo de Visio 2013
<a name="vis15_IntroVSDX_Scenarios"> </a>

Como se ha explicado anteriormente, el formato de archivo de Visio 2013 aprovecha varias tecnologías bien comprendidas, como archivos ZIP y XML, para almacenar datos. Para manipular un dibujo de Visio 2013 al nivel de archivo, una solución solo necesita usar las clases y los espacios de nombres de .NET Framework que se asocian al trabajo con archivos ZIP o XML, como [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) o [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).
  
La mayor ventaja para los desarrolladores de los formatos de archivo de Visio 2013 es que se puede leer y escribir en archivos de Visio 2013 sin automatizar la aplicación de cliente de Visio. Estos son algunos de los escenarios que puede considerar como desarrollador para trabajar con el formato de archivo de Visio 2013:
  
- Comprobación de archivos individuales de Visio 2013 en busca de datos específicos. Puede leer un elemento del contenedor ZIP de manera selectiva sin tener que extraer todo el archivo.
    
- Actualización de las bibliotecas de los archivos de Visio 2013 con contenido específico. Puede cambiar el logotipo en todas las páginas de fondo mediante programación para reflejar nuevas pautas de marca.
    
- Creación de aplicaciones que utilizan los archivos de Visio 2013. Por ejemplo, puede crear una herramienta que lea un diagrama de flujo de trabajo de Visio y luego ejecute su propia lógica empresarial basándose en ese flujo de trabajo.
    
Tenga en cuenta que dado que estas soluciones usan ensamblados .NET Framework estándar, la mayoría de las soluciones que se pueden ejecutar en un equipo cliente también se pueden ejecutar en un servidor.
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Manipulación del formato de archivo de Visio 2013 mediante programación
<a name="vis15_IntroVSDX_Explore"> </a>

La tarea más básica y fundamental para los programadores que trabajan con el formato de archivo de Visio 2013 es abrir el archivo como un paquete y, a continuación, acceder a los elementos individuales dentro del paquete. El **System.IO.Packaging.Package** en la WindowsBase.dll contiene muchas clases que le permiten abrir y manipular paquetes y elementos. 
  
En el código de ejemplo siguiente, se puede ver cómo abrir un archivo .vsdx, leer la lista de elementos de paquete y obtener información sobre cada elemento.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Para abrir un archivo .vsdx y ver los elementos de documento

1. Abra Visio 2013 y cree un documento nuevo.
    
2. Cree un nuevo documento y guárdelo en el escritorio.
    
3. Abra Visual Studio 2012.
    
4. En el menú **Archivo**, elija **Nuevo** y, luego, ** Proyecto **.
    
5. En **Visual C# ** o **Visual Basic**, expanda **Windows**y seleccione **Aplicación de consola**.
    
6. En el cuadro **Nombre**, escriba 'VisioFileExplorer'. Se abre la aplicación de consola. 
    
7. En el **Explorador de soluciones**, haga clic con el botón derecho en **VisioFileExplorer**y, a continuación, en **Agregar referencia**. 
    
8. En el cuadro de diálogo **Agregar referencia**, en **Ensamblados**, expanda **Framework**y luego elija **WindowsBase**.
    
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

Para obtener más información sobre el formato de archivo de Visio 2013, las convenciones de empaquetado abierto o cómo trabajar con archivos de Visio 2013 u Office OpenXML mediante programación, consulte los recursos siguientes:
  
- [Visio para desarrolladores](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: Nuevo estándar para empaquetar sus datos](https://msdn.microsoft.com/magazine/cc163372.aspx)
    
- [Aspectos fundamentales de las convenciones de empaquetado abierto](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Introducción a los formato de archivo Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx)
    

