---
title: Elemento FaceName (FaceNames_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contiene información acerca de una fuente.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541018"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>Elemento FaceName (FaceNames_Type complexType) (XML de Visio)

Contiene información acerca de una fuente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contiene una colección de **elementos FaceName.**  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd:string  <br/> |opcional  <br/> |Los juegos de caracteres admitidos de la fuente.  <br/> |Valores del tipo xsd:string.  <br/> |
|Flags  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Marcas que indican lo siguiente: fuente que falta, fuente predeterminada, fuente asiática, fuente compleja, fuente vertical y tipo de fuente.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|NameU  <br/> |xsd:string  <br/> |necesario  <br/> |Nombre de la fuente como una cadena Unicode UTF-16.  <br/> ||
|Panos  <br/> |xsd:string  <br/> |opcional  <br/> |Firma panose de la fuente. Panose es un sistema de clasificación para tipos de letra que los clasifica en función de sus características visuales.  <br/> |Valores del tipo xsd:string.  <br/> |
|UnicodeRanges  <br/> |xsd:string  <br/> |opcional  <br/> |Intervalos Unicode admitidos de la fuente.  <br/> |Valores del tipo xsd:string.  <br/> |
   

