---
title: Elemento SnapExtensions (DocumentSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Especifica si una opción de configuración de extensión del complemento específico está habilitado o deshabilitado para la ventana activa.
ms.openlocfilehash: 4c00d8d45c1eb33f57f727779db91e358a83a969
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823270"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Elemento SnapExtensions (DocumentSettings_Type complexType) ('XML de Visio')

Especifica si una opción de configuración de extensión del complemento específico está habilitado o deshabilitado para la ventana activa. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contiene elementos que especifican la configuración de documentos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Observaciones

El valor del elemento **SnapExtensions** puede ser una suma de los valores en la tabla siguiente. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No se ajusta a ningún objeto.  <br/> |
|1  <br/> |Se ajusta a la extensión del cuadro de alineación.  <br/> |
|2  <br/> |Se ajusta a la extensión del centro del eje.  <br/> |
|4  <br/> |Se ajusta a la extensión tangentes de curva.  <br/> |
|8  <br/> |Se ajusta a la extensión del extremo.  <br/> |
|16  <br/> |Se ajusta a la extensión de punto medio.  <br/> |
|32  <br/> |Se ajusta a la extensión lineal.  <br/> |
|64  <br/> |Se ajusta a la extensión de la curva.  <br/> |
|128  <br/> |Se ajusta a la extensión perpendicular de extremo.  <br/> |
|256  <br/> |Se ajusta a la extensión perpendicular de punto medio.  <br/> |
|512  <br/> |Se ajusta a la extensión de extremo horizontal.  <br/> |
|1024  <br/> |Se ajusta a la extensión de extremo vertical.  <br/> |
|2048  <br/> |Se ajusta a la extensión de centro de elipse.  <br/> |
|4096  <br/> |Se ajusta a la extensión de ángulos isométrica.  <br/> |
   

