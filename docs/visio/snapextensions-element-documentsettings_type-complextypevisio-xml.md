---
title: Elemento SnapExtensions (complexType DocumentSettings_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334534"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Elemento SnapExtensions (complexType DocumentSettings_Type) ("XML" de Visio)

Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contiene los elementos que especifican la configuración del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Comentarios

El valor del elemento **SnapExtensions** puede ser una suma de los valores de la tabla siguiente. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |No se ajusta a ningún objeto.  <br/> |
|1  <br/> |Se ajusta a la extensión del cuadro de alineación.  <br/> |
|segundo  <br/> |Se ajusta a la extensión del eje central.  <br/> |
|4  <br/> |Ajustar a la extensión tangente a curva.  <br/> |
|8,5  <br/> |Ajustar a la extensión de extremo.  <br/> |
|16  <br/> |Se ajusta a la extensión de punto medio.  <br/> |
|32  <br/> |Se ajusta a la extensión lineal.  <br/> |
|64  <br/> |Ajustar a la extensión de curva.  <br/> |
|128  <br/> |Ajustar a la extensión perpendicular del extremo.  <br/> |
|256  <br/> |Se ajusta a la extensión perpendicular de punto medio.  <br/> |
|512  <br/> |Ajustar a la extensión horizontal del extremo.  <br/> |
|1024  <br/> |Ajustar a la extensión vertical del extremo.  <br/> |
|2048  <br/> |Se ajusta a la extensión del centro de elipses.  <br/> |
|4096  <br/> |Ajustar a la extensión ángulos isométricos.  <br/> |
   

