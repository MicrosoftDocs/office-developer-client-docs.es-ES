---
title: Elemento SnapAngles (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 803ddfc1-b7d3-736f-2d85-7b8780ef9278
description: Contiene una colección de elementos SnapAngle.
ms.openlocfilehash: d0b2c2a0643b4f3bccd5b450ef0d9c89ce9ab7c2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540395"
---
# <a name="snapangles-element-documentsettings_type-complextype-visio-xml"></a>Elemento SnapAngles (DocumentSettings_Type complexType) (Visio XML)

Contiene una colección de **elementos SnapAngle.** 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contiene elementos que especifican la configuración del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[SnapAngle](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[SnapAngle_Type](snapangle_type-complextypevisio-xml.md) <br/> |Contiene un número de punto flotante que especifica un ángulo de ajuste en grados.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

