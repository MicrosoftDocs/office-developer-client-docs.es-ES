---
title: ActionTag_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: 864f4f9b5069fa3968ceb8d3a8db1589113d931a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541417"
---
# <a name="actiontag_type-complextype-visio-xml"></a>ActionTag_Type complexType (Visio XML)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Section_Type  <br/> |
   
## <a name="definition"></a>Definición

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Row](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

Ninguno.
  

