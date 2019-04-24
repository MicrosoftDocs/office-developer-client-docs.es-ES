---
title: Elemento FaceName (complexType FaceNames_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contiene información acerca de una fuente.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322606"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Elemento FaceName (complexType FaceNames_Type) ("XML" de Visio)

Contiene información acerca de una fuente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contiene una colección de elementos **FaceName** .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Juegos de caracteres  <br/> |xsd: String  <br/> |opcional  <br/> |Los juegos de caracteres admitidos de la fuente.  <br/> |Valores del tipo xsd: String.  <br/> |
|Flags  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Marcas que indican lo siguiente: fuente que falta, fuente predeterminada, fuente asiática, fuente compleja, fuente vertical y tipo de fuente.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|NameU  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre de la fuente como una cadena Unicode UTF-16.  <br/> ||
|Panos  <br/> |xsd: String  <br/> |opcional  <br/> |La firma Panose de la fuente. Panose es un sistema de clasificación para los tipos de letra que los clasifica en función de sus características visuales.  <br/> |Valores del tipo xsd: String.  <br/> |
|UnicodeRanges  <br/> |xsd: String  <br/> |opcional  <br/> |Rangos Unicode admitidos de la fuente.  <br/> |Valores del tipo xsd: String.  <br/> |
   

