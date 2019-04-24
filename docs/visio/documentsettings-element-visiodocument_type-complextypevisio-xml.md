---
title: Elemento DocumentSettings (complexType VisioDocument_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Contiene los elementos que especifican la configuración del documento.
ms.openlocfilehash: e86dc5a0875006cb8bd1bbaffd36037a07fd5c0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315221"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>Elemento DocumentSettings (complexType VisioDocument_Type) ("XML" de Visio)

Contiene los elementos que especifican la configuración del documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |El elemento raíz de un documento de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Un archivo de interfaz de usuario de Microsoft Visio (VSU) codificado de MIME (Extensiones multipropósito de correo Internet) que representa barras de herramientas personalizadas.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Contiene el nombre del archivo de interfaz de usuario de Microsoft Visio (. VSU) que define los menús y los aceleradores personalizados para un documento.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Contiene el nombre del archivo de interfaz de usuario de Microsoft Visio (. VSU) que define barras de herramientas y barras de estado personalizadas para un documento.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica si la característica de cuadrícula dinámica está habilitada para un documento o una ventana.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos a los que se pegan las formas cuando está habilitado el pegado en el documento.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Especifica si se impide al usuario eliminar o editar páginas de fondo.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Especifica si se impide que el usuario cree, edite o elimine patrones. Independientemente de esta configuración, el usuario todavía puede crear instancias de patrones.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Especifica si se impide al usuario seleccionar formas que tienen el elemento **LockSelect** establecido en 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Especifica si se impide al usuario crear o editar estilos.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contiene una colección de elementos **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica los objetos a los que se ajustan las formas cuando se activa ajustar en la ventana.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de la **hoja de estilos** .  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de la **hoja de estilos** .  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de la **hoja de estilos** .  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de un elemento de la **hoja de estilos** .  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Página Web  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de la página que debe mostrarse cuando Microsoft Visio abre el documento.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
   

