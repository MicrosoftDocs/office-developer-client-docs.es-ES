---
title: Elemento DocumentSettings (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contiene elementos que especifican la configuración del documento.
ms.openlocfilehash: 0d8e0809afae7b3de059166343577bb58f0eb01b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540073"
---
# <a name="documentsettings-element-visiodocument_type-complextype-visio-xml"></a>Elemento DocumentSettings (VisioDocument_Type complexType) (Visio XML)

Contiene elementos que especifican la configuración del documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Elemento raíz de un documento Visio Microsoft.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Un archivo MIME (Multipurpose Internet Mail Extensions) codificado por Microsoft Visio de usuario (VSU) que representa barras de herramientas personalizadas.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contiene el nombre del archivo Visio interfaz de usuario (.vsu) de Microsoft que define menús y aceleradores personalizados para un documento.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contiene el nombre del archivo de interfaz de usuario (.vsu) de Microsoft Visio que define barras de herramientas y barras de estado personalizadas para un documento.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica si la característica de cuadrícula dinámica está habilitada para un documento o una ventana.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos a los que se pegan las formas cuando el pegado está habilitado en el documento.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Especifica si se impide que el usuario elimine o edite páginas en segundo plano.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Especifica si el usuario no puede crear, editar o eliminar patrones. Independientemente de esta configuración, el usuario todavía puede crear instancias de patrones.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Especifica si el usuario no puede seleccionar formas que tengan el **elemento LockSelect** establecido en 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Especifica si el usuario no puede crear o editar estilos.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contiene una colección de **elementos SnapAngle.**  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un **elemento StyleSheet.**  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un **elemento StyleSheet.**  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un **elemento StyleSheet.**  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un **elemento StyleSheet.**  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|TopPage  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la página que debe mostrarse cuando Microsoft abre el documento Visio.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

