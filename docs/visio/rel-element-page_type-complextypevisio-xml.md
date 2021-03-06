---
title: Elemento Rel (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Especifica una relación con un elemento con el XML de página correspondiente.
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542782"
---
# <a name="rel-element-page_type-complextype-visio-xml"></a>Elemento Rel (Page_Type complexType) (Visio XML)

Especifica una relación con un elemento con el XML de página correspondiente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Especifica una instancia de XML de página almacenada en el dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> Consulte Comentarios.  <br/> |necesario  <br/> |Especifica una relación con un elemento.  <br/> |"rId#"  <br/> Consulte Comentarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor del atributo **r:id** debe ser **ST_RelationshipID** tipo. El **ST_RelationshipID** es una cadena que debe tener el formato 'rId#', donde el carácter final debe ser un número. El número debe ser único entre todos los elementos del mismo nivel del **elemento Rel.** 
  
Para obtener más información acerca del tipo ST_RelationshipID, vea la especificación [ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

