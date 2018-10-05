---
title: Connect_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383916"
---
# <a name="connecttype-complextype-visio-xml"></a>Connect_Type complexType ('XML de Visio')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|FromPart  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|ToPart  <br/> |xsd: int  <br/> |opcional  <br/> ||Valores del tipo XSD: int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
   

