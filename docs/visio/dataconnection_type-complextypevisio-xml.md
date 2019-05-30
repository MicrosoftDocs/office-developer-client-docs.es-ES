---
title: ComplexType DataConnection_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539652"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a>ComplexType DataConnection_Type (XML de Visio)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base de extensión** <br/> |Ninguno  <br/> |
   
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

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd: Boolean  <br/> |opcional  <br/> ||Valores del tipo xsd: Boolean.  <br/> |
|Command  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
|ConnectionString  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
|FileName  <br/> |xsd: String  <br/> |necesario  <br/> ||Valores del tipo xsd: String.  <br/> |
|FriendlyName  <br/> |xsd: String  <br/> |opcional  <br/> ||Valores del tipo xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
|Timeout  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> ||Valores del tipo xsd: unsignedInt.  <br/> |
   

