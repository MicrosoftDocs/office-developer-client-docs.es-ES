---
title: Elemento de nombre de fuente (FaceNames_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contiene información acerca de una fuente.
ms.openlocfilehash: 8a66d5294e239e4540939cc7053e1f67a777144d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822086"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Elemento de nombre de fuente (FaceNames_Type complexType) ('XML de Visio')

Contiene información acerca de una fuente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contiene una colección de elementos de **nombre de fuente** .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Juegos de caracteres  <br/> |xsd: String  <br/> |opcional  <br/> |Los conjuntos de caracteres compatibles de la fuente.  <br/> |Valores del tipo XSD: String.  <br/> |
|Marcas  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Marcas que muestran lo siguiente: falta una fuente, fuente predeterminada, fuente asiática, fuente complejo, fuente vertical y tipo de fuente.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|NameU  <br/> |xsd: String  <br/> |necesario  <br/> |El nombre de la fuente como una cadena Unicode UTF-16.  <br/> ||
|Panos  <br/> |xsd: String  <br/> |opcional  <br/> |La firma panose para la fuente. Panose es un sistema de clasificación para los tipos de letra que categorice a ellos en función de sus características visuales.  <br/> |Valores del tipo XSD: String.  <br/> |
|UnicodeRanges  <br/> |xsd: String  <br/> |opcional  <br/> |Los intervalos admitidos de Unicode de la fuente.  <br/> |Valores del tipo XSD: String.  <br/> |
   

