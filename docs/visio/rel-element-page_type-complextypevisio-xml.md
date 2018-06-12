---
title: Elemento rel (Page_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Especifica una relación con un elemento con el XML de la página correspondiente.
ms.openlocfilehash: 9fc42527d311faa66b0b4041a0f978818ee84595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822925"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a>Elemento rel (Page_Type complexType) ('XML de Visio')

Especifica una relación con un elemento con el XML de la página correspondiente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Pages.XML, masters.xml, recordsets.xml, página # .xml, maestra # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Especifica una instancia de página que XML almacenada en el dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|r: Id.  <br/> |xsd: String  <br/> Consulte Comentarios.  <br/> |necesario  <br/> |Especifica una relación con un elemento.  <br/> |"quitar #"  <br/> Consulte Comentarios.  <br/> |
   
## <a name="remarks"></a>Notas

El valor del atributo **id: r** debe ser un tipo de **ST_RelationshipID** . El tipo **ST_RelationshipID** es una cadena que debe tener el formato '# deshacerse', donde el carácter final debe ser un número. El número debe ser único entre todos los elementos del mismo nivel del elemento **Rel** . 
  
Para obtener más información sobre el tipo de ST_RelationshipID, vea la [especificación ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

