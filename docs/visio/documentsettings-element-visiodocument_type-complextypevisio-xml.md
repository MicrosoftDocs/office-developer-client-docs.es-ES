---
title: Elemento de DocumentSettings (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contiene elementos que especifican la configuración de documentos.
ms.openlocfilehash: 8cd10e43b95918ccd2ceaa75a47c9e93de2acc14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822010"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>Elemento de DocumentSettings (VisioDocument_Type complexType) ('XML de Visio')

Contiene elementos que especifican la configuración de documentos.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |El elemento raíz de un documento de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |MIME (Extensiones multipropósito de correo Internet) con una codificación de archivo de (VSU) de la interfaz de usuario de Microsoft Visio que representa las barras de herramientas personalizadas.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contiene el nombre del archivo de interfaz (.vsu) de usuario de Microsoft Visio que define menús y aceleradores para un documento personalizados.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contiene el nombre del archivo de interfaz (.vsu) de usuario de Microsoft Visio que define las barras de herramientas personalizadas y las barras de estado para un documento.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica si está habilitada la característica de cuadrícula dinámica de un documento o ventana.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos que se pegan las formas cuando el pegado está habilitado en el documento.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Especifica si el usuario no puede eliminar o modificar las páginas de fondo.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Especifica si el usuario impide crear, editar o eliminar a los patrones. Independientemente de esta configuración, el usuario puede crear instancias de patrones.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Especifica si se impide que el usuario la selección de las formas que tienen su elemento **LockSelect** establecida en 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Especifica si el usuario impide crear o editar los estilos.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contiene una colección de elementos de **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica si una opción de configuración de extensión del complemento específico está habilitado o deshabilitado para la ventana activa.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos que las formas ajustan ajustar cuando está en la ventana activa.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de **hoja de estilos** .  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de **hoja de estilos** .  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de **hoja de estilos** .  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de **hoja de estilos** .  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|TopPage  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la página que se debe mostrar cuando se abre el documento de Microsoft Visio.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

