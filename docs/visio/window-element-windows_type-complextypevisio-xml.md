---
title: Elemento de la ventana (Windows_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Representa una ventana abierta en una instancia de Microsoft Visio. Este elemento contiene la información necesaria para exactamente volver a crear una ventana de interfaz de usuario en el área de trabajo de la aplicación cuando inicialmente se abre el archivo de Visio.
ms.openlocfilehash: 762b689d625c7865696a0bf8bb8c4acc25e3d8eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823549"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Elemento de la ventana (Windows_Type complexType) ('XML de Visio')

Representa una ventana abierta en una instancia de Microsoft Visio. Este elemento contiene la información necesaria para exactamente volver a crear una ventana de interfaz de usuario en el área de trabajo de la aplicación cuando inicialmente se abre el archivo de Visio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contiene los elementos de la **ventana** de un documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica si está habilitada la característica de cuadrícula dinámica de un documento o ventana.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos que se pegan las formas cuando el pegado está habilitado en el documento.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Especifica si los puntos de conexión se muestran en una ventana.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Especifica si se muestra una cuadrícula en la ventana de dibujo.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Especifica si se muestran guías en la ventana de dibujo.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Especifica si se muestran los saltos de página en una ventana.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Especifica si se muestran reglas en la ventana de dibujo.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contiene una colección de elementos de **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica si una opción de configuración de extensión del complemento específico está habilitado o deshabilitado para la ventana activa.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos que las formas ajustan ajustar cuando está en la ventana activa.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Especifica el grupo de windows de galería de símbolos combinadas de que la ventana es un miembro.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contiene un número entero que especifica la posición relativa de una galería de símbolos dentro de un grupo en una ventana.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Especifica el ancho del control de ficha de página de una ventana de dibujo (como una fracción del ancho total de la ventana de dibujo).  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de contenedor: página, hoja o patrón. Sólo relevantes y es necesario si se especifica **ContainerType** .  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |opcional  <br/> |Puede ser uno de los siguientes valores: Document, Page o Master. Solo es relevante cuando se especifica **WindowType** como dibujo o la hoja.  <br/> |Valores del tipo xsd:token.  <br/> |
|Documento  <br/> |xsd: String  <br/> |opcional  <br/> |Ruta de acceso de archivo del documento que se muestra en esta ventana.  <br/> |Valores del tipo XSD: String.  <br/> |
|id.  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de patrón si esta ventana muestra a un patrón.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Page  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de la página si la ventana muestra una página. Es relevante sólo cuando se especifica **WindowType** como dibujo y **ContainerType** se especifica como página.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de ventana en la que se encuentra esta ventana de galería de símbolos. Es relevante sólo si se especifica **WindowType** como galería de símbolos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Marca de solo lectura si esta galería de símbolos no es una galería de símbolos de documento.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Hoja  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de hoja en el contenedor. Es relevante sólo si se especifica el contenedor en una hoja.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que se supone una nueva vista (ventana) cuando se abre inicialmente.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ViewCenterY  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que se supone una nueva vista (ventana) cuando se abre inicialmente.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ViewScale  <br/> |xsd: Double  <br/> |opcional  <br/> |El factor de ampliación predeterminado para usar cuando se abre una nueva vista (ventana) de la página. Por ejemplo, 1 = 100%; 1,5 = 150% y así sucesivamente.  <br/> |Valores del tipo XSD: Double.  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Alto del rectángulo de la ventana.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |opcional  <br/> |Coordenada izquierda del rectángulo de la ventana.  <br/> |Valores del tipo xsd:short.  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Un entero que especifica los indicadores de bits.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |opcional  <br/> |Coordenada superior del rectángulo de la ventana.  <br/> |Valores del tipo xsd:short.  <br/> |
|Tipo ventana  <br/> |xsd:token  <br/> |necesario  <br/> |Un valor enumerado que puede ser uno de los siguientes: dibujo, hoja, Galería de símbolos o icono.  <br/> |Valores del tipo xsd:token.  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Ancho del rectángulo de la ventana.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

