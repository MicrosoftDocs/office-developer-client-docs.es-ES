---
title: Elemento Shapes (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contiene una colección de elementos Shape.
ms.openlocfilehash: e9f45d1f61b83339274d24aea2c0473adf282bac
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542103"
---
# <a name="shapes-element-shapesheet_type-complextype-visio-xml"></a>Elemento Shapes (ShapeSheet_Type complexType) (Visio XML)

Contiene una colección de elementos Shape.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica una colección de propiedades asociadas a una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen una forma en un **elemento Master**, **Page** o forma de grupo.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

