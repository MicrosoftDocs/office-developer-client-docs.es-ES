---
title: DataConnection_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389144"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a>DataConnection_Type complexType ('XML de Visio')

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base de extensión** <br/> |Ninguna  <br/> |
   
## <a name="definition"></a>Definición

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
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
|AlwaysUseConnectionFile  <br/> |Boolean con tipo  <br/> |opcional  <br/> ||Valores del tipo Boolean con tipo.  <br/> |
|Comando  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|ConnectionString  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|FileName  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo XSD: String.  <br/> |
|FriendlyName  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo XSD: String.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd:unsignedInt.  <br/> |
   

