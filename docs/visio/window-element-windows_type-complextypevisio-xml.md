---
title: Elemento Window (Windows_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Representa una ventana abierta en una instancia de Microsoft Visio. Este elemento contiene información necesaria para volver a crear exactamente una ventana de interfaz de usuario en el área de trabajo de la aplicación cuando Visio abre inicialmente el archivo.
ms.openlocfilehash: 2700ee7a9a17460f6ac707f5b1a8f35d622e33e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538462"
---
# <a name="window-element-windows_type-complextype-visio-xml"></a>Elemento Window (Windows_Type complexType) (XML de Visio)

Representa una ventana abierta en una instancia de Microsoft Visio. Este elemento contiene información necesaria para volver a crear exactamente una ventana de interfaz de usuario en el área de trabajo de la aplicación cuando Visio abre inicialmente el archivo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contiene los **elementos Window** de un documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica si la característica de cuadrícula dinámica está habilitada para un documento o una ventana.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos a los que se pegan las formas cuando se habilita el pegado en el documento.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Especifica si los puntos de conexión se muestran en una ventana.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Especifica si se muestra una cuadrícula en la ventana de dibujo.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Especifica si se muestran guías en la ventana de dibujo.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Especifica si los saltos de página se muestran en una ventana.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Especifica si las reglas se muestran en la ventana de dibujo.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contiene una colección de **elementos SnapAngle.**  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Especifica el grupo de ventanas de galería de símbolos combinadas de las que la ventana es miembro.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contiene un entero que especifica la posición relativa de una galería de símbolos dentro de un grupo en una ventana.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Especifica el ancho del control de pestaña de página de una ventana de dibujo (como una fracción del ancho total de la ventana de dibujo).  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador del contenedor: Página, Hoja o Patrón. Solo es relevante y necesario si **se especifica ContainerType.**  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |opcional  <br/> |Puede ser uno de los siguientes valores: Documento, Página o Patrón. Sólo es relevante **cuando WindowType** se especifica como Dibujo o Hoja.  <br/> |Valores del tipo xsd:token.  <br/> |
|Documento  <br/> |xsd:string  <br/> |opcional  <br/> |Ruta de acceso del documento que se muestra en esta ventana.  <br/> |Valores del tipo xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de patrón si esta ventana muestra un patrón.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Page  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de página si esta ventana muestra una página. Sólo es relevante **cuando WindowType** se especifica como Drawing y **ContainerType** se especifica como Page.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de ventana en la que se encuentra esta ventana de galería de símbolos. Sólo es relevante **cuando WindowType** se especifica como galería de símbolos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |xsd:boolean  <br/> |opcional  <br/> |Marca de solo lectura si esta galería de símbolos no es una galería de símbolos de documento.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|Sheet  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador de la hoja en el contenedor. Solo es relevante cuando el contenedor se especifica como Hoja.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que una nueva vista (ventana) asume cuando se abre inicialmente.  <br/> |Valores del tipo xsd:double.  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que una nueva vista (ventana) asume cuando se abre inicialmente.  <br/> |Valores del tipo xsd:double.  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |opcional  <br/> |Factor de ampliación predeterminado que se usará cuando se abra una nueva vista (ventana) de la página. Por ejemplo, 1 = 100%; 1,5 = 150 %, y así sucesivamente.  <br/> |Valores del tipo xsd:double.  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Alto del rectángulo de la ventana.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |opcional  <br/> |Coordenada izquierda del rectángulo de ventana.  <br/> |Valores del tipo xsd:short.  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Entero que especifica marcas de bits.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |opcional  <br/> |Coordenada superior del rectángulo de la ventana.  <br/> |Valores del tipo xsd:short.  <br/> |
|WindowType  <br/> |xsd:token  <br/> |necesario  <br/> |Un valor enumerado que puede ser uno de los siguientes: Dibujo, Hoja, Galería de símbolos o Icono.  <br/> |Valores del tipo xsd:token.  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Ancho del rectángulo de la ventana.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

