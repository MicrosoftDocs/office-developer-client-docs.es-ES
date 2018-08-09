---
title: Nuevo en Visio para desarrolladores
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: Este documento proporciona una vista de nivel superior de las mejoras e incorporaciones para desarrolladores de Visio 2013. Para los desarrolladores que están listos para empezar a un salto de la plataforma de Visio, le proporciona detalles suficientes para empezar a codificar en Visio 2013.
ms.openlocfilehash: 3e0f119ac0b6b43737ff394a4553405982a4ec04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822682"
---
# <a name="new-in-visio-for-developers"></a>Nuevo en Visio para desarrolladores

Este documento proporciona una vista de nivel superior de las mejoras e incorporaciones para desarrolladores de Visio 2013. Para los desarrolladores que están listos para empezar a un salto de la plataforma de Visio, le proporciona detalles suficientes para empezar a codificar en Visio 2013.
  
## <a name="introduction"></a>Introducción
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 proporciona una potente plataforma única para las soluciones personalizadas de dibujo. Nuevos objetos, colecciones, propiedades, métodos, enumeraciones y eventos, junto con nuevas funciones y las celdas de ShapeSheet proporcionan más opciones para definir el comportamiento de los elementos en sus soluciones.
  
Entre las nuevas características de interés para los desarrolladores en Visio 2013 son el nuevo formato de archivo; actualizaciones sólidas para temas; cambiar la función de forma (lo que permite reemplazar las formas con otra); efectos de forma nuevos; mejoras realizadas a comentarios; co-autoría en SharePoint Server 2013; recorte de imágenes personalizable; geometría relativa; compatibilidad con datos de servicios de conectividad empresarial (BCS); actualizaciones de los servicios de Visio en Microsoft SharePoint Server 2013; y una característica de página duplicada. En este tema se proporciona un resumen breve de cada una de estas características y se menciona algunos de los nuevos objetos de Visio y miembros que están asociados con las características y exponen en Visual Basic para aplicaciones (VBA). Para obtener información acerca de estas características y ejemplos de código que lo acompaña, consulte el [Centro de desarrolladores de Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx).
  
> [!NOTE]
> Visio 2013 incluye muchas nuevas ShapeSheet celdas, filas y funciones para admitir las nuevas características de Visio. Para obtener más información acerca de novedades de la ShapeSheet de Visio 2013, vea el artículo [Novedades para programadores de Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md). 
  
## <a name="new-file-format"></a>Nuevo formato de archivo
<a name="vis15_WhatsNew_NewFF"> </a>

Visio 2013 presenta un nuevo formato de archivo basado en el estándar de convenciones de empaquetado abierto (Open Packaging Conventions u OPC, ISO 29500 parte 2) y los elementos de XML del anterior formato de archivo de Visio XML (.vdx). Es un formato de archivo zip, basado en XML similar a los formatos de archivo usados en otras aplicaciones.
  
Debido a que el nuevo formato de archivo es compatible con Visio 2013 y servicios de Visio en Microsoft SharePoint Server 2013, puede guardar un dibujo de Visio directamente a una biblioteca de SharePoint Server, sin tener que volver a publicar el archivo como un dibujo de Web de Visio (.vdw). Aun así, los servicios de Visio puede leer y mostrar los archivos de dibujo Web de Visio.
  
El nuevo formato de archivo incluye los siguientes tipos de archivo (por extensión):
  
- .vsdx (dibujo de Visio)
    
- .vsdm (dibujo de Visio habilitado para macros)
    
- .vssx (galería de símbolos de Visio)
    
- .vssm (galería de símbolos de Visio habilitada para macros)
    
- .vstx (plantilla de Visio)
    
- .vstm (plantilla de Visio habilitada para macros)
    
Mediante el uso de soporte existente para leer y escribir en el paquete de formatos de archivo (por ejemplo, [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) ) y el análisis XML ( [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ), puede trabajar mediante programación con los nuevos formatos de archivo. 
  
Visio 2013 conserva la capacidad de leer los formatos de archivo anterior (.vsd, .vss, .vst, .vdx, .vsx, .vtx, VDW, .vwi). Visio 2013 no se guarda en el formato de archivo XML de Visio (.vdx) anterior. Soluciones o herramientas que consumen los archivos de formato (.vdx) de archivo XML de Visio anteriores que tenga que se va a refactorizar con el fin de leer el nuevo formato de archivo y sus esquemas.
  
Servicios de Visio conserva la capacidad de mostrar el formato de los dibujos web de Visio (.vdw) en el explorador. Ahora también representa los nuevos formatos de dibujo de Visio (.vsdx) y de dibujo habilitado para macros de Visio (.vsdm).
  
## <a name="themes"></a>Temas
<a name="vis15_WhatsNew_Themes"> </a>

Los temas se han rediseñado en Visio 2013 a fin de aprovechar mejor la gran variedad de efectos y estilos, incluyendo la integración de efectos de Shape Art. Los usuarios ahora pueden decidir en un estilo general aplicando un tema, personalizar el diagrama con variaciones de temas y resaltar las formas individuales con estilos rápidos. Los desarrolladores de ShapeSheet pueden aprovechar las ventajas de estas características con nuevas funciones y las celdas de ShapeSheet.
  
También puede manipular temas en el nivel de los objetos [Page](http://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx), [Shape](http://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) y [Selection](http://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx). Las nuevas API para trabajar con temas incluyen los métodos [Page.SetTheme](http://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx), [Page.SetThemeVariant](http://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx), [Shape.SetQuickStyle](http://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) y [Selection.SetQuickStyle](http://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx). 
  
Para obtener una lista detallada de las nuevas API en Visio 2013, vea la sección de [cambios del modelo de objetos de Visio](#vis15_WhatsNew_NewOM) en este artículo. Para obtener más información acerca de las nuevas celdas de ShapeSheet en Visio 2013, vea el artículo [Novedades para programadores de Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="change-shape"></a>Cambio de forma
<a name="vis15_WhatsNew_ChangeShapes"> </a>

Visio 2013 incluye un reemplazo de forma API que le permite intercambiar una o varias formas para otra forma contenida en una galería de símbolos, conservando algunos de los valores de la forma original, al igual que la forma de texto de forma, datos de formas o formato de forma locales. Los programadores de forma pueden actualizar la configuración de ShapeSheet de sus formas personalizadas para especificar el comportamiento de la forma de cambiar de sus formas. Entre las nuevas API son los métodos [Shape.ReplaceShapes](http://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) y [Selection.ReplaceShapes](http://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) y el evento [ReplaceShape](http://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) . 
  
Para obtener una lista detallada de las nuevas API en Visio 2013, vea la sección de [cambios del modelo de objetos de Visio](#vis15_WhatsNew_NewOM) en este artículo. Para obtener más información acerca de las nuevas celdas de ShapeSheet en Visio 2013, vea el artículo [Novedades para programadores de Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="shape-effects"></a>Efectos de formas
<a name="vis15_WhatsNew_ShapeEffects"> </a>

Se han agregado a Visio 2013 nuevos efectos de forma como los de bisel, giro 3D, iluminado, reflejo y esbozo. La ShapeSheet incluye nuevas celdas para trabajar con estos efectos.
  
Para obtener más información acerca de las nuevas celdas de ShapeSheet en Visio 2013, vea el artículo [Novedades para programadores de Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="commenting"></a>Comentarios
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 incluye un nuevo marco para comentarios. Ahora pueden asociarse comentarios con una forma o página particular. Visio 2013 incluye dos nuevos objetos, [comentarios](http://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) y [comentario](http://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx). Nuevas API para obtener acceso mediante programación a comentarios incluyen las propiedades [Document.Comments](http://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx), [Page.Comments](http://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx), [Shape.Comments](http://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx)y [Page.ShapeComments](http://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) . 
  
Servicios de Visio incluye JavaScript APIs para leer los comentarios de una página o una forma en un diagrama.
  
Para obtener una lista detallada de las nuevas API en Visio 2013, vea la sección de [cambios del modelo de objetos de Visio](#vis15_WhatsNew_NewOM) en este artículo. 
  
> [!NOTE]
> Ya no se puede obtener acceso a los comentarios a través de la ShapeSheet. 
  
## <a name="coauthoring"></a>Co-autoría
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 incluye la capacidad de diagramas de coautor almacenados en SharePoint o Microsoft OneDrive. Los desarrolladores tienen acceso al evento [Document.AfterDocumentMerge](http://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) que proporciona información acerca de los cambios del diagrama debido a la co-autoría. Los programadores de soluciones también tienen la capacidad para deshabilitar la co-autoría para adaptarse a sus necesidades personalizados mediante la celda [NoCoauth](nocoauth-cell-document-properties-section.md) en la ShapeSheet del documento. 
  
Para obtener una lista detallada de las nuevas API en Visio 2013, vea la sección de [cambios del modelo de objetos de Visio](#vis15_WhatsNew_NewOM) en este artículo. 
  
## <a name="customizable-image-clipping"></a>Recorte de imágenes personalizable
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 admite la definición de una ruta de recorte de imágenes personalizable para recortar las imágenes a cualquier forma. Esto amplía las capacidades de Visio 2010, que admite imágenes de recorte en una forma rectangular. Esta funcionalidad está disponible en la hoja ShapeSheet mediante el uso de la celda [ClippingPath](clippingpath-cell-foreign-image-info-section.md) en la sección **Foreign Image Info** . 
  
Para obtener más información acerca de las nuevas celdas de ShapeSheet en Visio 2013, vea el artículo [Novedades para programadores de Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="relative-geometries"></a>Geometrías relativas
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

En las versiones anteriores de Visio, geometría de forma definida por las fórmulas que dependían el alto o el ancho de la forma. Por ejemplo, en Visio 2010 se han definido los vértices de muchas formas de Visio integradas multiplicando el alto o el ancho de la forma por una constante. Estas formas tenían las secciones de **geometría** que incluyen filas [MoveTo](moveto-row-geometry-section.md) o [LineTo](lineto-row-geometry-section.md) (por ejemplo) con fórmulas como `Width*1` y `Height*0`.
  
Visio 2013 pasa a admitir geometrías relativas en la ShapeSheet. Los programadores de forma ahora pueden usar geometrías relativas para especificar geometrías como valores simples o las fórmulas, que multiplican por el alto o el ancho automáticamente. Vértices de forma ahora se pueden expresar con constantes, por ejemplo, eliminando la necesidad de express vértices como múltiplos del ancho de la forma o el alto. Esto facilita a los desarrolladores crear formas, con un mejor rendimiento y tamaños de archivo más pequeños. Las nuevas filas incluyen las filas [RelMoveTo](relmoveto-row-geometry-section.md) y [RelLineTo](rellineto-row-geometry-section.md) , donde los valores de celda **X** e **Y** se multiplican automáticamente por el ancho o el alto de la forma (respectivamente). 
  
Para obtener más información acerca de las nuevas filas de ShapeSheet de Visio 2013, vea el artículo [Novedades para programadores de Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Compatibilidad con los datos de Servicios de conectividad empresarial (BCS)
<a name="vis15_WhatsNew_BCS"> </a>

Diagramas de Visio 2013 ahora pueden conectarse a listas externas en servidores de SharePoint Server 2013. Una lista externa es un origen de contenido externo a SharePoint (por ejemplo, una tabla de SQL Server) que se ha conectado a una lista de SharePoint mediante el uso de servicios de conectividad empresarial (BCS) de Microsoft. Servicios de Visio admite la capacidad de actualizar los diagramas de Visio como las actualizaciones de datos.
  
Para obtener más información acerca de novedades de servicios de Visio, vea el artículo [Servicios de Visio en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx). Para obtener más información acerca de los servicios de conectividad empresarial (BCS), vea [Business Connectivity Services in SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163782%28office.15%29.aspx).
  
## <a name="improvements-in-visio-services"></a>Mejoras en los servicios de Visio
<a name="vis15_WhatsNew_VisioServices"> </a>

Servicios de Visio en Microsoft SharePoint Server 2013 incluye muchas mejoras. Como se mencionó anteriormente, los servicios de Visio es compatible con el nuevo formato de archivo de Visio (.vsdx y .vsdm). Servicios de Visio se ha ampliado la actualización de datos y los nuevos cálculos, incluida la posibilidad de volver a calcular las fórmulas a través de un diagrama completo. 
  
Para obtener más información acerca de novedades de servicios de Visio, vea el artículo [Servicios de Visio en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx).
  
## <a name="duplicate-page"></a>Página duplicada
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Ahora puede copiar una página y todas sus formas dentro del mismo documento en Visio 2013. Por lo tanto, el objeto **Page** tiene un método nuevo, [Duplicar](http://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx), que duplica la página y devuelve un objeto **Page** nuevo. 
  
## <a name="visio-object-model-changes"></a>Cambios del modelo de objetos de Visio
<a name="vis15_WhatsNew_NewOM"> </a>

Nuevos objetos, propiedades, métodos y eventos se han agregado al modelo de objetos de Visio para proporcionar compatibilidad con programación de nuevas características de Visio 2013. Además, las mejoras del modelo de objetos tratan las solicitudes de desarrollador frecuentes de los cambios realizados en la plataforma de Visio.
  
### <a name="new-members"></a>Nuevos miembros

Los miembros siguientes se han agregado a los objetos existentes en el modelo de objetos de Visio.
  
 **Tabla 1. Mejoras del modelo de objetos de Visio**
  
|**Objeto o colección**|**Nuevos miembros**|
|:-----|:-----|
|[Objeto de aplicación (Visio)](http://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Evento Application.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Evento Application.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Evento Application.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Evento Application.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[ApplicationSettings (objeto) (Visio)](http://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[Propiedad ApplicationSettings.EnterCommitsText (Visio)](http://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[Propiedad ApplicationSettings.SVGExportFormat (Visio)](http://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Objeto Document (Visio)](http://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Evento Document.AfterDocumentMerge (Visio)](http://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Propiedad Document.Comments (Visio)](http://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Propiedad Document.CompatibilityMode (Visio)](http://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Objeto Documents (Visio)](http://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Evento Documents.AfterDocumentMerge (Visio)](http://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Evento Documents.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Evento Documents.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Evento Documents.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Evento Documents.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[Objeto InvisibleApp (Visio)](http://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[Evento InvisibleApp.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[Evento InvisibleApp.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[Evento InvisibleApp.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[Evento InvisibleApp.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Objeto Page (Visio)](http://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Evento Page.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Evento Page.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Propiedad Page.Comments (Visio)](http://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Método Page.Duplicate (Visio)](http://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Método Page.GetTheme (Visio)](http://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Método Page.GetThemeVariant (Visio)](http://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Evento Page.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Evento Page.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Método Page.SetTheme (Visio)](http://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Método Page.SetThemeVariant (Visio)](http://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Propiedad Page.ShapeComments (Visio)](http://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Objeto Pages (Visio)](http://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Evento Pages.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Evento Pages.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Evento Pages.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Evento Pages.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Objeto Selection (Visio)](http://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Método Selection.ReplaceShape (Visio)](http://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Método Selection.SetQuickStyle (Visio)](http://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Objeto Shape (Visio)](http://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Método Shape.ChangePicture (Visio)](http://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Propiedad Shape.Comments (Visio)](http://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Método Shape.ReplaceShape (Visio)](http://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Método Shape.SetQuickStyle (Visio)](http://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>Nuevos objetos y enumeraciones

Los objetos siguientes se han agregado al modelo de objetos de Visio.
  
 **Tabla 2. Adiciones al modelo de objetos de Visio**
  
|**Object**|**Properties**|**Métodos**|
|:-----|:-----|:-----|
|[Objeto CoauthMergeEvent (Visio)](http://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[Propiedad CoauthMergeEvent.BaseDocument (Visio)](http://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [Propiedad CoauthMergeEvent.DownloadDocument (Visio)](http://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [Propiedad CoauthMergeEvent.ObjectType (Visio)](http://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [Propiedad CoauthMergeEvent.Stat (Visio)](http://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [Propiedad CoauthMergeEvent.WorkingDocument (Visio)](http://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |Ninguno  <br/> |
|[Objeto Comment (Visio)](http://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Propiedad Comment.AssociatedObject (Visio)](http://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Propiedad Comment.AuthorInitials (Visio)](http://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Propiedad Comment.AuthorName (Visio)](http://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Propiedad Comment.AuthorSipAddress (Visio)](http://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Propiedad Comment.AuthorSMTPAddress (Visio)](http://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Propiedad Comment.Collapsed (Visio)](http://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Propiedad Comment.CreateDate (Visio)](http://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Propiedad Comment.Document (Visio)](http://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Propiedad Comment.EditDate (Visio)](http://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Propiedad Comment.ObjectType (Visio)](http://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Propiedad Comment.Stat (Visio)](http://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Propiedad Comment.Text (Visio)](http://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Método Comment.Delete (Visio)](http://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Comments (objeto) (Visio)](http://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Propiedad Comments.Count (Visio)](http://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Propiedad Comments.Document (Visio)](http://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Propiedad Comments.Item (Visio)](http://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Propiedad Comments.ObjectType (Visio)](http://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Propiedad Comments.Stat (Visio)](http://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Método Comments.Add (Visio)](http://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Método Comments.DeleteAll (Visio)](http://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[Objeto ReplaceShapesEvent (Visio)](http://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[Propiedad ReplaceShapesEvent.ObjectType (Visio)](http://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [Propiedad ReplaceShapesEvent.ReplaceFlags (Visio)](http://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [Propiedad ReplaceShapesEvent.ReplacementMaster (Visio)](http://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [Propiedad ReplaceShapesEvent.SelectionSource (Visio)](http://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [Propiedad ReplaceShapesEvent.Stat (Visio)](http://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |Ninguno  <br/> |
   
En la siguiente tabla se enumera las nuevas enumeraciones y constantes que se incluyen en Visio 2013.
  
 **Tabla 3. Adiciones de enumeraciones de Visio**
  
|**Enumeración**|**Descripción**|
|:-----|:-----|
|[VisQuickStyleColors (enumeración) (Visio)](http://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |Especifica nombres designados para los colores contenidos dentro de un tema.  <br/> |
|[VisQuickStyleMatrixIndices (enumeración) (Visio)](http://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |Especifica los nombres designados para los temas y variaciones proporcionadas con Visio 2013.  <br/> |
|[VisReplaceFlags (enumeración) (Visio)](http://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |Especifica los comportamientos de una operación de cambio de forma.  <br/> |
|[VisSVGExportFormat (enumeración) (Visio)](http://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |Especifica la inclusión o exclusión del marcado de Visio al exportar un diagrama a SVG.  <br/> |
   
### <a name="deprecated-objects-and-members"></a>Objetos y miembros desusados

En la siguiente tabla se enumera los objetos en desuso y miembros que se incluyen en Visio 2013. Sólo los miembros que se enumeran en la columna **en desuso a miembros** de objeto en desuso. 
  
 **Tabla 4. Degradaciones del modelo de objetos de Visio**
  
|**Objeto o colección**|**Miembros desusados**|
|:-----|:-----|
|Objeto **Window**  <br/> |**PageTabWidth (** propiedad)  <br/> |
   
## <a name="see-also"></a>Vea también
<a name="vis15_WhatsNew_Additional"> </a>

- [Visio para desarrolladores](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Novedades para programadores de ShapeSheet de Visio](what-s-new-for-visio-shapesheet-developers.md)
    
- [Servicios de Visio en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx)
    
- [¿Qué es una novedad de Visio (Office.com)](http://office.com/redir/HA102749364.aspx)
    
- [Centro para desarrolladores de Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    

